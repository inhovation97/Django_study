## 장고는 admin 사이트를 이용해서 직관적으로 데이터 다룰 수 있다.
> 2021-02-13   
> 단, 테이블을 admin 사이트에 등록해주어야한다.   
> ~~실제 제대로된 웹을 만든다면, admin을 크게 활용할지는 모르겠다.~~    
### 1. 우선 admin 사이트의 관리자 계정을 만들어줍니다.
```shell
# 슈퍼유저 만들기
cd ch3
python manage.py createsuperuser
```
슈퍼계정으로 접속하면, 기본적으로 Groups, Users 테이블이 있다.   
앞서 말했듯이 여기에 애플리케이션의 테이블을 만들어서 admin에 등록해주면, admin에서 직관적으로 데이터를 조작할 수 있다.
### 2. admin에 등록할 애플리케이션(polls)을 개발하자 - Model 코딩
> 앞서 만든 polls라는 애플리케이션의 테이블을 만들었다.   
> 테이블은 [models.py]()에서 정의한다.   
> [admin.py]()에서 resister함수를 통해 테이블을 반영해준다.   
> 데이터베이스에 변경사항을 반영해주어야하므로 아래 명령어를 입력해주어야한다.
```shell
cd ch3
python manage.py makemigrations
python manage.py migrate
```
![image](https://user-images.githubusercontent.com/59557720/107843769-20e04480-6e11-11eb-8ff8-86976c3298f5.png)   
위에서 만든 테이블이 등록됨을 알 수 있다.
