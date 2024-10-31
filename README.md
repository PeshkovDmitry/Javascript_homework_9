В этом задании вам предстоит работать с различными событиями и манипуляциями
DOM.   
Все задачи выполняйте внутри тега "script".

Дан код:
```
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <title>Homework 5</title>
    <style>
        .error {
            border: 2px solid red;
            outline: none;
            /* Убираем стандартное выделение при фокусе */
        }
        /* Анимация для появления */
        .animate_animated {
            animation-duration: 1s;
            /* Продолжительность анимации */
            animation-fill-mode: both;
            /* Держать финальное состояние анимации */
        }
        .animate_fadeInLeftBig {
            @keyframes fadeInLeftBig {
                0% {
                    opacity: 0;
                    transform: translateX(-1000px);
                }

                100% {
                    opacity: 1;
                    transform: translateX(0);
                }
            }
            animation-name: fadeInLeftBig;
        }
    </style>
</head>

<body>
    <input id="from" type="text">В инпуте написано: <span></span>
    <br>
    <button class="messageBtn">Показать блок</button>
    <div class="message">Привет :)</div>
    <br>
    <form>
        <label>
            Первый инпут:
            <input class="form-control" type="text">
        </label>
        <br>
        <br>
        <label>
            Второй инпут:
            <select class="form-control">
                <option value=""></option>
                <option value="1">Один</option>
                <option value="2">Два</option>
            </select>
        </label>
        <br>
        <br>
        <button type="submit">Отправить</button>
    </form>
</body>

</html>
```

Задачи:
1. При изменении значения в "input" с id="from", значение, содержащееся
в нем, должно моментально отображаться в "span".
- Это значит, что при каждом изменении текста в инпуте, текст в "span"
должен обновляться соответственно.
2. При клике на кнопку с классом messageBtn необходимо выполнить
следующие действия для элемента с классом message:
- Добавить два класса: animate_animated и animate_fadeInLeftBig.
- Установить стиль visibility в значение 'visible'.
3. При отправке формы проверьте, заполнены ли все поля.
- Если какое-либо поле не заполнено, форма не должна отправляться.
- Незаполненные поля должны быть подсвечены (добавлен класс error).  
Как только пользователь начинает заполнять поле, выполните проверку:  
Если поле пустое, подсветите его (добавьте класс error).  
Если поле заполнено, уберите подсветку (удалите класс error).
