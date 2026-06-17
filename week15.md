# pandas prompt

> import plotly.express as px <br>
> import plotly.graph_objects as go <br>
> import pandas as dp <br>


<details><summary>
두 객체의 문자열간 변환
</summary> 
➜ fig = px.scatter(df_gapminder, x="gdpPercap", y="lifeExp",color="continent",size="pop" , hover_data=["country"])<br>
➜ <br>
) <br>
➜ <br>
➜ idx = pd.date_range('2024-01-01', periods=12, freq='QE')<br>
➜ pd.Timedelta, print(td.days), print(td.seconds), print(td.total_seconds()) <br>
➜ Timestamp + Timedelta = Timestamp, Timestamp - Timestamp = Timedelta의 편의기능 제공. <br>
➜ Timestamp와 Timedelta 모두 대소비교 기능 제공.
</details>

<details><summary>
두 객체의 문자열간 변환
</summary> 
# -----------------------datetime---------------------Timestamp<br>
# 문자열 → 객체-------datetime.strptime()----------pd.to_datetime()<br>
# 객체 → 문자열-------dt.strftime()----------------ts.strftime()<br>
➜ pd.to_datetime('2024년 06월 04일', format='%Y년 %m월 %d일')<br>
➜ idx = pd.DatetimeIndex(['2024-01-01', '2024-06-04', '2024-12-31'])
print(idx)<br>
print(idx.year) <br>
➜ print(idx.dayofweek), print(idx.day_name()), print(idx.quarter)<br>
➜ idx = pd.date_range('2024-01-01', periods=12, freq='QE')<br>
➜ pd.Timedelta, print(td.days), print(td.seconds), print(td.total_seconds()) <br>
➜ Timestamp + Timedelta = Timestamp, Timestamp - Timestamp = Timedelta의 편의기능 제공. <br>
➜ Timestamp와 Timedelta 모두 대소비교 기능 제공.
</details>

<details><summary>
두 객체의 문자열간 변환
</summary> 
# -----------------------datetime---------------------Timestamp<br>
# 문자열 → 객체-------datetime.strptime()----------pd.to_datetime()<br>
# 객체 → 문자열-------dt.strftime()----------------ts.strftime()<br>
➜ pd.to_datetime('2024년 06월 04일', format='%Y년 %m월 %d일')<br>
➜ idx = pd.DatetimeIndex(['2024-01-01', '2024-06-04', '2024-12-31'])
print(idx)<br>
print(idx.year) <br>
➜ print(idx.dayofweek), print(idx.day_name()), print(idx.quarter)<br>
➜ idx = pd.date_range('2024-01-01', periods=12, freq='QE')<br>
➜ pd.Timedelta, print(td.days), print(td.seconds), print(td.total_seconds()) <br>
➜ Timestamp + Timedelta = Timestamp, Timestamp - Timestamp = Timedelta의 편의기능 제공. <br>
➜ Timestamp와 Timedelta 모두 대소비교 기능 제공.
</details>

