# markdown_20230127
마크다운 설명

### 7. 하이퍼링크 
[e클래스](https://cafe.daum.net/pcwk "e클래스의 cafe입니다.")

### 6. 가로 라인
---
***
------
###5. 코드블록 
```
def index(request):
    '''Question 목록'''
    #list order create_date desc
    # print('index 레벨로 출력')
    question_list = Question.objects.order_by('-create_date') #DSC / 마이너스 빼면 ASC
    # question_list = Question.objects.filter(id=99)
    context = {'question_list': question_list}
    print('question_liste:{}')
    return render(request,'pybo/question_list.html',context)
```


### 4. 목록  
1. 아이템1  
2. 아이템2  
   9. 단계 하위 아이템   
     3. 단계 하위 아이템  
- 아이템 1  
+ 아이템 2  
  - 1단계 하위 아이템 
    * 2단계 하위 아이템 
* 목록이름  
- 목록 
+ 목록
+ 위 3개 html로 따지면 ul이다 (순서가 없는 목록) 

순서있는 목록  
1. 목록이름
2. 목록
3. 3번 째 목록 

#### 3. 인용문 
> 여기에 인용할 내용을 넣으면 됩니다. 
> 빈 줄이 없으면 자동으로 인용 상자에 포함이 됩니다. 

## 2. 헤더 
# 헤더1
## 헤더2
### 헤더3
#### 헤더4
##### 헤더5


### 1. 문단 구분을 위한 개행.
문단을 작성합니다.(엔터역할 : 공백 2개)    
겨울이 가고 봄이 옵니다. 
