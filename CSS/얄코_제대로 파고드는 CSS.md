# **선택자**

- 우선순위 : 태그 < class < id
- CSS는 구체적으로 표현할 경우 우선순위가 높아진다.

```
/* 모든 요소 선택 */
* {
  font-weight: bold;
  color: darkorange;
}

/* 같은 선택자의 경우 뒤에 오는 것이 우선순위 높음 */
* {
  color: plum;
}


/* class 선택자 */
/* 태그보다 우선순위 높음 */
.blue {
  color: lightblue;
}

/* 다른 선택자에 이어붙일 수 있음(태그, 클래스 등...) */
/* 선택자는 구체적일수록 우선순위 높음 */
p.blue {
  color: slateblue;
}

.blue.dark {
  color: mediumblue;
}

p.blue.dark {
  color: darkblue;
}

/* id 선택자 */
/* class보다 우선순위 높음 */
/* id는 페이지상에서 요소마다 고유해야 함 */
#red {
  color: tomato;
}

/* 그룹 선택자 */
span, .dark, #red {
  text-decoration: underline;
}
```

```
//EX code

<div class="outer">
    <li>a</li>
    <li>a</li>
    <li>a</li>
        <ul>
            <li>b</li>
            <li>b</li>
            <li>b</li>
        </ul>
    <li>a</li>
</div>
```

```
/* outer 속 모든 li 적용 */
.outer li {
  color: olivedrab;
}

/_ outer 바로 아래의 li에만 적용 _/
.outer > li {
color: dodgerblue;
}

.outer > li li {
text-decoration: underline;
}

/_ 해당 클래스 다음의 li는 다 적용 _/
.starter ~ li {
font-style: italic;
}

/_ 뒤따르는 바로 다음 요소만 적용_/
.starter + li {
font-weight: bold;
}

/_ 첫 번째, 마지막 요소 가상 클래스 _/
ol li:first-child,
ol li:last-child {
color: yellowgreen;
}

/_마지막 li는 제외하고 다 적용 _/
.outer > li:not(:last-child) {
text-decoration: line-through;
}

ul:not(.outer) li {
font-weight: bold;
}

```

```
li의 스타일을 지정 가능
ul {
  list-style: circle;
}

/* li별로 지정하는 것도 가능 */
ul > li:first-child {
  list-style: "🚩 "
}

ol {
  list-style: lower-alpha;
}
```

# **font**

- px는 절대값 , %는 부모요소를 기준으로 결정되며 100% = 1em이다.
- rem은 부모요소가 아닌 html요소를 기준으로 결정된다.

# **Box-model**

- vw와 vh는 viewport를 기준으로 적용된다.
- vmax와 vmin을 사용하여 가로 세로 중 큰것 혹은 작은것을 기준으로 결정할 수 있다.
- calc(50% +50px)으로 산수식으로 결정할 수 있다.

```
[margin]
- margin의 경우 자식요소가 부모요소에 상관없이 적용될 수 있으므로 조심해야한다.
- block의 경우 , 위 아래가 margin이 있는경우 더 큰쪽이 적용된다.
- margin :auto 너비가 지정된 block의 가로 방향의 남은 공간을 채운다.
```

- overflow는 자식요소가 부모요소보다 높이나 너비가 큰 경우 사용한다.
- box-sizing이 content-box인 경우 width,height는 border가 포함되지 않지만, border-box일 경우 border도 포함되어 계산된다.

```
[position]
- static은 요소의 위치를 지정하지 않음
- relative 원래 위치를 기준으로 움직인다.(원래 위치는 고정된 상태)
- absoulte는 맨 위의 부모를 기준으로 움직인다.(원래 위치는 사라짐)
- fixed는 veiwport를 기준으로 고정된다.
- sticky는 요소가 고정될 위치를 지정해줄 수 있다.
```

```
 <meta name="viewport" content="minimum-scale=1, initial-scale=1, width=device-width" />
 위 코드를 입력해줘야 반응형웹에서 viewport가 올바르게 적용된다.
```

- verticle-align은 inline속성에서 적용된다.
- transition 속성은 CSS값이 달라질 경우 어떤 효과로 보여질 지 지정한다.(속성 , 지속시간, 시간함수 , 지연시간 순)
