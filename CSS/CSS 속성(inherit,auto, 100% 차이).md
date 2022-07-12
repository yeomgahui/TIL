
width나 Height를 쓸때 100 %, inherit, auto 의 차이점에 대해서 알아보자 

### 1. 100%
 - #innerDiv의 부모 컨테이너의 height의 100%를 차지함으로 실제 50px의 height를 갖게 된다.

```html
<div class="parent" style="height: 50px"> 
  <div id="innerDiv" style="height: 100%"></div>
</div>
```

### 2. auto
- #innerDiv의 자식노드의 height를 기준으로 height가 정해진다. 즉, #innerDiv의 height는 10px이 된다.

```html
<div style="height: 50px">
  <div id="innerDiv" style="height: auto">
    <div id="evenInner" style="height: 10px"></div>
  </div>
</div>
```

### 3. inherit
- 절대값 (부모의 height: 50px)부모의 height 값을 상속 받는다.
- #innerDiv는 부모의 height 값인 50px을 그대로 상속받는다.
```html
<div style="height: 50px">
  <div id="innerDiv" style="height: inherit">
    <div id="evenInner" style="height: 10px"> 
    </div>
  </div> 
</div>
```

-  상대값(부모의 height: 50%) #innerDive는 부모의 height값의 50%를 물려받으므로 부모 height값의 50%가 height로 지정된다.
```html
<div style="height: 50%">
  <div id="innerDiv" style="height: inherit"> 
    <div id="evenInner" style="height: 10px"> 
    </div>
  </div>
</div>
```
