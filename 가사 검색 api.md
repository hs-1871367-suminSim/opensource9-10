가사 검색 api - Musixmatch Developer

음악의 가사 검색 api로 Musixmatch Developer 를 채택했다.

Musixmatch Developer는 웹사이트나 애플리케이션에서 노래 가사를 표시하는 api이며

62개의 언어를 지원하고 사용자가 노래의 가사를 직접 등록 할 수 있는 특징이 있다. 

API 작동 단계

\- musixmatch API 이용약관, 개인정보 보호정책 확인

\- API 키 등록

\- API 호출 및 응답 에 대한 세부 정보 확인

\- musixmatch 서비스를 웹 사이트, 애플리케이션과 통합 

`  `- 2가지 API 호출을 구현

`     `첫 번째 호출은 검색 기능을 사용하여 카탈로그와 일치시키는 것

`     `두 번째 호출은 가사를 가져오는 것



\*검색 기능- track.search

q\_track

q\_artist

q\_lyrics

q\_track\_artist

q\_writer

q

f\_artist\_id

f\_music\_genre\_id

f\_lyrics\_language

f\_has\_lyrics

f\_track\_release\_group\_first\_release\_date\_min

f\_track\_release\_group\_first\_release\_date\_max

s\_artist\_rating

s\_track\_rating

quorum\_factor

page

page\_size

\*가사를 가져오는 기능 - track.lyrics.get 

웹사이트용 자바스크립트 스크립트

<script type="text/javascript" src="http://tracking.musixmatch.com/t1.0/AMa6hJCIEzn1v8RuOP">

이미지 픽셀 (스크립트를 사용할 수 없는 경우 이미지 src로 pixel\_tracking\_url 필드에 반환된 URL을 포함)

<img src="http://tracking.musixmatch.com/t1.0/AMa6hJCIEzn1v8RuXW">

매개변수

track\_id, commontrack\_id

Musixmatch Developer 장점

-노래가 등록되어 있다면 누구라도 가사 등록이 가능

-다른 사람이 등록한 가사를 자신이 추가로 편집하거나 반대의 경우도 가능

Musixmatch Develope 단점 

-Musixmatch에 곡을 추가하고 싶어도 해당 곡이 등록되기 전까지는 사용자가 할 수 있는 방법이 없음

-가사 검색 기능에 오류가 있음

활용 방법

Musixmatch를 활용하여 노래의 가사를 검색해 가져오고, 만약 노래의 가사가 없거나 오류가 있다면

Musixmatch에서 직접 수정할 것이다.





