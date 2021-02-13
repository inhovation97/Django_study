## View, Temaplate 코딩하기
> 앞서 polls라는 어플리케이션의 mdoels.py에서 클래스를 만들었음.      
> 이제 해당 클래스의 View(로직), Template(UI 화면)를 만들어야함.    
> 순서는 상관없지만, URLconf -> Template -> View 순으로 코딩함.   

### 1. 사이트 설계하기
**질문 -> 답변을 투표 -> 결과 집계 화면**   
위 형식으로 사이트를 구성할 것이므로 4개의 view 함수( index(), detail(), vote(), results() )와 3개의 Tempalte(index, detail, results)를 코딩한다.   

### 2. URLconf 코딩
> url.py에서 자신이 설계한 페이지의 url과 그 url을 어떤 View와 매칭 시킬지 정의해줍니다.
> 지금은 간단하지만, 실제로는 수많은 애플리케이션이 있을 수 있기 때문에 URLconf를 계층적으로 구성해야함
```shell
# 구조가 굉장히 간단함
urlpatterns = [
    path('url 주소1', 매칭시킬 view1),
    path('url 주소2', 매칭시킬 view2),
    path('url 주소3', 매칭시킬 view3),
    ]
```
[polls 애플리케이션url파일](https://github.com/inhovation97/Django_study/blob/main/django_ex/ch3/polls/urls.py)에서 이름 공간을 정의하고, 이를 
[상위url파일](https://github.com/inhovation97/Django_study/blob/main/django_ex/ch3/mysite/urls.py)에서 받음

### 3. View, Template 코딩
> 질문 화면 -> 답변을 투표하는 화면
> UI 화면을 생각하면서 로직을 풀어나가면 쉽기 때문에 Template을 먼저 코딩
template 디렉토리 만들어주기
```shell
cd ch3\polls
mkdir templates
mkdir templates\polls   
cd tempaltes\polls
notepad index.html # html 생성
```

가장 먼저 [index.html](https://github.com/inhovation97/Django_study/blob/main/django_ex/ch3/polls/templates/polls/index.html)코딩   
view.py에서 [index 매핑 함수](https://github.com/inhovation97/Django_study/blob/main/django_ex/ch3/polls/views.py)코딩   
두번째 페이지인 [detail.html](https://github.com/inhovation97/Django_study/blob/main/django_ex/ch3/polls/templates/polls/detail.html)을 코딩   
view.py에서 [detail 매핑 함수](https://github.com/inhovation97/Django_study/blob/main/django_ex/ch3/polls/views.py)코딩   
투표하는 것은 **detail.html** 화면에서 이뤄지므로 템플릿은 필요없고, 로직 [vote()](https://github.com/inhovation97/Django_study/blob/main/django_ex/ch3/polls/views.py)만 코딩   
마지막 화면 [results.html](https://github.com/inhovation97/Django_study/blob/main/django_ex/ch3/polls/templates/polls/results.html)코딩   
view.py에서 [results 매핑 함수](https://github.com/inhovation97/Django_study/blob/main/django_ex/ch3/polls/views.py)코딩  
마지막으로 admin 사이트에서 질문이나 답변 데이터를 넣어줌!   
### 사이트가 제대로 반영됨!
![image](https://user-images.githubusercontent.com/59557720/107852851-42afea80-6e56-11eb-9d40-a8b235f72f78.png)   



