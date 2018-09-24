# VisualizationPandas
# This formats the plots such that they appear on separate rows
fig, axes = plt.subplots(nrows=2, ncols=1)
# Plot the PDF
df.fraction.plot(ax=axes[0], kind='hist', bins=30, normed=True, range=(0,.3))
plt.show()
# Plot the CDF
df.fraction.plot(ax=axes[1], kind='hist', bins=30, normed=True, cumulative=True, range=(0,.3))
plt.show()

# Print the number of countries reported in 2015
print(df['2015'].count())
# Print the 5th and 95th percentiles
print(df.quantile([0.05,0.95]))
# Generate a box plot
years = ['1800','1850','1900','1950','2000']
df[years].plot(kind='box')
plt.show()

# Extract data from 2010-Aug-01 to 2010-Aug-15: unsmoothed
unsmoothed = df['Temperature']['2010-Aug-01':'2010-Aug-15']
# Apply a rolling mean with a 24 hour window: smoothed
smoothed = unsmoothed.rolling(window=24).mean()
# Create a new DataFrame with columns smoothed and unsmoothed: august
august = pd.DataFrame({'smoothed':smoothed, 'unsmoothed':unsmoothed})
# Plot both smoothed and unsmoothed data using august.plot().
august.plot()
plt.show()

Pandas groupby:
# Group titanic by 'pclass': by_class
by_class = titanic.groupby('pclass')
# Select 'age' and 'fare'
by_class_sub = by_class[['age','fare']]
# Aggregate by_class_sub by 'max' and 'median': aggregated
aggregated = by_class_sub.agg(['max','median'])
# Print the maximum age in each class
print(aggregated.loc[:, ('age','max')])
# Print the median fare in each class
print(print(aggregated.loc[:,('fare','median')]))

MANIPULATING DATA FRAMES
# Select the 'NOC' column of medals: country_names
country_names = medals['NOC']
# Count the number of medals won by each country: medal_counts
medal_counts = country_names.value_counts()
print(medal_counts.head(15))

# Construct the pivot table: counted
counted = medals.pivot_table(index='NOC',values='Athlete',columns='Medal',aggfunc='count')
# Create the new column: counted['totals']
counted['totals'] = counted.sum(axis='columns')
# Sort counted by the 'totals' column
counted = counted.sort_values('totals',ascending=False)
print(counted.head(15))

# Select columns: ev_gen
ev_gen = medals[['Event_gender','Gender']]
# Drop duplicate pairs: ev_gen_uniques
ev_gen_uniques = ev_gen.drop_duplicates()
print(ev_gen_uniques)

# Group medals by the two columns: medals_by_gender
medals_by_gender = medals.groupby(['Event_gender','Gender'])
# Create a DataFrame with a group count: medal_count_by_gender
medal_count_by_gender = medals_by_gender.count()
print(medal_count_by_gender)

# Create the Boolean Series: sus
sus = (medals.Event_gender=='W')&(medals.Gender=='Men')
# Create a DataFrame with the suspicious row: suspect
suspect = medals.loc[sus]
print(suspect)

# Group medals by 'NOC': country_grouped
country_grouped = medals.groupby('NOC')
# Compute the number of distinct sports in which each country won medals: Nsports
Nsports = country_grouped['Sport'].nunique()
# Sort the values of Nsports in descending order
Nsports = Nsports.sort_values(ascending=False)
print(Nsports.head(15))

# Extract all rows for which the 'Edition' is between 1952 & 1988: during_cold_war
during_cold_war =((medals['Edition']>=1952)&(medals['Edition']<=1988))
# Extract rows for which 'NOC' is either 'USA' or 'URS': is_usa_urs
is_usa_urs = medals.NOC.isin(['USA','URS'])
# Use during_cold_war and is_usa_urs to create the DataFrame: cold_war_medals
cold_war_medals = medals.loc[during_cold_war & is_usa_urs]
# Group cold_war_medals by 'NOC'
country_grouped = cold_war_medals.groupby('NOC')
Nsports = country_grouped['Sport'].nunique().sort_values(ascending=False)
print(Nsports)

# Create the pivot table: medals_won_by_country
medals_won_by_country = medals.pivot_table(index='Edition',values='Athlete',columns='NOC',aggfunc='count')
# Slice medals_won_by_country: cold_war_usa_usr_medals
cold_war_usa_usr_medals = medals_won_by_country.loc[1952:1988, ['USA','URS']]
# Create most_medals 
most_medals = cold_war_usa_usr_medals.idxmax(axis='columns')
print(most_medals.value_counts())

# Define count_entries()
def count_entries(csv_file,c_size,colname):
    """Return a dictionary with counts of
    occurrences as value for each key."""
    # Initialize an empty dictionary: counts_dict
    counts_dict = {}
    # Iterate over the file chunk by chunk
    for chunk in pd.read_csv(csv_file,chunksize=c_size):
        # Iterate over the column in DataFrame
        for entry in chunk[colname]:
            if entry in counts_dict.keys():
                counts_dict[entry] += 1
            else:
                counts_dict[entry] = 1
    return counts_dict
# Call count_entries(): result_counts
result_counts = count_entries('tweets.csv',10,'lang')
print(result_counts)

def plot_pop(filename, country_code):
    # Initialize reader object: urb_pop_reader
    urb_pop_reader = pd.read_csv(filename, chunksize=1000)
    # Initialize empty DataFrame: data
    data = pd.DataFrame()
    # Iterate over each DataFrame chunk
    for df_urb_pop in urb_pop_reader:
        # Check out specific country: df_pop_ceb
        df_pop_ceb = df_urb_pop[df_urb_pop['CountryCode'] == country_code]
        # Zip DataFrame columns of interest: pops
        pops = zip(df_pop_ceb['Total Population'],
                    df_pop_ceb['Urban population (% of total)'])
        # Turn zip object into list: pops_list
        pops_list = list(pops)
        # Use list comprehension to create new DataFrame column 'Total Urban Population'
        df_pop_ceb['Total Urban Population'] = [int(tup[0] * tup[1]) for tup in pops_list]
        # Append DataFrame chunk to data: data
        data = data.append(df_pop_ceb)
    # Plot urban population data
    data.plot(kind='scatter', x='Year', y='Total Urban Population')
    plt.show()
# Set the filename: fn
fn = 'ind_pop_data.csv'
# Call plot_pop for country code 'CEB'
plot_pop('ind_pop_data.csv','CEB')
# Call plot_pop for country code 'ARB'
plot_pop('ind_pop_data.csv','ARB')
