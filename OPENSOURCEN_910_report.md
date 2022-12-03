## 오픈소스 소프트웨어 (N)_ 910조_ Mood Station

- 1692110 백승호
- 1771365 박호제
- 1771383 양정우
- 1871367 심수민
- 2171328 양서진
- 2171454 심혜진
- 2171312 오윤지

## 목차

#### Mood Station 소개

- 서비스의 선정 배경 그리고 목적과 정의

- 서비스의 기능

- 서비스를 통해 기대되는 효과

#### 유사 서비스 분석

- 지니뮤직 - 뮤직컬러_세밀하게 분석한 고객의 음악감상이력에 새로운 컬러매칭 AI 큐레이션 기술을 적용

- 멜론 - 뮤직DNA_나의 감상 이력 데이터를 기반으로 여러 가지 통계를 볼 수 있는 개인화 서비스

- 플로 - 내 취향 MIX_곡 차트에서 AI분석을 통해 노래를 추천하는 서비스

- Mood Station과 타 플랫폼과의 차이점
 
#### 사용 오픈소스 소프트웨어

- Django, Elasticesearch을 사용한 검색 엔진
- Musixmatch Developer
- FireBase
- Text Analytics API
- KoNLPy 자연어 처리 라이브러리
- NLTK 불용어 제거 라이브러리
- sklearn

#### DFD

- 최종 DFD
- DFD 설명

#### 시스템 설계 요약

- 사용자 시나리오와 관리자 시나리오
- 사용자 시나리오
- 관리자 시나리오
- 설계 요약

## Mood Station 소개

#### 서비스의 선정 배경 그리고 목적과 정의

지난 2년은 코로나19 펜데믹으로 정치, 사회, 경제 및 문화 전반에 걸쳐 많은 변화를 가지고 온 해였다. 그 영향으로 과거 장기간에 걸쳐 필요했던 변화가 단기간에 이뤄졌다고 할 수 있는데, 그 중심에는 ‘개인화’가 있다. 이제 우리는 개인화를 넘어, 초개인화의 시대에 접어들었다.

소비자는 개개인에 맞는 맞춤형 서비스를 빠르고 편리하게 사용하길 원하는데, 이는 우리가 흔히 알고 있는 ‘넷플릭스’나 ‘유튜브’의 개인 맞춤형 서비스는 물론, 금융이나 헬스, 관광, 패션 등 다양한 분야에서도 기업이 개인화 전략을 내세워 마케팅을 하고 있다. 우리는 그 다양한 장르 중에서도 ‘음악’이라는 장르에 초점을 맞춘다.

우리가 소개할 서비스의 이름은 ‘Mood Station’다. 이는 노래를 장르나 아티스트는 물론이고, 음악이나 가사에서 연출되는 다양한 분위기마저 세밀하게 분류하여 사용자에게 추천 및 제공하는 서비스다. 유사한 기존 서비스들의 장점을 흡수하면서도 ‘Mood Station’만의 차별성을 제공한다.

#### 서비스의 기능

노래의 제목, 아티스트, 장르 등의 정보와, ‘KoNLPy 자연어 처리 라이브러리’와 ‘NLTK 불용어 제거 라이브러리’를 통해 분류된 여러 분위기 태그들을 포함한 다양한 노래의 정보들을 ‘FireBase’ DB에 저장한다.

이 정보들은 ‘ElasticeSearch’를 이용한 검색엔진과 ‘Musixmatch Developer’기능을 통해 음악을 다양한 정보와 함께 사용자에게 접근한다. 

그리고 ‘TextAnalyticsAPI’와 ‘sklearn’ 기계 학습 라이브러리를 통해 사용자에게 유사한 곡들을 추천하는데, 이는 국내의 ‘지니뮤직’이나 ‘플로’, 해외의 ‘스포티파이’의 다양한 태그 및 추천 서비스와 유사하다.

지금 까지가 유사 서비스의 장점을 갖고 온 것이었다면, ‘Mood Station’의 차별화된 서비스로 번역기능을 제공한다.

우리는 ‘NLLB-200’ 이라는 오픈소스를 통해 노래번역 기능을 제공하는데, 이는 페이스북 운영사 메타(Meta)가 올해 7월에 공개한 오픈소스 기술이다. 이를 통해 200여개의 다른 언어를 번역하여 더 발전되고 차별화된 결과를 제공한다.

#### 서비스를 통해 기대되는 효과

우리 모두는 각자의 개성과 취향이 있다. ‘Mood Station’은 감성을 자극하는 ‘음악’을 개인에게 맞춤형 서비스로 제공한다.

다양한 분위기나 상황에 맞는 곡을 빠르게 검색할 수 있고, 개인의 취향에 맞는 곡을 맞춤형으로 계속해서 추천한다.

이와 유사한 서비스는 이미 여럿 있으나 Mood Station은 그들과 차별점을 만들어 간다.

다양한 언어의 제공과 번역 기능은 수많은 국가와 인종의 사용자들이 ‘Mood Station’ 내에서 음악으로 하나되고 소통할 수 있는, 음악의 문화 소통 가능성을 열어준다.

## 유사 서비스 분석

#### 지니뮤직 - 뮤직컬러_세밀하게 분석한 고객의 음악감상이력에 새로운 컬러매칭 AI 큐레이션 기술을 적용

- 뮤직컬러는 음악의 매력을 색채의 매력으로 표현한 서비스다.

- 음악을 다양한 색상에 연결해 자신만의 뮤직컬러 정체성을 부여하는 신개념 컬러 큐레이션이다.

- 지니뮤직은 컬러와 노래를 매칭한 뮤직컬러 서비스를 운영한다.

- 뮤직컬러는 사용자의 노래 감상 취향을 장르, 분위기, 감정 등 요소로 세밀하게 분석하여 음악 성향을 (8가지의 메인 컬러를 중심으로 한 341가지의) 컬러로 표현한다.

- 뮤직컬러는 사용자가 어떤 노래를 감상하느냐에 따라 계속 변하며, 사용자마다 표현된 컬러에 해당하는 음악을 추천해준다. 

- 추천된 노래는 나만의 뮤직 캘린더에 기록되어 자신의 음악 감성이 어떻게 변하는지 확인할 수 있다.

- 자신의 음악적 취향을 공유함으로써 재미적 요소를 더한 차별성이 있다.

- 기존 큐레이션 기능은 추천음악을 단순히 나열하는 데 그쳤다면 뮤직컬러는 사용자의 음악 취향 정체성을 색상으로 표현하고 공유하면서 드러내는 요소 덕분에 사용자들이 추천 받은 음악을 실제로 듣는 경험까지 이어질 수 있도록 유도하는 데 성공했다.

#### 멜론 - 뮤직DNA_나의 감상 이력 데이터를 기반으로 여러 가지 통계를 볼 수 있는 개인화 서비스

- 뮤직DNA는 자신의 감상 이력을 통해 각 기간별 음악 청취 패턴을 분석하여 선호하는 장르, 아티스트, 작곡가, 소속사를 알려주고 어떤 음악을 어떤 시기에 얼마나 들었는지 분석하여 사용자의 뮤직 DNA를 보여준다. 이를 통해 새로운 음악이나 아티스트를 발견할 수 있다.

#### 플로 - 내 취향 MIX_곡 차트에서 AI분석을 통해 노래를 추천하는 서비스

- 내 취향 MIX를 차트 리스트에서 활성화하면, 사용자의 취향에 맞는 순서로 노래가 재조정된다.

- 사용자의 취향인 노래를 AI가 분석하여 정렬하기 때문에 사용자가 원하는 노래를 쉽게 찾아서 들을 수 있는 장점이 있다.

- 또한 '점프(JUMP)'를 통해 사용자가 마음에 든 곡과 유사한 곡을 추천해주는 기능도 있다.

- 취향에 맞지 않는 곡이 추천된다면, '이곡 안 듣기' 버튼을 눌러 해당 곡을 AI가 더 이상 추천하지 않으며 플레이리스트나 차트에서도 자동으로 제외할 수 있다.

#### Mood Station과 타 플랫폼과의 차이점

- 앞서 얘기한 타 음악 재생 플랫폼과 Mood Station을 비교해본다면 Mood Station은 가사의 자연어 처리를 통해 좀 더 직관적인 필터링이 가능하다는 점과 가사를 여러 언어로 번역 지원한다는 점에서 타 플랫폼의 재미적인 요소를 흡수, 가미한다면 상용화까지도 가능할 것이다.

## 사용된 오픈소스 소프트웨어 소개  

## Django, Elasticesearch을 사용한 검색 엔진

#### 기능

- Django를 이용한 서버 구성
- Elasticesearch와 연동하여 음악 검색 기능 구성

#### 장점

- Lucene의 강력하고 풍부한 기능의 대부분을 지원
- 기존 DBMS에서는 어려운 전문 검색, 문서의 점수화를 이용한 정렬, 실시간 검색이 가능
- RESTful API를 지원하여 URL을 사용한 동작이 가능
- 필요한 기능에 대한 플러그인으로 기능 확장 가능

#### 구현 방식

- Django 서버 구성
- Python ES API, ES 형태소 분석기 설치
- 인덱스 설정 및 생성
- 데이터 삽입
- view 구현
- url 설정
- 검색 결과 확인

#### 라이센스

- SSPL
- Elastic

## Musixmatch Developer

#### 기능

- 가사가 필요한 노래의 가사를 제공

#### 장점

- 62개 언어를 지원
- 사용자가 노래 가사를 직접 등록 가능
- 다른 사용자가 등록한 가사를 수정 가능

#### 사용 방식

- API 키 등록

- API 호출 및 응답 에 대한 세부 정보 확인

- musixmatch 서비스를 웹 사이트, 애플리케이션과 통합

- 2가지 API 호출을 구현

	- 검색 기능을 사용하여 카탈로그와 일치시키는 호출

	- 가사를 가져오는 호출

#### 라이센스

- EULA

## FireBase

#### 기능

- 검색을 통해 가져온 노래의 앨범 정보, 가수, 제목과 같은 노래 정보와 전처리된 데이터들을 NoSQL 방식으로 저장

#### 장점

- 노래 가사와 전처리된 데이터들을 저장할 수 있는 DB
- 일정 사용량까지 무료
- 구글 아이디로 가입이 가능한 접근 용이성
- Realtime Database

#### 라이센스

- Apache 2.0

## Text Analytics API

#### 기능

- 정서 분석
	- 노래 가사에서 긍정적 또는 부정적 감정에 대한 단서를 찾아서 사용자가 원하는 분위기에 맞는 노래를 추천 및 제공
	- 문장 수준에서 서비스가 찾은 높은 신뢰도 점수에 따라 부정, 중립, 긍정과 같은 감정 레이블을 제공
	- 부정, 중립, 긍정 감정에 대한 각 문서 및 그 안의 문장을 0과 1 사이의 신뢰도 점수로 반환
- 핵심 문구 추출
	- 텍스트의 주요 개념을 빠르게 식별
	- 노래 가사의 일부 문장에서 핵심 문구를 추출하여 사용자가 원하는 분위기나 느낌에 맞는 가사가 포함된 노래를 제공
	- 예시 
		- "음식이 맛있었고 훌륭한 직원이 있었습니다"
		- "음식", "훌륭한 직원"
- 언어 검색
	- 검색한 단어(텍스트)가 작성된 언어를 감지하고 광범위한 언어나 변형, 방언 및 일부 지역/문화 언어로 요청 시 제출된 모든 문서에 대해 단일 언어 코드를 보고
- 명명된 엔터티 인식
	-  사람, 장소, 조직, 수량으로 텍스트의 엔터티를 식별하고 분류할 수 있으므로 노래 가사의 엔터티를 식별하고 분석

#### 라이센스

- MIT 

## KoNLPy 자연어 처리 라이브러리

#### 기능

- 노래를 태그로 분류하기 위해 가사의 자연어 처리
- 다양한 형태소 분석기 중 성능이 좋은 편으로 알려진 Otk 형태소 분석기를 사용

#### 형태소란

- 의미를 가지는 가장 작은 단위


#### 사용 방식

- Okt에서 제공되는 함수를 통해 텍스트를 형태소 단위로 분류하여 품사 태깅(tagging)을 통해 명사와 형용사, 동사를 구분
- okt.pos()를 이용하여 형태소 단위로 나누어 그에 해당하는 품사와 함께 리스트화
- 예시

		text = “하지만 미안해 네 넓은 가슴에 묻혀 다른 누구를 생각했었어” 
        print(okt.pos(text, join = true))
        
        [‘하지만/Verb’, ‘네/Pronoun’, ‘넓다/Adjective’, ‘가슴/Noun’, ‘에/Josa’, 
        ‘묻히다/Verb’, ‘다른/Detective’, ‘누구/Pronoun’, ‘를/Josa’, ‘생각하다/Verb’]         

#### 라이센스

- GPL v3

#### 라이센스 충돌 회피

- 개정된 GPL 3.0은 특허보복조항을 포함시키는 한편 추가제한금지 규정을 보다 탄력적으로 규정함으로 Apache 2.0과 양립할 수 있게 되었다.
- Apache 2.0 과 GPL 3.0, BSD와 GPL 3.0은 네트워크 사용과 관련된 조항에서 충돌이 예상된다.
- MariaDB와 Kafka가 파이프와 소켓, 명령행 인자 등으로 통신한다면 MariaDB와 Kafka는 서로 라이선스 영향을 주지 않는다.

## NLTK 불용어 제거 라이브러리

#### 기능

- 자연어 처리된 데이터의 불필요한 불용어 제거
- 일반적으로 사용되는 한국어 불용어 리스트  
<https://www.ranks.nl/stopwords/korean>

#### 불용어란

- 분석에 큰 의미가 없고 문맥적으로 큰 의미가 없는 단어


#### 사용 방식

- 한국어의 경우 불용어 리스트를 받아와 제거
- 영어의 경우 nltk 라이브러리에 존재하는 리스트를 받아와 제거
- 예시
	
        ['Family', 'is', 'not', 'an', 'important', 'thing', '.', 'It', "'s", 'everything', '.']
        
 		['Family', 'important', 'thing', '.', 'It', "'s", 'everything', '.']

#### 라이센스

- Apache License Version 2.0.

## sklearn

#### 기능

- 추출한 키워드를 데이터 세트에서 가져온 키워드 데이터와 비교하여 유사도가 높은 곡을 출력

#### 사용 방식

- 데이터 세트에서 가져온 키워드 데이터를 벡터화
- 벡터화 한 데이터들의 코사인 유사도를 생성
- 코사인 유사도가 높은 순으로 곡들을 추천
- 예시
		
        Santa Tell Me (Ariana Grande)
        
        1. Santa Tell Me의 가사에서 자주 사용되는 단어들을 추출
   			`'Santa', 'love', 'next year', etc.`
		2. 벡터화, 코사인 유사도 생성 과정은 생략
		3. 코사인 유사도가 높은(사용 단어가 비슷한) 곡들을 나열
  			`'Santa, Can't You Hear Me','Oh Santa!', etc.`

#### 라이센스

- BSD

## DFD

#### 최종 DFD

![시스템 설계서_DFD](https://user-images.githubusercontent.com/90822147/205430270-2dd80757-628f-4ed0-808f-5cbc0f891516.png)

#### DFD 설명

- 먼저 파이어베이스 DB에 인풋되는 데이터들을 살펴보면 가장 중요한 가사데이터와 노래데이터가 들어오며 관리자에 의해 노래들에 분위기 태깅과정이 이루어진다.
- 파이어베이스의 가사데이터는 코엔엘파이, NLTK, 텍스트 어날리틱스 순서대로 전처리, 자연어처리, 불용어제거, 핵심문구 추출의 과정이 시행되며 최종적으로는 가사 데이터를 통해 json 파일로 추출된 핵심 문구들이 파이어베이스에 저장된다.
- 사용자들이 노래를 재생하면 재생할수록 협업 필터링을 통해 유사한 주제와 분위기의 노래를 추천해주는 사이클이 계속된다.

## 시스템 설계 요약

#### 사용자 시나리오와 관리자 시나리오

![시스템 시나리오](https://user-images.githubusercontent.com/90822147/205430450-9ffed7be-34e7-4f59-bbc8-bfe1a58b88c4.png)

#### 사용자 시나리오

- 사용자 시나리오로는 최초 회원가입 후 로그인 시 관심 주제, 분위기를 선택한다. 이는 관리자가 설정한 태그와 연관되어 최초에 아무런 정보 없이 추천이 가능하게끔 한다.

- 음악 재생 기록이 남겨지면서 지속적으로 주제별/분위기별 음악추천이 가능하다.

#### 관리자 시나리오

- 파이어베이스 DB를 보면 기본적으로 사용자의 로그인 필요한 ID, PW와 노래, 가사 데이터, json형태의 핵심 문구 추출 데이터가 있고 관리자는 핵심 문구 추출 데이터를 분위기 및 주제 태그로서 활용할 수 있도록 태그를 직접 파이어베이스에 만들 필요가 있다.

- 음악의 트렌드에 따라 태그의 주기적인 최신화 작업이 이루어 져야하며 협업필터링의 경우에는 사용자에게 적절한 노래가 추천이 되는지 추천 알고리즘의 성능을 충분히 검토할 필요가 있다.

#### 설계 요약

- Mood Station은 노래 가사를 분석하여 사용자가 원하는 분위기에 맞는 노래를 추천 및 제공하는 시스템이다.

- 먼저 Text Analytics API의 여러 기능을 통해 사용자의 음악 재생 목록을 분석한다.

- Text Analytics API의 감정 분석 기능을 활용하여 노래 가사에서 긍정적 또는 부정적 감정에 대한 단서를 찾거나, 핵심 문구 추출을 사용하여 텍스트의 주요 개념을 빠르게 식별합니다. 또, 노래 가사의 엔터티를 식별하고 분석한다. 

- 사용자의 음악 재생 목록 분석이 끝나면 파이어베이스(Firebase)를 데이터베이스로 사용함으로써 노래에 대한 제목부터 그 노래의 분위기에 맞는 태그, 노래의 장르, 노래의 가사 등과 같이 상황에 맞는 노래 데이터를 저장한다. 

- 파이어베이스를 선택한 이유는 일정 사용량까지 무료로 제공되는 서비스이며 구글 ID를 사용하면 바로 가입할 수 있어 접근성이 굉장히 용이하기 때문이다.

- 또 규칙이 간단하여 사용하기 쉬운 점을 고려하면 제일 적절한 DBMS이다. 

- 파이어베이스를 이용하는 방법은 Realtime Database보다 관리가 쉬운 NoSQL 방식으로 저장한다. 즉, 앞서 수집한 음악들을 바탕으로 하여 각각 아티스트 이름, 타이틀 제목, 노래 가사, 트랙 제목 등등 음악 정보와 관련된 데이터들을 저장하게 됩니다. 이렇게 저장된 데이터들을 바탕으로 해서 파이썬의 텍스트 마이닝 기법을 사용해 우리가 원하는 서비스를 구성하기 위해 필요한 키워드들(장르, 분위기 태그 등)을 추출해낸다.

- 추출된 데이터들은 기존에 저장했던 노래의 테이블과는 분리하여 Realtime Database로 저장해 분위기에 맞는 노래를 추천할 데이터로써 사용된다.

- Realtime Database를 사용하는 이유는 음악 수집 API를 통해 수집한 음악 정보와는 달리 저장해야 하는 키워드들이 몇 개 되지 않아 관리가 용이하고 나중에 데이터가 추가되는 일이 있다고 하더라도 기존에 비해 추가되는 양이 그리 크지 않은 데이터이기 때문이다.

- 그리고 앨범 사진, 아티스트 사진과 같이 이미지로 구성된 데이터들은 firebase storage를 활용하여 데이터를 저장합니다. 이미지를 업로드한 뒤, 이 이미지가 저장되는 경로를 Realtime Database로 저장하면 연결된 링크 주소를 이용하여 이미지를 가져올 수 있다.

- 데이터 저장 과정이 끝나면 노래 가사에서 분위기를 찾아내야 합니다. 이때 자연어 처리를 활용해야 하는데 한글 자연어 처리를 돕는 도구로서 파이썬 오픈소스 라이브러리의 KoNLPy (코엔엘파이)를 채택했다. 한글의 자연어처리 과정에는 형태소 분석이 가장 핵심적이다. 

- KoNLPy에서는 기존에 C, C++, Java등의 언어를 통해 형태소 분석을 할 수 있는 라이브러리들을 파이썬 라이브러리로 통합해서 제공한다. KoNLPy는 다양한 형태소 분석기들이 객체 형태로 포함되어 있으며 그 중에 성능이 좋은 편으로 알려진 Okt 형태소 분석기를 활용하여 Mood Station의 설계가 진행된다.

- 노래 가사 자연어 처리 과정으로는 firebase DB에서 자연어 처리를 위한 노래가사를 가져와 Okt에서 제공되는 함수를 통해 텍스트를 형태소 단위로 분류하여 품사 태깅(tagging)을 통해 명사와 형용사, 동사를 구분한다.

- 따라서 텍스트를 형태소 단위로 나누어 그에 해당하는 품사와 함께 리스트화 해주는 Pos 함수를 통해 노래 가사의 특정 명사나 형용사, 동사가 들어가는 노래를 태그 할 수 있다.

- 자연어 처리 과정이 끝나면 불용어 제거 단계에 들어간다. 불용어란 분석에 큰 의미가 없는 문맥적으로 큰 의미가 없는 단어들을 말한다. 

- 이런 불용어는 텍스트에 빈번하게 나타나므로 전처리 과정에서 중요한 단어로 인지될 수 있기 때문에 사전에 제거 과정이 필요하다. 

- 태그별로 노래들을 나누기 위해서는 DB에서 가져온 가사를 자연어 처리 KoNLPy를 이용하여 전처리 과정이 필요하다.

- 전처리된 데이터를 태그별로 쉽게 분류하기 위해서는 필요 없는 단어들을 추가로 제거해줘야 한다. 한국어의 경우 토큰화 단계에서 조사나, 접속사를 제거하면 됨으로 따로 정해진 불용어가 없지만 필요 없는 명사나 형용사를 제거하기 위해서는 직접 만든 불용어 리스트를 이용하여 제거할 수 있다.

- 불용어 제거 과정까지 마치고 나면 최종적으로 음악의 가사 검색 단계로 들어가게 된다. 가사 검색 api로는 Musixmatch Developer를 채택하였습니다. Musixmatch Developer는 웹 사이트나 애플리케이션에서 노래 가사를 표시하는 api이며 62개의 언어를 지원하고 사용자가 노래의 가사를 직접 등록할 수 있는 특징이 있다. 

- 첫 번째 호출은 검색 기능을 사용하여 카탈로그와 일치시키는 것이며, 두 번째 호출은 가사를 가져오는 것이다. 이렇게 사용자의 음악 재생 목록 분석을 통한 노래 추천 서비스 Mood Station이 설계된다.