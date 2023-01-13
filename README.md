
[![N|Solid](dom-in-js.jpg)

```
                                         Table of Contents
```
****
****
#### 1 Dom

#### 2 Introduction to browser events

#### 3 Forms, controls
****
****
## DOM
[![N|Solid](que-es-don.png)
***
[![N|Solid](document-object.avif)

> DOM ба объекти ҳуҷҷат
Модели (DOM), ҳар як теги HTML як
объект аст. Тегҳои дохилшуда "фарзандони" мебошанд
иҳотакунанда. Матни даруни а
тег низ объект аст.
***
***
[![N|Solid](image4-1.png)
***
***
## DOM - Searching: getElement*,querySelector* - getElementById
> Дар ин боб шумо хоҳед фаҳмид, ки барои чӣ getElement* истифода мешавад ва инчунин ду усули муҳими зерин: querySelectorва querySelectorAll.

##### Document.getElementById ё Танҳо ID
> Хусусиятҳои навигатсионии DOM вақте ки онҳо ба ҳамдигар наздиканд, аъло мебошанд. Дар акси ҳол, усулҳои иловагии ҷустуҷӯ истифода мешаванд.

Яке аз онхост document.getElementById(id). Шумо метавонед онро вақте истифода баред, ки элемент атрибут дошта бошад id, новобаста аз он ки он дар куҷост.

Намунаи истифодаи document.getElementById(id)он чунин аст:
let div = document.createElement('div');
div.id = 'content';
div.innerHTML = '<p>Create Element example</p>';
document.body.appendChild(div);
document.getElementById('content').style.padding = '10px';
document.getElementById('content').style.background = 'yellow';
document.getElementById('content').style.color = 'red';
***

### Introduction to browser events
>Муносибати JavaScript бо HTML ин аст
тавассути рӯйдодҳое, ки рӯй медиҳанд, ҳал карда мешаванд
вақте ки корбар ё браузер
саҳифаро идора мекунад.
Вақте ки саҳифа бор карда мешавад, он номида мешавад
ҳодиса. Вақте ки корбар тугмаро пахш мекунад,
ки ин клик хам вокеаест. Дигар
мисолхо ходисахои монанди
пахш кардани ягон тугма, пӯшидани тиреза,
тағир додани андозаи тиреза ва ғайра.
<!DOCTYPE html>
<html>
  <head>
    <title>Title of the Document</title>
  </head>
  <body>
    <input id="inputId" type="button" value="Click">
    <script>
      inputId.onclick = function() {
        alert('Welcome to SoftClub');
      };
    </script>
  </body>
</html>

****
***

### Forms, controls

> Санҷиши формати HTML-ро тавассути JavaScript иҷро кардан мумкин аст.
Агар майдони форма (fname) холӣ бошад, ин функсия паёмро огоҳ мекунад ва бардурӯғ бармегардонад, то пешниҳоди формаро пешгирӣ кунад:
function validateForm() {
  let x = document.forms["myForm"]["fname"].value;
  if (x == "") {
    alert("Name must be filled out");
    return false;
  }
}
***
>Тасдиқи формати HTML метавонад тавассути браузер ба таври худкор анҷом дода шавад.
Агар майдони форма (fname) холӣ бошад, requiredатрибут пешниҳоди ин формаро пешгирӣ мекунад:


<form action="/action_page.php" method="post">
  <input type="text" name="fname" required>
  <input type="submit" value="Submit">
</form>

****
****
[![N|Solid](document.png)
***
***
## createElement()
> Усули JavaScript document.createElement() ба шумо имкон медиҳад, ки а эҷод ва баргардонед
унсури нав (гиреҳи Элементи холӣ) бо номи барчасп.
> 1) createElement(elementName): Элементи html эҷод мекунад, ки тегаш аст
ҳамчун параметр гузашт. Элементи сохташударо бармегардонад
2) createTextNode(text): гиреҳи матниро эҷод ва бармегардонад. Матни гиреҳ аст
ҳамчун параметр гузашт.

> 1)let div = document.querySelector("div")
let but = document.createElement("button");
but.innerHTML = "BUTTON";
div.appendChild(but)
[![N|Solid](Screenshot%20A.png)




