## MTV 패턴

장고는 파이썬으로 작성된 오픈 소스 웹 프레임워크로 ```MVC(Model - View - Controller)``` 패턴을 따르고 있다.  
하지만 장고에서는 같은 개념을 ```MTV(Model - Template - View) ```라고 부른다.


### 1. Model
: ```DB```에 저장되는 데이터를 의미한다. 모델은 클래스로 정의되며 하나의 클래스가 하나의 ```DB 테이블```이 된다.
```장고```는 ```SQL```을 몰라도 ```DB``` 작업을 가능하게 해주는 ```ORM```을 제공해주기 때문에 직접 ```SQL```문을 짜지 않아도 된다.   
cf. ```ORM``` : ```Object-Relation Mapping```의 약자로 관계형 데이터베이스과 객체를 알아서 연결해주는 것.

### 2. Template
: 유저에게 보여지는 화면, ```html``` 파일   

### 3. View
: ```Request```에 따라 적절한 ```로직```을 수행하여 결과를 템플릿으로 ```렌더링``` 하여 ```Response```한다.

### + URLConf(URL설계)
: ```URL```과 ```View```를 매핑하는 단계, 해당하는 ```url``` 이 들어올 때 ```view```에서 어떤 ```함수```를 쓸지 설정해준다.   

--------------------------------------------------------------------------------------------------------------
```MVC``` 패턴과 ```MTV``` 패턴는 이름만 다를 뿐 둘은 대응된다.   
```MTV```패턴에서 ```Controller```의 역할은 누가 하는지 궁금해서 검색한 글에서 참고한 ```MVC``` 와 ```MTV```의 대응과 의미
```
Idiomatic term | Django term | Meaning
Model          | Model       | Contains all the business logic. At the very least the database access logic
View           | Template    | Responsible for generating the HTML and other UI
Controller     | View        | Contains the logic to tie the other parts together and to generate a response to a user request
```
즉, ```MVC```패턴의 ```Controller``` 는 ```Model```과 ```View```의 중간다리이고, 그에 대응되는      
```MTV```패턴의 ```View```는 ```Model```과 ```Template```의 중간다리 역할을 한다.  

출처: https://stackoverflow.com/questions/50636257/django-and-tinymce-nameerror-name-url-is-not-defined/50651288
