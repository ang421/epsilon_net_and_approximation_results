# fixed_object_set_results

We have one folder each for the results from our experiments in estimating the size **m** needed for (1) **epsilon net** and (2) **epsilon approximation**.

Under each result directory, we have the following common directories:
1. **kurtosis** - We measured the **kurtosis** values for reasonsable **m** sizes to see whether the **kurtosis** is indeed _o(n)_ as desired.
2. **trials** - We observed how the **m** value changes depending on how many **trials** we used to calculate the required statistics.
3. **k** - We inspected whether the **k** value (tolerance w.r.t. how many sd's from mean) used will impact the estimated **m** value.

Meanwhile, we also plot the estimated **m** against the **epsilon (e)** values used.

For the **epsilon net** results, we plot the graphs for (1) **m vs 1/e** and (2) **m vs 1/e log 1/e**.

For the **epsilon approximation** results, we added an extra **1/e** factor and plot (1) **m vs 1/e^2** and (2) **m vs 1/e^2 log 1/e**.

Under each directory mentioned above, we experimented with the following three datasets:
1. **aol** - We used data from the [AOL Query Log](http://www.cim.mcgill.ca/~dudek/206/Logs/AOL-user-ct-collection/), where the clicked URL per query is used to generate the range space.
2. **yandex_url** - We used data from the [anonymized Yandex dataset](https://www.kaggle.com/c/yandex-personalized-web-search-challenge/overview), where the clicked URL per query is used to generate the range space.
3. **yandex_domain** - We used data from the [anonymized Yandex dataset](https://www.kaggle.com/c/yandex-personalized-web-search-challenge/overview), where the domain of the clicked URL per query is used to generate the range space.

Note that all html files are of the format **{top, random, mixed}\_{5k, 10k, 50k}.html** where **{top, random, mixed}** indicates how we chose the set of users for the range space and **{5k, 10k, 50k}** indicates how many users we selected.
1. **top** - We select the users with the most distinct websites visited.
2. **random** - We select the users randomly from all possible users.
3. **mixed** - We select the top 1/3 users, the bottom 1/3 users, and choose the other 1/3 users randomly.
