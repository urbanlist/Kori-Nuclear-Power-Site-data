# 신고리 5,6호기 공론화위원회 시민참여형 조사 원자료 데이터 만들기

## 변수명, 변수, 설문문항 데이터화

- 원본
  - [원본자료 Url](http://npp.jiniworks.com/npp/join/output.do?mode=view&articleNo=9054&article.offset=0&articleLimit=10)
  - [github에 백업한 원본자료](data/origin/)
- 변환
  - [데이터화한 xls](data/converted_variable.xlsx) 
  - [json](data/converted_variable.json)
  - [csv](data/converted_variable.csv)

### 참고 사항

```
<수정사항> 1월 16일

건설 중단/재개에 대한 공감도(3,4차)

변수명 C_Q7_1  건설재개->건설중단
변수명 C_Q7_2  건설중단->건설재개
변수명 D_Q6_1  건설재개->건설중단
변수명 D_Q6_2  건설중단->건설재개
```

- 위 참고사항은 반영되어 있음

## 변수 데이터화 작업 방식

- pdf -> txt 는 Computer
- txt -> xls 는 Powered by `Human Intelligence` and `Drink`


## 차후 목표

- [ ] 설문지 다시 읽어볼 겸 xls 검수해보기
- [x] xls를 json 형식으로 변경
  - csv도 만들어둠
- [ ] 기존 1,2,3,4차 데이터를 json 형식으로 변경
- [ ] 어떻게 시각화해서 볼지 고민이란걸 해본다.
  - 아무 생각이 안나니까 일단 전체 다 볼 수 있는걸 만들어본다거나...