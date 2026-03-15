

# anaconda prompt

>touch for open these
<details><summary>시작
</summary>
➜ conda ; //  실행확인 방법 중 하나.<br>
➜ cls ; // 창 깨끗이 하기.<br>
</details>
<details><summary>
개발환경 만들기
</summary>
➜ conda env list ; // 환경 리스트. <br>
➜ conda create -n 202444011 ; // 환경 만들기, 이름 붙여서. <br>
➜ conda create -n 202444011_2 python=3.12 ; //  파이썬 호환 <br>
</details>

방향키로 기존 명령어 불러오기 가능.

<details><summary>
conda active로 이동하기
</summary>
➜ conda activate 202444011_2 ; // 이동하기. <br>
➜ conda deactivate ; // 되돌아온 후 <br>
➜ conda activate 202444011 ; // 재이동 가능. <br>
</details>

<details><summary>
파이썬 커널 설치
</summary>
➜ conda activate 202444011_2 ; // 이동하기 <br>
➜ conda install ipykernel ; // 파이썬 커널 설치 <br>
</details>

<details><summary>
pandas 설치하기
</summary>
➜ import pandas ; // VS Code에서 <br>
➜ conda install pandas ; // prompt에서 <br>
</details>
