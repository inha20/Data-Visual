# pandas prompt

> import plotly.express as px <br>
> import plotly.graph_objects as go <br>
> import pandas as dp <br>


<details><summary>
pl
</summary> 
➜ fig = px.scatter(df_gapminder, x="gdpPercap", y="lifeExp",color="continent",size="pop",hover_data=["country"],title="1인당 GDP vs 기대수명",labels={"gdpPercap": "1인당 GDP", "lifeExp": "기대수명"})<br>
➜ print(df_gapminder["continent"].unique())<br>
fig = px.scatter(df_gapminder, x="gdpPercap", y="lifeExp",color="continent",trendline="lowess",trendline_color_override="black",facet_col="continent")<br>
➜ fig = px.line(df_gapminder, x="year", y="lifeExp",color="continent",line_dash="continent",
markers=True,title="대륙별 기대수명 변화",labels={"year": "연도", "lifeExp": "기대수명"})<br>
➜fig = px.bar(df_medals_long, x="nation", y="count",color="medal",barmode="group",title="국가별 메달 수",labels={"nation": "국가", "count": "메달 수"})<br>
➜ fig = px.histogram(df_tips, x="total_bill",color="sex",nbins=30, histnorm="probability", title="성별 총 계산서 분포",labels={"total_bill": "총 계산서", "sex": "성별"})
<br>
➜ fig = px.box(df_tips, x="day", y="total_bill", color="sex", points="all", notched=True, title="요일별 총 계산서 분포", labels={"day": "요일", "total_bill": "총 계산서", "sex": "성별"})
<br>
➜ fig = px.sunburst(df_tips, path=["sex", "day", "time"],values="total_bill",title="성별 > 요일 > 시간대별 총 계산서",labels={"total_bill": "총 계산서"}) <br>
➜ fig = px.treemap(df_tips, path=["sex", "day", "time"],values="total_bill",title="성별 > 요일 > 시간대별 총 계산서",labels={"total_bill": "총 계산서"})  <br>
➜fig = px.icicle(df_tips, path=["sex", "day", "time"],values="total_bill", title="성별 > 요일 > 시간대별 총 계산서",labels={"total_bill": "총 계산서"}). <br>
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

