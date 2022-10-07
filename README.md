# State of Non-Workers in Uttarakhand (Census 2011)
---

Unemloyment has been a burning issue in the country. But add 'non-workers' to the mix and you have yourself a peculiar problem. The aim of this project is to share observations regarding the trends among non-workers in the state of Uttarakhand, India. There were two things that caught my eye but we will get to that after going over some basics.


## 1. Basics
---

### Definition
Non-workers are defined as those who do not participate in any economic activity — paid or unpaid, household duties, or cultivation.

These non-workers survive on:
* House Rents; or,
* Pensions; or,
* Government Unemployment Transfers; or,
* Daddy ji ve cash 💸

### Methodology
I initially charted the total number of non-workers in every development block per district. But soon realised it didn't give an apt picture of where govenment efforts should be prioritised as some development blocks had high non-worker density because they were greatly populated than other regions. For example,

![alt text](https://github.com/adam-p/markdown-here/raw/master/src/common/images/icon48.png "Logo Title Text 1")

The graph above shows 'Gangolihat' as the hub of non-workers, totaling to approx. 38k! But it is also true that Gangolihat is more densely populated than other blocks in the district.
So, as a workaround, I calculated 'non-worker percentage against total population' for each development block through:

```python
df_pct = df_cdb.assign(non_working_population_percent=((df_cdb['Non Working Population Person']/df_cdb['Total Population Person']) * 100))
```

The resulting plot was very different:
![alt text](https://github.com/adam-p/markdown-here/raw/master/src/common/images/icon48.png "Logo Title Text 2")
