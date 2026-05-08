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
</details>
