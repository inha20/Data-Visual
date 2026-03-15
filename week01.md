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
print(pandas.Dataframe())<nbsp><nbsp><nbsp><nbsp>(2)
</summary>
➜ data = numpy.array([[1, 2, 3], [4, 5, 6], [7, 8, 9]])<br>
df = pandas.DataFrame(data, columns=['A', 'B', 'C'])<br>
print(df) ; //  옆으로 나열. <br>
➜ print(f"'A' 컬럼의 타입: {type(df['A'])}") ; // series 형태로 반환. df는 임시저장 series. <br>
➜ print(column_a.index), print(list(column_a.index)) ; // 시작부터 끝이 되기 전까지, 간격. <br>
➜ df.dtypes ; // int64. <br>
</details>


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

