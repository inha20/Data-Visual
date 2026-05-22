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
➜ print(df_tips["smoker"].cat.categories)     # Index(['Yes', 'No'])에서 cat은 접근자.<br>
➜ CategoricalDtype(categories=["S", "M", "L", "XL"], ordered=True) 으로 카테고리 만들기. df["size"] = df["size"].astype(size_type)으로 사용 가능.
<br>
➜  <br>
➜  <br>
➜  <br>
➜  <br>
</details>

<details><summary>
Ui
</summary> 
➜ .set_facecolor('lightblue')<br>
➜ .set_edgecolor('salmon')  .set_linewidth(10)    ax.spines['top'].set_color('red') <br>
➜ .set_linewidth(3)    .set_linestyle('--')      .set_visible(False) <br>
➜ fig.savefig('figure.png')    ax.set_title('제목')    ax.set_xlabel('x축 이름') <br>
➜ plt.tight_layout()  <br>
➜ ax.tick_params(axis='x', rotation=45)<br>
</details>

<details><summary>
그래프의 종류별 그리기
</summary> 
➜ plt.tight_layout(), plt.show(). 축 정보는 ax.<br>
➜ ax.plot(top20['Overall rank'], top20['Score'], color='antiquewhite', linewidth=5, linestyle='-.', marker='s', markersize=6 ) <br>
➜  ax.plot에 label한 것은 ax.legend로 그리고 plt.show()로 볼 수 있어.<br>
➜  ax.bar(top10['Country or region'], top10['Score'], color='steelblue', edgecolor='lightblue', linewidth=10)<br>
➜  ax.scatter(df_iris['petal_length'], df_iris['petal_width'], s=80,  # 마커 크기 (markersize가 아닌 s 사용) edgecolors='black', alpha=0.7)<br>
➜  ax.hist(df_iris['sepal_length'])<br>
➜  ax.boxplot(리스트)<br>
➜  ax.boxplot(리스트)<br>
➜  ax.boxplot(리스트)<br>
➜  ax.boxplot(리스트)<br>
➜  ax.boxplot(리스트)<br>
➜  ax.boxplot(리스트)<br>
➜  ax.boxplot(리스트)<br>
➜  ax.boxplot(리스트)<br>
➜  ax.boxplot(리스트)<br>
</details>
