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
print(pandas.Dataframe()) &nbsp&nbsp(2)
</summary>
➜ data = numpy.array([[1, 2, 3], [4, 5, 6], [7, 8, 9]])<br>
df = pandas.DataFrame(data, columns=['A', 'B', 'C'])<br>
print(df) ; //  옆으로 나열. <br>
➜ print(f"'A' 컬럼의 타입: {type(df['A'])}") ; // series 형태로 반환. df는 임시저장 series. <br>
➜ print(column_a.index), print(list(column_a.index)) ; // 시작부터 끝이 되기 전까지, 간격. <br>
➜ df.dtypes ; // int64. <br>
</details>


<details><summary>
df의 객체지향
</summary>
➜ df = pd.DataFrame(dict)<br>
print(df) ; // key가 columns. index=[]으로 지정 가능. <br>
➜ df_with_index = df.reset_index().set_index('Name') // index의 이름이 생겼다가 사라짐. <br>
➜ df_with_index ; // 문자열이 아닌 표로 보여줌. <br>
➜ df_with_index.reset_index(inplace=True) ; // 원본수정.
</details>

<details><summary>
loc, iloc
</summary>
➜ df.loc ; // 지정인덱스. 슬라이싱 끝에 포함. <br>
➜ df.iloc ; // 순서인덱스. 슬라이싱 끝에 제외. columns도 됨.<br>
➜ subset = df.loc[0:2, ['Name', 'Age']] <br>
</details>

<details><summary>
pandas 설치하기
</summary>
➜ import pandas ; // VS Code에서 <br>
➜ conda install pandas ; // prompt에서 <br>
</details>

<details><summary>
조작
</summary>
➜ b, dd ; // 생기기, 지우기. <br>
➜ y, m ; // 텍스트모드와 코딩모드. <br>
</details>

<details><summary>
마스크
</summary>
➜ 불리언인덱싱 ; // filtered_data = df[df['Age'] > 25] <br> 
</details>

<details><summary>
실습후기
</summary>
➜ 소괄호와 대괄호 주의, 문자열 표시하기. <br> 
&nbsp&nbsp&nbsp&nbsp ⤷loc와 iloc는 대괄호, series는 대괄호, 좌표는 소괄호, 마스크는 대괄호(사유 : series)
</details>

<details><summary>
sort와 결측치
</summary>
➜ sort_values(by="", na_position="first", ascending=False, ignore_index=True, inplace=True) <br> 
➜ 결측치 ; NaN, NaT <br> 
➜ sort_index
</details>

<details><summary>
CSV
</summary>
➜ Comma Seperated Values <br> 
➜ panda.read_csv("이름.csv", usecols=["",""], index_col="", na_values=["Not Available",""], nrows=3, skiprows=[4,5]) <br>
➜ set index <br> 
</details>
