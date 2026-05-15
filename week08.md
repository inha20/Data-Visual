# pandas prompt

> import matplotlib.pyplot as plt

<details><summary>
figure
</summary> 
➜ plt.figure() 도화지. figsize=(가로인치, 세로인치). get_size_inches. dpi=실수. get_dpi. <br> fig1.number, plt.get_fignums() : 번호부여.<br>
➜ plt.show(), plt.close("all"). <br>
</details>

<details><summary>
Axes
</summary> 
➜ plt.subplots(), fig.add_subplot(), fig.add_axes()<br>
➜ fig, axes = plt.subplots(nrows=2, ncols=2, figsize=(8, 6),
gridspec_kw={'hspace': 0.5, 'wspace': 0.3},
subplot_kw={'facecolor': 'lightgray', 'xlim': (0, 10), 'ylim': (0, 100)}  ) <br>
➜ fig, axes = plt.subplots(nrows=3, ncols=1, figsize=(4, 8), squeeze=False) <br>
➜ ax1 = fig.add_subplot(2, 3, 1)  # 2행 3열 중 1번째 <br>
➜ print(len(fig.axes))  # 6 - Figure에 추가된 Axes 수 <br>
➜ ax2 = fig.add_axes([0.1, 0.1, 0.8, 0.8], label='ax2') <br>
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
</details>
