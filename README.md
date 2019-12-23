# MULTICAMPUS-2nd-project

**잇슈왓슈(IssutWhatShow) - 한 눈에 보는 대한민국 핫이슈** (`spring`, `python`, `morphology`, `word2vec`, `tf-idf`, `three.js`, `aws`)

:link: [배포 URL: http://issuewhatshow.com](http://issuewhatshow.com)

:link:[발표 자료](doc/최종%20제출%20자료/%5B라떼는말이야%5D잇슈왓슈_PPT.pdf)

목차...TBD

## 개요

**현재** 대한민국에서 일어나고 있는 **일**(핫이슈)들을 짧은 시간에 파악할 수 있도록, 이슈 키워드들을 **중요도**(크기)와 **맥락**(주변 키워드) 그리고 **연관성**(링크 및 링크 거리)을 포함하여 **3D**로 시각화하여 보여주는 `Web Application`.

**웹** 서비스는 `Spring MVC`로 구축하였으며 **수집/전처리/분석** 모듈은 `python` 코드로 짜여져있다. 

### 웹서비스 실행 화면

![image-20191107183922771](.assets/image-20191107183922771.png)

### 소스 구성

#### **웹 서비스** - Web

- `Spring MVC`
- `Oracle RDBMS`(교육용 xe)
- `three.js` 기반 `3d-force-graph` 시각화 라이브러리

#### 수집/전처리기 - Crawllica

`crawllica`: 자체 개발 수집/전처리 최상위 `python` 모듈

- `harvesta`: 웹 문서 수집기
  - NAVER 관련 모듈
  - DAUM 관련 모듈
  - Google 관련 모듈
  - Twitter 관련 모듈
- `preproca`: 웹 문서 전처리기
  - whitelist 처리 코드
  - blacklist 처리 코드
  - 정규표현식 기반 불용문자 제거기

#### 분석기 - Analyza2

`analyza`: 자체 개발 NLP 분석기 최상위 `python` 모듈

- `morpheus`: khaiii 형태소 분석기를 이용한 형태소 분석 driver  모듈
- `word2veca`: gensim package의 word2vec driver 모듈
- `tfidf`: tfdif 계산 모듈

### 기존 이슈 파악 방법과의 차별성

#### 실시간 키워드 확인의 한계

포털 사이트의 실시간 검색어 트렌드는, 개별적인 키워드의 우선순위는 확인 할 수 있으나 따로 분류 되어 있는 동일한 사건에 대한 키워드 간의 연관관계를 파악할 수 없고, 또한 실제로 무슨 내용인지에 대한 맥락이 빠져있어서 단순 트렌드 키워드를 파악 외에는 특별히 알 수 있는 정보가 없다.

![image-20191107190054310](.assets/image-20191107190054310.png)

#### 실시간 트렌트 파악의 한계

기존의 실시간 트렌드 서비스는 관련 키워드 간의 1-depth 연관관계에 대한 정보를 알 수는 있으나 메인 키워드를 빼고는 키워드의 중요도 정보를 파악할 수 있는 scalar 정보가 제공되지 않는다. 또한 정작 해당 키워드가 순위권에 올라와 있어도 현재 이슈가 되고 있는 뉴스를 보는 섹션에는, 해당 키워드와는 무관한 단순 트렌드 순위 상위권의 뉴스들을 보여주고 있다. 따라서 해당 이슈의 맥락 파악에도 한계가 있고 자세한 내용으로 이어지는 연결 서비스에도 한계가 있다.

![image-20191107190156052](.assets/image-20191107190156052.png)

## 사용 기술

- Spring Framework
- Web scraping
- Data preprocessing
- Morphology
- Word2Vec
- TF-IDF
- DBMS(Oracle)
- AWS

## 잇슈왓슈의 기능

- 이슈 키워드 3D 시각화
  - TBD
- TBD

## 구현 된 UI 및 기능 소개



## 결과 및 수상 내역

