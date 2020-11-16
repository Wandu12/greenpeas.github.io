---
layout: post
title:  "파이썬 난수, 날짜·시간 처리 모듈 예시 코드 모음"
summary: 파이썬 난수, 날짜·시간 처리 모듈 예시 코드
author: Wandu
date: '2020-11-16 13:58:00 +0900'
category: jekyll
thumbnail: /assets/img/posts/20201116_135714.png
---
# 파이썬 난수&날짜 및 시간 처리 모듈
## 파이썬 난수 발생 모듈 예시

```python
import random
random.randint(1,6) # 1이상 6이하 랜덤 정수 반환
random.randrange(0, 30, 2) #0이상 30이하 2씩 건너뛴 랜덤 정수 반환(ex.26)
random.choice([3,5,7,9]) #공백 아닌 시퀀스(임의의 리스트 등)에서 랜덤 반환
random.sample([3,5,7,9], 2) #공백 아닌 시퀀스에서 중복 없이 랜덤 n개를 리스트로 반환
```

## 파이썬 날짜 및 시간 관련 처리 모듈 예시

```python
import datetime
date_obj = datetime.date(2020, 11, 16) # 년 월 일 
time_obj = datetime.time(11, 26, 40) # 시 분 초
datetime_obj = datetime.datetime(2020, 11, 16, 11, 26, 40)
print(datetime_obj)	#2020-11-16 11:26:40 형식으로 출력
print('{0}/{1}/{2}'.format(set_day.year, set_day.month, set_day.day)) #2019/3/1 출력

day1 = datetime.date(2020, 7, 7)
day2 = datetime.date(2020, 11, 16) #datetime.date
diff_day = day2-day1 # 날짜도 빼기 연산 가능. datetime.timedelta로 데이터타입 변경
print(diff_day) #132 days, 0:00:00
print(diff_day.days) #132 날짜만 출력
print(datetime.date.today()) #2020-11-16 오늘날짜출력

set_dt = datetime.datetime(2020, 11, 16, 11, 51, 10)
print(set_dt)
print('날짜: {0}/{1}/{2}'.format(set_dt.year, set_dt.month, set_dt.day))
print('시각: {0}/{1}/{2}'.format(set_dt.hour, set_dt.minute, set_dt.second))
now = datetime.datetime.now() #현재시간 2020-11-16 12:01:04.652480
```

## 파이썬 날짜 및 시간 서식 맞춰 출력

```python
print("Date&Time: {:%Y-%m-%d, %H:%M:%S}".format(now)) #2020-11-16, 13:47:07
print("Date: {:%Y, %m, %d}".format(now)) #2020, 11, 16
print("Time: {:%H/%M/%S}".format(now)) # 13/47/07

set_dt = datetime.datetime(2017, 5, 24, 13, 49, 38)
print("현재 날짜 및 시각:", now)
print("차이:", set_dt - now) # -1272 days, 0:02:30.323322
```


- 출처: 최은석, <데이터 분석을 위한 철저 입문>
