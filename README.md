# State of Non-Workers in Uttarakhand (Census 2011)
---

Unemployment has been a burning issue in the country. But add **non-workers** to the mix and you have yourself a peculiar problem. This project aims to share observations regarding the trends among non-workers in the state of Uttarakhand, India. Two things caught my eye but we will get to that after going over some basics.


## 1. Basics
---

### Definition
Non-workers are defined as those who do not participate in any economic activity — paid or unpaid, household duties, or cultivation.

These non-workers survive on the:
* House Rents; or,
* Pensions; or,
* Government Unemployment Transfers; or,
* DaddyJi ve cash 💸

### Methodology
I initially charted the total number of non-workers in every development block per district. But soon realized it didn't give an apt picture of where government efforts should be prioritized as some development blocks had high non-worker density because they were more greatly populated than other regions. For example,

![alt text](https://github.com/dtolia/nonworker-analysisUK/blob/main/charts/incorrectPlotPithoragarh.png "Incorrect Plot for District Pithoragarh")

The graph above shows **Gangolihat** as the hub of non-workers, totaling approx. 38k people! But it is also true that Gangolihat is more densely populated than other blocks in the district. So, as a workaround, I calculated the *non-worker percentage against the total population* for each development block through:

```python
df_pct = df_cdb.assign(non_working_population_percent=((df_cdb['Non Working Population Person']/df_cdb['Total Population Person']) * 100))
```

The resulting plot was very different:

![alt text](https://github.com/dtolia/nonworker-analysisUK/blob/main/charts/1_Pithoragarh.png "Correct Plot for District Pithoragarh")

Gangolihat is no longer in the top 3, replaced by **Berinag**. While an obscure **Kanali Chhina** has come to the forefront. 
And friends, this is how data can be misinterpreted to transfer funds to the wrong places. Incorrect policies could also be implemented as a result.


## 2. Observation -1
---
