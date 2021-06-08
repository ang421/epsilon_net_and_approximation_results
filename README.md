# epsilon_net_and_approximation_results

We have one folder each for the results from our experiments in estimating the sizes needed for (1) **epsilon net** and (2) **epsilon approximation**.

Under each directory, we experimented with the following three datasets:
1. **aol** - We used data from the AOL Query Log, where the range space used is the clicked URL per query.
2. **yandex_url** - We used data from the [anonymized Yandex dataset](https://www.kaggle.com/c/yandex-personalized-web-search-challenge/overview), where the range space is the clicked URL per query.
3. **yandex_domain** - We used data from the [anonymized Yandex dataset](https://www.kaggle.com/c/yandex-personalized-web-search-challenge/overview), where the range space is the domain of the clicked URL per query.

Under each dataset for the results, we have the following common directories:
1. **kurtosis** - We measure the kurtosis values for reasonable m sizes to see whether the kurtosis is indeed _o(n)_ as we expected.
2. **trials** - We measure how the m value changes depending on how many trials we do per iteration for the sampled data.
3. **k** - We inspect whether the k value (tolerance w.r.t. how many sd's from the mean) used will greatly impact the m value.

Meanwhile, we also plot the calculated **m** against the **epsilon** values used.

For the **epsilon net** results, we plot the graphs for (1) **m vs 1/e** and (2) **m vs 1/e log 1/e**.

For the **epsilon approximation** results, we added an extra **1/e** factor and plot (1) **m vs 1/e^2** and (2) **m vs 1/e^2 log 1/e**.

Note that all html files are of the format **{top, random, mixed}\_{5k, 10k, 50k}.html** where **{top, random, mixed}** indicates how we chose the set of users and **{5k, 10k, 50k}** indicates how many users we selected.
1. **top** - We select the users with the most distinct websites visited.
2. **random** - We select the users randomly.
3. **mixed** - We select the top 1/3 users, the bottom 1/3 users, and choose the other 1/3 users randomly.
