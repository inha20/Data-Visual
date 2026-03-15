# pandas prompt

>touch for open these
<details><summary>print(pandas.Dataframe())
</summary>
➜ Empty DataFrame ; //  columns가 나오고 index가 나온다.<br>
➜ 리스트 문자열 ; // 0번 columns 안에 나열된다.<br>
➜ 문자열.shape ; // (index방향, columns 방향)으로 총 갯수.<br>
➜ 문자열.dtypes ; // str은 명시적, object는 묵시적.<br>
➜ 문자열.head, 문자열.tail ; // 숫자 넣을 수 있음.<br>
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

