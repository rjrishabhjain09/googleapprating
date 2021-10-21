# Google App Rating
### Exploratory Analysis and Visualization
In statistics, exploratory data analysis is an approach to analyzing data sets to summarize their main characteristics, often with visual methods. A statistical model can be used or not, but primarily EDA is for seeing what the data can tell us beyond the formal modeling or hypothesis testing task. Data visualization is the graphic representation of data. It involves producing images that communicate relationships among the represented data to viewers of the images.
```
klib.cat_plot(df) # returns a visualization of the number and frequency of categorical features
```
![](https://stream-download.herokuapp.com/53292)

```
klib.corr_mat(df) # returns a color-encoded correlation matrix
```
![](https://stream-download.herokuapp.com/53308)
```
klib.corr_plot(df) # returns a color-encoded heatmap, ideal for correlations
```
![](https://stream-download.herokuapp.com/53310)
```
klib.dist_plot(df) # returns a distribution plot for every numeric feature
```
![](https://stream-download.herokuapp.com/53314)
![](https://stream-download.herokuapp.com/53319)
![](https://stream-download.herokuapp.com/53321)
![](https://stream-download.herokuapp.com/53323)

```
klib.missingval_plot(df) # returns a figure containing information about missing values
```
![](https://stream-download.herokuapp.com/53327)


```
klib.pool_duplicate_subsets(df) # pools subset of cols based on duplicates with min. loss of information
```
![](https://stream-download.herokuapp.com/53330)

```
sns.pairplot(df, size=7)
```
![](https://stream-download.herokuapp.com/53332)

```
# Plot a Boxplot
plt.figure(figsize=(20,20))
df.boxplot()
```
![](https://stream-download.herokuapp.com/53335)

```
# Plot a heatmap
sns.heatmap(df.corr(),annot=True)
```
![](https://stream-download.herokuapp.com/53338)

```
plt.figure(figsize=(18,13))
plt.xlabel("Count")
plt.ylabel("Category")

graph = sns.barplot(x = xsis, y = ysis, palette= "husl")
graph.set_title("Top categories on Google Playstore", fontsize = 25);
```
![](https://stream-download.herokuapp.com/53340)


```
plt.figure(figsize=(12,10))
plt.bar(x2sis,y2sis,width=0.8,color=['#15244C','#FFFF48','#292734','#EF2920','#CD202D','#ECC5F2'], alpha=0.8);
plt.title('Content Rating',size = 20);
plt.ylabel('Apps(Count)');
plt.xlabel('Content Rating');
```
![](https://stream-download.herokuapp.com/53342)

```
plt.figure(figsize=(15,9))
plt.xlabel("Rating")
plt.ylabel("Frequency")
graph = sns.kdeplot(df.Rating, color="Blue", shade = True)
plt.title('Distribution of Rating',size = 20);
```
![](https://stream-download.herokuapp.com/53344)


```
plt.figure(figsize=(10,10))
labels = df['Type'].value_counts(sort = True).index
sizes = df['Type'].value_counts(sort = True)
colors = ["blue","lightgreen"]
explode = (0.2,0)
plt.pie(sizes, explode=explode, labels=labels, colors=colors, autopct='%1.1f%%', shadow=True, startangle=0)
plt.title('Percent of Free Vs Paid Apps in store',size = 20)
plt.show()
```
![](https://stream-download.herokuapp.com/53346)


```
x2sis = []
y2sis = []

for i in range(len(highest_Installs_df)):
    x2sis.append(highest_Installs_df.Installs[i])
    y2sis.append(highest_Installs_df.index[i])

plt.figure(figsize=(18,13))

plt.xlabel("Installs")
plt.ylabel("Category")
graph = sns.barplot(x = x2sis, y = y2sis, alpha =0.9, palette= "viridis")
graph.set_title("Installs", fontsize = 25);
```
![](https://stream-download.herokuapp.com/53348)



```
findtop10incategory('Sports')
```
![](https://stream-download.herokuapp.com/53350)


```
plt.figure(figsize=(15,12));
plt.pie(top10PaidApps_df.Installs, explode=None, labels=top10PaidApps_df.App, autopct='%1.1f%%', startangle=0);
plt.title('Top Expensive Apps Distribution',size = 20);
plt.legend(top10PaidApps_df.App, 
           loc="lower right",
           title="Apps",
           fontsize = "xx-small"
          );
```
![](https://stream-download.herokuapp.com/53353)


```
df.sort_values(by='Reviews', ascending=False).head(20)
```
![](https://stream-download.herokuapp.com/53356)


```
plt.figure(figsize=(15,9))
plt.ylabel('Genres(App Count)')
plt.xlabel('Genres')
graph = sns.barplot(x=x3sis,y=y3sis,palette="deep")
graph.set_xticklabels(graph.get_xticklabels(), rotation=90, fontsize=12)
graph.set_title("Top Genres in the Playstore", fontsize = 20);
```
![](https://stream-download.herokuapp.com/53359)




```
# PLot a bar chart of earning at y and app names at x
plt.figure(figsize=(15,9))
plt.bar(earning_df_sorted_by_Price.App, earning_df_sorted_by_Price.Earnings, width=1.1, label=earning_df_sorted_by_Price.Earnings)
plt.xlabel("Apps")
plt.ylabel("Earnings")
plt.tick_params(rotation=90)
plt.title("Top Earning Apps");
```
![](https://stream-download.herokuapp.com/53361)


### Thankyou 
***




