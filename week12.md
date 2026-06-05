# pandas prompt

> import seaborn as sns

<details><summary>
sns
</summary> 
➜ sns.get_dataset_names()    <br>  
➜ sns.load_dataset("tips")<br>
➜ plt.show(), plt.close("all"). <br>
</details>

<details><summary>
pandas
</summary> 
➜ print(df_tips["smoker"].cat.categories)     # Index(['Yes', 'No'])에서 cat은 접근자. 반면 unique는 실제 값이 있어야 포함.<br>
➜ CategoricalDtype(categories=["S", "M", "L", "XL"], ordered=True) 으로 카테고리 만들기. df["size"] = df["size"].astype(size_type)으로 사용 가능. 특이사항 : print문은 str 변환이라 아스키코드, 관련 조치 없으면 오류나.
<br>
</details>

<details><summary>
sns 그래프
</summary> 
➜ sns.histplot(data=df_tips, x="total_bill", bins=10, kde=10, hue="sex", multiple="layer", color="coral", alpha=0.8)<br>
➜ sns.scatterplot(data=df_penguins, x="bill_length_mm", y="flipper_length_mm", hue="species", style="species", size="body_mass_g", sizes=(20, 200))
<br>
➜ sns.lineplot(data=df_flights, x="year", y="passengers", hue="month", style="month", estimator="sum", palette="cool" ) <br>
➜ sns.relplot(data=df_tips, x="total_bill", y="tip", kind="scatter",  hue="day", col="sex", row="smoker")<br>
➜ sns.barplot(data=df_tips, x="day", y="tip", errorbar=("ci", 95), hue="sex", palette="Set2", estimator="sum", errorbar=None, order=["Thur", "Fri", "Sat", "Sun"], hue_order=["Male", "Female"], orient="h", width=0.9, alpha=0.7) <br>
➜ sns.countplot(data=df_titanic, x="class", hue="survived", palette="Set2", order=["First", "Second", "Third"], hue_order=[1, 0], orient="h", width=0.4)<br>
➜ sns.boxplot(data=df_penguins, x="species", y="flipper_length_mm", hue="sex", palette="Set2", flierprops={"marker": "o", "markeredgecolor": "red", "markerfacecolor": "red", "markersize": 8} )<br>
➜ sns.violinplot(data=df_penguins, x="species", y="flipper_length_mm", hue="sex", split=True, palette="Set2", inner="quart")<br>
➜ sns.stripplot(data=df_tips, x="day", y="tip", hue="sex", jitter=False, palette="Set2")<br>
➜ sns.swarmplot(data=df_tips, x="day", y="tip", hue="sex", palette="Set2", color="black", size=4, alpha=0.3)<br>
➜ sns.pointplot(data=df_flights, x="year", y="passengers", hue="month", palette="cool", markers=["o"], linestyles=["-"])<br>
➜ sns.catplot(data=df_tips, x="day", y="tip", kind="bar")<br>
➜ sns.catplot(data=df_tips, x="day", y="tip", kind="bar", col="sex", row="smoker", hue="day", palette="Set2", legend=False)<br>
➜ sns.pairplot(data=df_penguins, kind="kde", diag_kind="hist", hue="species", palette="Set2", diag_kws={"multiple": "dodge"})<br>
➜ <br>
➜ <br>
➜ <br>
➜ <br>
➜ <br>
</details>

<details><summary>
sns.pairplot
</summary> 
다변량(Multivariate) — pairplot
  
kind + diag_kind
kind: "scatter" (기본) / "kde" / "hist" / "reg"
diag_kind: "auto" (기본) / "hist" / "kde" / None

➜ sns.pairplot(data=df_penguins, kind="kde", diag_kind="hist", hue="species", diag_kws={"multiple": "dodge"})
➜ plt.show()

diag_kws는 대각선 그래프에, plot_kws는 비대각선 그래프에 추가 옵션을 전달

1. diag_kws의 키는

diag_kind="hist"일 때 → histplot 파라미터: multiple, bins, binwidth, alpha, stat
"multiple": "layer", "stack", "dodge", "fill"
bins: 5, 10, 20, 50 (정수)
binwidth: 0.5, 1.0, 2.0 (실수)
alpha: 0.0 ~ 1.0 (실수)
stat: "count", "frequency", "density", "probability"

diag_kind="kde"일 때 → kdeplot 파라미터: fill, alpha, linewidth, bw_adjust
fill: True, False
alpha: 0.0 ~ 1.0 (실수)
linewidth: 0.5, 1.0, 2.0 (실수)
bw_adjust: 0.5 (뾰족), 1.0 (기본), 2.0 (부드러움)

2. plot_kws의 키는

kind="scatter"일 때 → scatterplot 파라미터: alpha, s, edgecolor, linewidth
alpha: 0.0 ~ 1.0 (실수)
s: 10, 50, 100 (점 크기, 정수)
edgecolor: "black", "white", "none" (문자열)
linewidth: 0.5, 1.0, 2.0 (실수)

kind="kde"일 때 → kdeplot 파라미터: fill, alpha, linewidth, bw_adjust
fill: True, False
alpha: 0.0 ~ 1.0 (실수)
linewidth: 0.5, 1.0, 2.0 (실수)
bw_adjust: 0.5 (뾰족), 1.0 (기본), 2.0 (부드러움)

kind="hist"일 때 → histplot 파라미터: bins, alpha, stat
bins: 5, 10, 20, 50 (정수)
alpha: 0.0 ~ 1.0 (실수)
stat: "count", "frequency", "density", "probability"

kind="kde"의 경우 비대각 성분이 2D KDE
등고선이 촘촘할수록 → 그 영역에 데이터가 많이 몰려 있음
등고선이 넓을수록  → 데이터가 넓게 퍼져 있음

➜ sns.pairplot(data=df_penguins, vars=["bill_length_mm", "flipper_length_mm", "body_mass_g"], hue="species")
</details>

<details><summary>
sns.pairGrid
</summary> 
➜ g = sns.PairGrid(df_penguins) <br>
g.map(sns.scatterplot)<br>
plt.show()<br>
<br>
➜ g = sns.PairGrid(df_penguins)<br>
g.map_diag(sns.histplot)<br>
g.map_offdiag(sns.scatterplot)<br>
plt.show()<br>
<br>
➜ g = sns.PairGrid(df_penguins)<br>
g.map_diag(sns.histplot)<br>
g.map_upper(sns.scatterplot)<br>
g.map_lower(sns.kdeplot)<br>
plt.show()<br>
<br>
➜ g.add_legend()<br>
➜ g = sns.PairGrid(df_penguins, vars=["bill_length_mm", "flipper_length_mm", "body_mass_g"])<br>
</details>

<details><summary>
sns.FacetGrid
</summary> 
➜ g = sns.FacetGrid(df_tips, col="sex", row="smoker")<br>
g.map(sns.histplot, "tip")<br>
plt.show()<br>
<br>
➜ g = sns.FacetGrid(df_tips, col="sex", hue="smoker", palette="Set2")<br>
g.map(sns.scatterplot, "total_bill", "tip") <br>   
g.add_legend() <br>                               
plt.show()<br>
<br>
➜ g = sns.PairGrid(df_penguins)<br>
g.map_diag(sns.histplot)<br>
g.map_upper(sns.scatterplot)<br>
g.map_lower(sns.kdeplot)<br>
plt.show()<br>
<br>
➜ g.add_legend()<br>
➜ g = sns.PairGrid(df_penguins, vars=["bill_length_mm", "flipper_length_mm", "body_mass_g"])<br>
</details>

