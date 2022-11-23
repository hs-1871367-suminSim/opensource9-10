## 시스템 설계서_API 연계 과정

#### 사용자의 음악 재생 목록 분석

Text Analytics로 사용자의 음악 재생 목록을 분석, 노래 검색을 위한 데이터(제목, 아티스트 등)을 추출합니다.

#### 노래 데이터 검색 및 저장

추출한 데이터를 기반으로 Elasticsearch를 통해 노래 데이터(트랙, 앨범, 아티스트, 앨범 등)를 검색 및 추출합니다.
추출한 데이터를 firebase DB에 저장합니다.

#### 노래 가사 검색 및 저장

firebase DB에서 노래 데이터 추출합니다.
노래 데이터를 기반으로 Musixmatch Developer에서 가사 검색 및 추출합니다.
추출한 가사 데이터를 firebase DB에 저장합니다.

#### 키워드 추출 및 저장
firebase DB에서 노래 가사 데이터를 추출합니다.
KoNLPy를 통해 자연어 처리합니다.
NLTK 라이브러리를 통해 불용어 제거합니다.
Text Analytics로 키워드를 추출합니다.
추출한 키워드를 Realtime Database에 저장합니다.

#### 노래 추천 과정

Realtime Database에서 키워드 데이터를 추출합니다.
사용자의 선호 키워드를 기준으로 sklearn을 이용해 유사도가 높은 곡들을 뽑습니다.
firebase DB에서 해당 곡들의 데이터를 추출하여 나열합니다.