# react로 todo list 만들기

input value 값에 state를 하나 부여한다.

```
 const onSubmit = (e) => {
    e.preventDefault();
    if (toDo == "") {
      return;
    }
    setToDos((currentArray) => [toDo, ...currentArray]);
    setToDo("");
  };
```

---

> prevent defalut로 새로고침 방지하고
> 바닐라였다면 value값을 바로 어레이에 push 했겠지만
> value 값을...currentArray로 복사한 배열 값에 추가하는 방식으로 진행해야한다

```
 <ul>
        {toDos.map((item, i) => (
          <li key={i}>{item}</li>
        ))}
      </ul>
```

맵으로 생성한 li 값안에 유니크한 key값을 넣는다
