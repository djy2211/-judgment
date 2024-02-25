# judgment


https://dacon.io/competitions/official/236112/overview/description

월간 데이콘 법원 판결 예측 AI 경진대회


*Train 컬럼

ID	

first_party	

second_party	

facts	

first_party_winner



first_party_winner > Bool 타입

나머지는 텍스트, 비정형 데이터

facts 의 내용에 따라 어느 당사자가 이겼는지 맞출 수 있도록 모델을 사용해야 함.
> first_party_winner 의 값을 예측

# try1 

TfidfVectorizer 사용

MultinomialNB 모델 생성하여 predict 적용

Accuracy: 0.65

# try2

CountVectorizer 사용

first_party

second_party

에 해당하는 당사자들을 one-hot 인코딩 적용

MultinomialNB 모델 생성

Training Accuracy: 0.9757820383451059

Test Accuracy: 0.6149193548387096

![19aff05b-7990-4dae-bc29-e885afdea5e4](https://github.com/djy2211/-judgment/assets/131187694/ab0148e1-1430-4294-b454-75756200d09c)

# try3

BERT 토크나이저 사용

Accuracy: 0.65

***
***
