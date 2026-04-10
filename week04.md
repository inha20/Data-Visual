# pandas prompt

>축과 결측치
<details><summary>실수형 결측치와 다른 결측치
</summary>
➜ numpy의 Series는 원래 길쭉해서 위에서 아래로 반환하며 Series를 반환.<br>
➜ np.nan은 Not A Number라 float형.<br>
➜ 판다 시리즈 밖에서 None을 넣을때 시리즈에 배열 인덱스를 쓸 수 있어. [].<br>
➜ s.dropna()로 결측치 날리기. 다만 inplace true는 별도로. (how="all", 기본값 "any"). (thresh=2는 2개 이상이 남을때만 유지). (subset=[""]은 특정 컬럼을 기준으로). (axis=1으로 1번 축인 열 기준으로 제거할 수 있어). <br>
➜ numpy의 소수세계 말고, panda의 Not A _ 이랑 Not A Time이 있음. <br>
➜ numpy의 소수세계 밖 panda에서도 정수의 실수 통일은 일어남. <br>
➜ 정수로 강제로 넣기 위해 dtype="int64" 사용. 정수묶기만 하면 기본값인 실수로 처리됨.
<br>
➜ s.fillna()로 결측치를 채울 수 있음. <br>
</details>



<details><summary>축(axis= )과 결측치를 제외하는 연산 메소드
</summary>
➜ sum<br>
➜ count<br>
➜ mean은 평균<br>
➜ min<br>
➜ max<br>
</details>





<details><summary>multi index
</summary>
➜ pop[[i for i in pop.index if i[1]==2000]] ; //  boolean Series로 인덱싱.<br>
➜ [x**2 for x in range(10)] ; // in의 구간에서 하나하나 for문 안으로 꺼내어 맨 앞에 대입.<br>
 &nbsp&nbsp&nbsp&nbsp&nbsp&nbsp [w.upper() for w in words] <br>
 &nbsp&nbsp&nbsp&nbsp&nbsp&nbsp [f for f in fruits if 'a' in f] <br>
  &nbsp&nbsp&nbsp&nbsp&nbsp&nbsp ['Even' if x % 2 == 0 else 'Odd' for x in numbers]<br>
   &nbsp&nbsp&nbsp&nbsp&nbsp&nbsp [num for row in matrix for num in row]<br>
   &nbsp&nbsp&nbsp&nbsp&nbsp&nbsp {x: x**2 for x in range(5)}<br>
➜ panda.MultiIndex.from_tuples(index) ; // list type, MultiIndex type. ; // 멀티인덱스 각각에 names 줄 수 있어.<br>
➜ from_product, from_arrays, from_frame ; // 조작) ctrl shift -로 셀 분리 <br>
➜ reindex <br>
➜ df.index.names = ["",""] <br>
</details>





<details><summary>multy index와 Series
</summary>
➜ np.array(data_x), arr.reshape(4,6) ; // <br>
➜ health_data.loc[2014, ('Bob','HR')] ; // 튜플은 계층을 표현.<br>
</details>






<details><summary>merge()와 join()으로 join하기
</summary>
➜ 항목의 이름이 같으면 붙임. <br>
➜ one to one join 은 공통칼럼이 앞으로이지만 아름 다르면 두 번 출력, many to one은 이어져서.<br>
➜ 문자열.shape ; // (index방향, columns 방향)으로 총 갯수.<br>
➜ 문자열.dtypes ; // str은 명시적, object는 묵시적.<br>
➜ 문자열.head, 문자열.tail ; // 숫자 넣을 수 있음.<br>
</details>


