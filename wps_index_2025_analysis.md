## Data Source: Women, Peace and Security (WPS) Index 2025/26

The dataset used in this analysis comes from the **Women, Peace and Security (WPS) Index 2025/26**, produced by the **Georgetown Institute for Women, Peace and Security (GIWPS)** in collaboration with the **Peace Research Institute Oslo (PRIO)**, with support from the Government of Norway.

The WPS Index evaluates and ranks **181 countries** based on women’s overall wellbeing. Scores range from **0 (worst)** to **1 (best)** and are calculated using **13 indicators** that span three core dimensions:

Each row in the dataset represents a single country, and each column represents either an overall index score, a rank, or one of the component indicators used to compute the final score.

According to the 2025/26 Index, **Denmark ranks highest globally**, while **Afghanistan ranks lowest**, highlighting persistent global inequalities in women’s status. The report notes that global progress on women’s rights has stalled in recent years, though improvements have occurred in some conflict-affected countries.

The WPS Index is designed to support evidence-based policymaking, track trends over time, and hold governments accountable for commitments to advance women’s rights and security.

Source: Georgetown Institute for Women, Peace and Security (GIWPS), Women, Peace and Security Index 2025/26.



```python
import pandas as pd
import matplotlib.pyplot as plt
import plotly.express as px

df = pd.read_csv("data/wps-index-2025-analysis.csv")
df.head()

```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>WPS Index Rank</th>
      <th>Country</th>
      <th>Code</th>
      <th>Women, Peace, and Security Index</th>
      <th>Region</th>
      <th>Education</th>
      <th>Employment</th>
      <th>Financial Inclusion</th>
      <th>Cell Phone Use</th>
      <th>Parliamentary Representation</th>
      <th>Absence of Legal Discrimination</th>
      <th>Access to Justice</th>
      <th>Maternal Mortality Ratio</th>
      <th>Son Bias</th>
      <th>Intimate partner violence</th>
      <th>Community Safety</th>
      <th>Political Violence Targeting Women</th>
      <th>Proximity to Conflict</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>1</td>
      <td>Denmark</td>
      <td>DNK</td>
      <td>0.939</td>
      <td>DC</td>
      <td>13.2</td>
      <td>77.9</td>
      <td>100.0</td>
      <td>100.0</td>
      <td>43.6</td>
      <td>100.0</td>
      <td>4.0</td>
      <td>4.0</td>
      <td>105.6</td>
      <td>3.3</td>
      <td>85.0</td>
      <td>0.0</td>
      <td>0.0</td>
    </tr>
    <tr>
      <th>1</th>
      <td>2</td>
      <td>Iceland</td>
      <td>ISL</td>
      <td>0.932</td>
      <td>DC</td>
      <td>13.9</td>
      <td>83.7</td>
      <td>100.0</td>
      <td>100.0</td>
      <td>46.0</td>
      <td>100.0</td>
      <td>3.4</td>
      <td>3.0</td>
      <td>105.9</td>
      <td>2.8</td>
      <td>82.0</td>
      <td>0.0</td>
      <td>0.0</td>
    </tr>
    <tr>
      <th>2</th>
      <td>3</td>
      <td>Norway</td>
      <td>NOR</td>
      <td>0.924</td>
      <td>DC</td>
      <td>13.1</td>
      <td>78.6</td>
      <td>100.0</td>
      <td>100.0</td>
      <td>44.4</td>
      <td>96.9</td>
      <td>3.7</td>
      <td>1.0</td>
      <td>106.1</td>
      <td>4.4</td>
      <td>86.0</td>
      <td>0.0</td>
      <td>0.0</td>
    </tr>
    <tr>
      <th>3</th>
      <td>3</td>
      <td>Sweden</td>
      <td>SWE</td>
      <td>0.924</td>
      <td>DC</td>
      <td>12.8</td>
      <td>82.2</td>
      <td>100.0</td>
      <td>100.0</td>
      <td>45.0</td>
      <td>100.0</td>
      <td>3.7</td>
      <td>4.0</td>
      <td>105.6</td>
      <td>6.3</td>
      <td>74.0</td>
      <td>0.0</td>
      <td>0.0</td>
    </tr>
    <tr>
      <th>4</th>
      <td>5</td>
      <td>Finland</td>
      <td>FIN</td>
      <td>0.921</td>
      <td>DC</td>
      <td>13.1</td>
      <td>78.4</td>
      <td>99.1</td>
      <td>100.0</td>
      <td>45.5</td>
      <td>97.5</td>
      <td>3.5</td>
      <td>8.0</td>
      <td>105.2</td>
      <td>8.1</td>
      <td>78.0</td>
      <td>0.0</td>
      <td>0.0</td>
    </tr>
  </tbody>
</table>
</div>




```python
df.shape

```




    (181, 18)




```python
df.info()
```

    <class 'pandas.core.frame.DataFrame'>
    RangeIndex: 181 entries, 0 to 180
    Data columns (total 18 columns):
     #   Column                              Non-Null Count  Dtype  
    ---  ------                              --------------  -----  
     0   WPS Index Rank                      181 non-null    int64  
     1   Country                             181 non-null    object 
     2   Code                                181 non-null    object 
     3   Women, Peace, and Security Index    181 non-null    float64
     4   Region                              181 non-null    object 
     5   Education                           181 non-null    float64
     6   Employment                          181 non-null    float64
     7   Financial Inclusion                 181 non-null    float64
     8   Cell Phone Use                      181 non-null    float64
     9   Parliamentary Representation        181 non-null    float64
     10  Absence of Legal Discrimination     181 non-null    float64
     11  Access to Justice                   181 non-null    float64
     12  Maternal Mortality Ratio            181 non-null    float64
     13  Son Bias                            181 non-null    float64
     14  Intimate partner violence           181 non-null    float64
     15  Community Safety                    181 non-null    float64
     16  Political Violence Targeting Women  181 non-null    float64
     17  Proximity to Conflict               181 non-null    float64
    dtypes: float64(14), int64(1), object(3)
    memory usage: 25.6+ KB
    


```python
df.describe()
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>WPS Index Rank</th>
      <th>Women, Peace, and Security Index</th>
      <th>Education</th>
      <th>Employment</th>
      <th>Financial Inclusion</th>
      <th>Cell Phone Use</th>
      <th>Parliamentary Representation</th>
      <th>Absence of Legal Discrimination</th>
      <th>Access to Justice</th>
      <th>Maternal Mortality Ratio</th>
      <th>Son Bias</th>
      <th>Intimate partner violence</th>
      <th>Community Safety</th>
      <th>Political Violence Targeting Women</th>
      <th>Proximity to Conflict</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>count</th>
      <td>181.000000</td>
      <td>181.000000</td>
      <td>181.000000</td>
      <td>181.00000</td>
      <td>181.000000</td>
      <td>181.000000</td>
      <td>181.000000</td>
      <td>181.000000</td>
      <td>181.000000</td>
      <td>181.000000</td>
      <td>181.000000</td>
      <td>181.000000</td>
      <td>181.000000</td>
      <td>181.000000</td>
      <td>181.000000</td>
    </tr>
    <tr>
      <th>mean</th>
      <td>90.756906</td>
      <td>0.683110</td>
      <td>8.780110</td>
      <td>60.30442</td>
      <td>61.716022</td>
      <td>84.903867</td>
      <td>26.022652</td>
      <td>78.256354</td>
      <td>2.431492</td>
      <td>119.171271</td>
      <td>105.060773</td>
      <td>11.605525</td>
      <td>59.724862</td>
      <td>0.108840</td>
      <td>16.676243</td>
    </tr>
    <tr>
      <th>std</th>
      <td>52.426314</td>
      <td>0.142989</td>
      <td>3.573427</td>
      <td>18.53927</td>
      <td>27.718245</td>
      <td>14.547999</td>
      <td>12.128222</td>
      <td>16.818215</td>
      <td>0.841528</td>
      <td>169.212542</td>
      <td>1.643965</td>
      <td>7.447003</td>
      <td>16.416005</td>
      <td>0.320814</td>
      <td>29.663866</td>
    </tr>
    <tr>
      <th>min</th>
      <td>1.000000</td>
      <td>0.279000</td>
      <td>0.900000</td>
      <td>5.50000</td>
      <td>4.200000</td>
      <td>28.000000</td>
      <td>0.300000</td>
      <td>26.300000</td>
      <td>0.100000</td>
      <td>1.000000</td>
      <td>101.100000</td>
      <td>1.700000</td>
      <td>17.000000</td>
      <td>0.000000</td>
      <td>0.000000</td>
    </tr>
    <tr>
      <th>25%</th>
      <td>46.000000</td>
      <td>0.590000</td>
      <td>5.800000</td>
      <td>51.60000</td>
      <td>38.800000</td>
      <td>77.400000</td>
      <td>17.900000</td>
      <td>70.600000</td>
      <td>1.900000</td>
      <td>11.000000</td>
      <td>103.900000</td>
      <td>5.900000</td>
      <td>46.000000</td>
      <td>0.000000</td>
      <td>0.000000</td>
    </tr>
    <tr>
      <th>50%</th>
      <td>89.000000</td>
      <td>0.685000</td>
      <td>9.600000</td>
      <td>62.30000</td>
      <td>62.600000</td>
      <td>90.000000</td>
      <td>26.200000</td>
      <td>81.300000</td>
      <td>2.500000</td>
      <td>47.000000</td>
      <td>105.100000</td>
      <td>9.100000</td>
      <td>60.000000</td>
      <td>0.000000</td>
      <td>0.000000</td>
    </tr>
    <tr>
      <th>75%</th>
      <td>135.000000</td>
      <td>0.797000</td>
      <td>11.800000</td>
      <td>75.80000</td>
      <td>87.300000</td>
      <td>95.000000</td>
      <td>34.100000</td>
      <td>90.600000</td>
      <td>3.000000</td>
      <td>155.000000</td>
      <td>106.000000</td>
      <td>16.700000</td>
      <td>71.000000</td>
      <td>0.100000</td>
      <td>18.600000</td>
    </tr>
    <tr>
      <th>max</th>
      <td>181.000000</td>
      <td>0.939000</td>
      <td>14.000000</td>
      <td>90.00000</td>
      <td>100.000000</td>
      <td>100.000000</td>
      <td>61.300000</td>
      <td>100.000000</td>
      <td>4.000000</td>
      <td>993.000000</td>
      <td>111.300000</td>
      <td>35.600000</td>
      <td>97.000000</td>
      <td>3.000000</td>
      <td>100.000000</td>
    </tr>
  </tbody>
</table>
</div>



## Dataset Structure and Overview

The dataset contains **181 rows and 18 columns**, meaning that it includes data for **181 countries**, each described by **18 variables** related to women’s wellbeing, inclusion, justice, and security.

Each row represents a single country, while each column represents either the overall Women, Peace, and Security (WPS) Index score, the country’s rank, or one of the component indicators used to construct the index.

## Data Types and Completeness

An examination of the dataset structure shows that **all 181 entries are complete**, with no missing values across any of the 18 columns. This indicates a high-quality dataset suitable for analysis without the need for imputation or data cleaning.

The dataset includes:
- **1 integer column** (`WPS Index Rank`)
- **3 categorical (object) columns** (`Country`, `Code`, and `Region`)
- **14 numeric (float) columns**, representing index scores and component indicators

The numeric columns measure a wide range of dimensions, including education, employment, financial inclusion, safety, justice, and exposure to conflict.

## Summary Statistics

The summary statistics reveal substantial variation across countries in women’s wellbeing and security:

- The **average WPS Index score** is approximately **0.68**, with scores ranging from **0.279** (lowest-performing country) to **0.939** (highest-performing country).
- The **mean rank** is approximately **91**, reflecting the midpoint of the 181-country ranking.
- Indicators such as **Education**, **Employment**, and **Financial Inclusion** show wide dispersion, suggesting significant global inequality in women’s access to opportunities.
- **Maternal Mortality Ratio** exhibits particularly high variability, ranging from **1** to **993**, highlighting stark differences in women’s health outcomes across countries.
- Several security-related indicators, including **Political Violence Targeting Women** and **Proximity to Conflict**, have medians of **0**, indicating that while many countries experience low levels of these risks, others face extreme conditions.

Overall, the descriptive statistics confirm that the dataset captures substantial cross-national differences in women’s status and security, making it well-suited for comparative analysis and visualization.



```python
df['Women, Peace, and Security Index'].hist(bins=20)
plt.title("Distribution of Women, Peace and Security Index Scores (2025/26)")
plt.xlabel("WPS Index Score")
plt.ylabel("Number of Countries")
plt.show()
```


    
![png](wps_index_2025_analysis_files/wps_index_2025_analysis_6_0.png)
    


This histogram shows the distribution of WPS Index scores across 181 countries.
Most countries fall within the middle range of scores, with relatively few countries
achieving very high or very low values. This highlights persistent global disparities
in women’s wellbeing, even as many countries cluster around moderate outcomes.



```python
top10 = df.sort_values(
    'Women, Peace, and Security Index',
    ascending=False
).head(10)

bottom10 = df.sort_values(
    'Women, Peace, and Security Index'
).head(10)

plt.barh(top10['Country'], top10['Women, Peace, and Security Index'])
plt.title("Top 10 Countries by WPS Index Score")
plt.xlabel("WPS Index Score")
plt.ylabel("Country")
plt.gca().invert_yaxis()
plt.show()

```


    
![png](wps_index_2025_analysis_files/wps_index_2025_analysis_8_0.png)
    


This chart highlights the top-performing countries on the WPS Index. These countries
tend to combine strong legal protections, high levels of inclusion, and lower exposure
to violence, illustrating how multiple dimensions contribute to overall performance.



```python
plt.scatter(
    df['Absence of Legal Discrimination'],
    df['Parliamentary Representation']
)
plt.title("Legal Equality vs Women’s Parliamentary Representation")
plt.xlabel("Absence of Legal Discrimination Score")
plt.ylabel("Women in Parliament (%)")
plt.show()

```


    
![png](wps_index_2025_analysis_files/wps_index_2025_analysis_10_0.png)
    


This plot compares legal protections for women with their political representation.
While countries with stronger legal frameworks tend to perform better, the wide spread
suggests that legal equality alone does not guarantee meaningful political inclusion.



```python
fig = px.choropleth(
    df,
    locations="Code",  # ISO-3 country codes
    color="Women, Peace, and Security Index",
    hover_name="Country",
    color_continuous_scale="Viridis",
    title="Global Distribution of the Women, Peace and Security Index"
)

fig.show()
```



This choropleth map visualizes the global distribution of the Women, Peace and Security
Index. Higher scores are concentrated in Europe and parts of North America, while
lower scores are more prevalent in regions affected by conflict and instability.
The map highlights strong regional patterns and underscores global inequalities
in women’s wellbeing, security, and inclusion.


# Cultural–Historical Context and WPS Index Outcomes


```python
pagan_tengrist_countries = [ ### grouped all countries with significant Pagan or Tengrist heritage
    "Denmark", "Norway", "Sweden", "Finland", "Iceland",
    "Estonia", "Latvia", "Lithuania",
    "Mongolia", "Kazakhstan", "Kyrgyzstan"
]

df["Cultural Group"] = df["Country"].apply(
    lambda x: "Pagan / Tengrist Heritage" if x in pagan_tengrist_countries else "Other"
)


```


```python
group_means = ( ### calculate mean WPS Index by Cultural Group
    df.groupby("Cultural Group")["Women, Peace, and Security Index"]
    .mean()
    .reset_index()
)
group_means

```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Cultural Group</th>
      <th>Women, Peace, and Security Index</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>Other</td>
      <td>0.671282</td>
    </tr>
    <tr>
      <th>1</th>
      <td>Pagan / Tengrist Heritage</td>
      <td>0.865909</td>
    </tr>
  </tbody>
</table>
</div>




```python
import matplotlib.pyplot as plt ### plot average WPS Index by Cultural Group

plt.figure()
plt.bar(
    group_means["Cultural Group"],
    group_means["Women, Peace, and Security Index"]
)
plt.title("Average Women, Peace and Security Index by Cultural-Historical Group")
plt.ylabel("Average WPS Index")
plt.xlabel("Cultural Group")
plt.show()

```


    
![png](wps_index_2025_analysis_files/wps_index_2025_analysis_17_0.png)
    


This chart compares average Women, Peace and Security Index scores between countries
with historical roots in pagan or Tengrist cultural traditions and all other countries.
The grouping is exploratory and based on historical-cultural heritage rather than
contemporary religious practice. While the results suggest higher average WPS scores
among countries in the Pagan/Tengrist heritage group, this analysis does not imply
causation. Instead, it highlights a potential association between long-standing cultural
norms and modern institutional outcomes, warranting further research.
