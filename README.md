# grad_project
<1. 악플 골라내기>

1.네이버 웹 크롤링(beautifulsoup 도구 이용하여 댓글 크롤링하기
(선플 예시 : https://entertain.naver.com/ranking/read?oid=311&aid=0001096155, https://entertain.naver.com/ranking/read?oid=008&aid=0004335668,
https://entertain.naver.com/ranking/read?oid=312&aid=0000429270
악플 예시 : https://entertain.naver.com/ranking/read?oid=408&aid=0000084626,
https://entertain.naver.com/ranking/read?oid=052&aid=0001384803,
https://entertain.naver.com/ranking/read?oid=382&aid=0000788705)
google cloud 감성 api 사용해서 걸러내기
->악플 20000개, 선플 20000개씩 데이터 얻기
->train : val : test(3-way holdout) = 6: 2: 2로 데이터 나누기

2.텍스트 전처리 시작 
토큰화 및 불용어 제거 : 형태소 분석기 통해서 중요 명사, 동사 추출하기(형태소 분석기로 Okt(Open Korea Text), 메캅(Mecab), 코모란(Komoran), 한나눔(Hannanum), 꼬꼬마(Kkma))

3.기계가 데이터를 숫자로 처리하도록 정수 인코딩 수행

4.LSTM 사용하여 감성 분류하기(epochs 및 activation funtion은 https://wikidocs.net/44249 참고)



<2. 선플 만들어내기>

1.1-1에서 얻은 선플 샘플 데이터 이용하기

2.텍스트 전처리 시작 
토큰화 및 불용어 제거 : 형태소 분석기 통해서 중요 명사, 동사 추출하기(형태소 분석기로 Okt(Open Korea Text), 메캅(Mecab), 코모란(Komoran), 한나눔(Hannanum), 꼬꼬마(Kkma))

3.문맥을 살리기 위해서 word embedding matrix 구성

4.rnn-language 모델 및 seqgan 이용하여 새로운 선플 문장 생성해내기
