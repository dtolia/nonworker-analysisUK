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

The graph above shows **Gangolihat** as the hub of non-workers, totaling approximately thirty-eight thousand people! But it is also true that Gangolihat is more densely populated than other blocks in the district. So, as a workaround, I calculated the *non-worker percentage against the total population* for each development block through:

```python
df_pct = df_cdb.assign(non_working_population_percent=((df_cdb['Non Working Population Person']/df_cdb['Total Population Person']) * 100))
```

The resulting plot was very different:

![alt text](https://github.com/dtolia/nonworker-analysisUK/blob/main/charts/1_Pithoragarh.png "Correct Plot for District Pithoragarh")

Gangolihat is no longer at the top, replaced by **Berinag**. While an obscure **Kanali Chhina** has come to the forefront. 
And friends, this is how data can be misinterpreted to transfer funds to the wrong places. Incorrect policies could also be implemented as a result.


## 2. Observation -I
---

![alt text](https://github.com/dtolia/nonworker-analysisUK/blob/main/charts/8_Chamoli.png "Plot for District Chamoli")

The chart above has two parts: 
* Horizontal Bar Graph that compares the non-worker percentage in each development block; 
* Vertical Bar Graph that compares the Men-Women ratio among non-workers in the top three non-worker-dominated development blocks.

Therefore, in the Chamoli district, we must provide aid in order of Karnaprayag -> Narayan Bagar -> Dasholi development blocks. This would ensure that the most needful get the help first. 
Also, notice that most non-workers are women in each of these development blocks. This is a trend that repeats in almost every district as can be seen by clicking the tab below.

<details><summary>See All Charts</summary>
<p>

![alt text](https://github.com/dtolia/nonworker-analysisUK/blob/main/charts/2_Bageshwar.png "Plot for District Bageshwar")

![alt text](https://github.com/dtolia/nonworker-analysisUK/blob/main/charts/3_Almora.png "Plot for District Almora")

![alt text](https://github.com/dtolia/nonworker-analysisUK/blob/main/charts/4_Champawat.png "Plot for District Champawat")

![alt text](https://github.com/dtolia/nonworker-analysisUK/blob/main/charts/5_Nainital.png "Plot for District Nainital")

![alt text](https://github.com/dtolia/nonworker-analysisUK/blob/main/charts/6_UdhamSinghNagar.png "Plot for District Udham Singh Nagar")

![alt text](https://github.com/dtolia/nonworker-analysisUK/blob/main/charts/7_Uttarkashi.png "Plot for District Uttarkashi")

![alt text](https://github.com/dtolia/nonworker-analysisUK/blob/main/charts/9_Tehri.png "Plot for District Tehri")

![alt text](https://github.com/dtolia/nonworker-analysisUK/blob/main/charts/10_Rudraprayag.png "Plot for District Rudraprayag")

![alt text](https://github.com/dtolia/nonworker-analysisUK/blob/main/charts/11_Dehradun.png "Plot for District Dehradun")

![alt text](https://github.com/dtolia/nonworker-analysisUK/blob/main/charts/12_Pauri.png "Plot for District Pauri")

![alt text](https://github.com/dtolia/nonworker-analysisUK/blob/main/charts/13_Haridwar.png "Plot for District Haridwar")

</p>
</details>

Hence, any policy we implement must be women-centric to provide equal relief to all non-workers in these districts.


## 3. Observation -II
Compare the following two graphs from Kumaon Division:

![alt text](https://github.com/dtolia/nonworker-analysisUK/blob/main/charts/1_Pithoragarh.png "Plot for District Pithoragarh")
![alt text](https://github.com/dtolia/nonworker-analysisUK/blob/main/charts/6_UdhamSinghNagar.png "Plot for District Udham Singh Nagar")

You may observe a sharp men/women disparity among non-workers in the top three non-worker-dominated development blocks. But when comparing the Himalayan districts (like Pithoragarh) of Uttarakhand with those that have parts of the northern plains in them (like Udham Singh Nagar), we come across a unique observation:

"The non-working women in districts with parts of the northern plains in them are twice in number than non-working men. Himalayan districts fare better comparatively."

A similar observation can be made for Garhwal Division as well:

![alt text](https://github.com/dtolia/nonworker-analysisUK/blob/main/charts/7_Uttarkashi.png "Plot for District Uttarkashi")
![alt text](https://github.com/dtolia/nonworker-analysisUK/blob/main/charts/13_Haridwar.png "Plot for District Haridwar")

Thus, we have a relationship but what can be the cause?! Is it the difference in ethnic culture? The result of exclusionary and unequal urbanization? Or could it be something that we’re completely missing out on!?! 
This shall be determined as we thoroughly analyze relevant data in this regard.

---