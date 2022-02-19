# development_log

# 0. 오늘한것
javascript 동적 html생성 방식으로 불러온 데이터를 화면에 동적으로 생성해주기 => 정말 많이 헤맸음. 넌적스로만 해결해보려다가 사용할 수 있는 문법이 너무 제한적이라서 포기하고 자바스크립트로 직접 추가해주는 방향으로 진행함.

# 1.동적 html 생성
swiper-slide > image_wrap > slideimg, item-wrap > item-list
순서대로 태그가 있어서 이에 맞게 태그를 만들어줌.
* javascript 내에서 변수를 어떻게 쓰는지 헤맸는데 넌적스랑 똑같이 {{user.nick}} 형식으로 쓸 수 있음.
```html
  let itemlist2 = document.createElement('div');
  itemlist2.setAttribute('class', 'item-list2');
  itemlist2.innerText = '{{msg[2].sender}}';
  let a = parent3.lastChild;
  a.appendChild(itemlist2);
```
* parent3.lastchild: parent3 객체의 마지막 순서의 자식태그를 의미함.
* 문제: swiper가 우리가 새로 js로 만든 태그는 인식을 못했음. script순서에도 영향을 받음. 그래서 swiper관련 script를 html 태그 생성 script 밑에 넣어줬더니 성공적으로 해결됨.

# 2. 내일할것
1. 거래내역 완성하기
2. 메세지확인 버튼 고치기
3. 간격조정
