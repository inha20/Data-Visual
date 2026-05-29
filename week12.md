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
➜ <br>
➜ <br>
➜ <br>
</details>

