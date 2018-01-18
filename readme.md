# 신고리 5,6호기 공론화위원회 시민참여형 조사 원자료 데이터 정제

## 목표

- 데이터 정제

## 변수명, 변수, 설문문항 meta 데이터

- 데이터 출처
  - [신고리 5,6호기 공론화 위원회](http://npp.jiniworks.com/npp/join/output.do?mode=view&articleNo=9054&article.offset=0&articleLimit=10)

- 원본
  - [원본PDF](data/origin/자료이용지침서_신고리_56호기_공론화위원회.pdf)
- 변환
  - [xls](data/converted_variable.xlsx) 
  - [json](data/converted_variable.json)
  - [csv](data/converted_variable.csv)

## 1,2,3,4차 설문조사 데이터

- 데이터 출처
  - [신고리 5,6호기 공론화 위원회](http://npp.jiniworks.com/npp/join/output.do?mode=view&articleNo=9054&article.offset=0&articleLimit=10)
- 원본
  - [xlsx](data/origin/)
- 변환
  - [1,2,3,4차 데이터 통합본 csv](data/converted_rawdata_1234st_about_total_user.csv)
  - [1,2,3,4차 모두 참가한 사람들 데이터 csv](data/converted_rawdata_1234st_about_user.csv)
  - [3,4차 모두데이터 csv](data/converted_rawdata_1234st.csv)

## 변환된 데이터 읽기

- PID: 설문조사에 참여한 사람의 익명화된 ID (개인식별번호)
- var_id: 질문지 변수 (key)값
  - 1,2,3,4차 필드에 맞쳐서 보면 된다.
- episode: 몇회차 질문인지 표기
- description: 질문(변수)에 대한 설명
  - main
  - sub 
- question: 질문
  - main
  - sub
  - type: 객관식 혹은 주관식인지
    - objective, subjective
- objective_statemet: 객관식 항목

## 참고 사항

```
<수정사항> 1월 16일

건설 중단/재개에 대한 공감도(3,4차)

변수명 C_Q7_1  건설재개->건설중단
변수명 C_Q7_2  건설중단->건설재개
변수명 D_Q6_1  건설재개->건설중단
변수명 D_Q6_2  건설중단->건설재개
```

- 위 참고사항은 데이터 변환에 반영되어 있음

## 설문 변수 데이터화 작업 방식

- pdf -> txt : `notebook\exctract_from_pdf.cmd`
- txt -> xls : Powered by `Human Intelligence` and `Drink`
- xls -> json, csv : `jupyter notebook` \ `variable_xls_to_json.ipynb`


## To do

- [ ] 설문지 다시 읽어볼 겸 xls 검수해보기
- [x] xls를 json 형식으로 변경
  - csv도 만들어둠
- [ ] 기존 1,2,3,4차 데이터를 json 형식으로 변경