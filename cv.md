![my photo](assets/IMG20220805104253.jpg)
My name is Tatyana Shuniborova.
I live in Minsk, Belarus.
My telephone number: +375-29-863-88-11
Other communication methods: viber/telegram +375-29-863-88-11
Content:
1. [About me](#about)
2. [Skills](#skills)
3. [Example code](#example)


<a id="about">___About me___</a>
I graduated Institute of business BSU on web-design.  I learned some languages of programming as:  HTML5, CSS3, JavaScript. 
On the lessons of JavaScript we were studying native JavaScript, jQuery and some features of animation.
I finished study some graphic program such as: Photoshop, corel, adobe animation and 3ds max.
In that time i am learning in innodom on the course of JavaScript. 
I learned English some time ago, and I want to learn this language more. I graduated some curses of English as: elementary, pre-intermediate and intermediate levels.
I started to learn programming in some years ago and I hope that i will know this on the nessesary level for get new job on this sphere.
I am working as technical support of some web-sites and i want to try be developer on react in our project.

---

<a id="skills">__Skills:__</a>
* HTML5.0;
* CSS3.0;
* JavaScript;
* jQuery;
* SQL;
* graffic programs:
  * Corel;
  * PhotoShop;
  * AdobeAnimation.

---

<a id="example">__Example code:__</a>
```
_//счетчик  цифр_
const timeCount = 10000,
  step = 20;
function outNum(num, elem) {
  let numb = document.querySelector("#" + elem);
  n = 0;
  let timeView = Math.round(timeCount / (num / step));
  let interval = setInterval(() => {
    n<num? (n += step): clearInterval(interval);
    numb.innerHTML = n;
  }, timeView);
}
_// валидация формы регистрации_
function validate() {
  let errList=document.querySelectorAll ("span");
  let userName=document.getElementById('userName');
  console.log(userName);
  let userPhone=document.getElementById('userTelephone');
let item=document.createElement("span"); 
item.innerHTML ="Поле обязательно для заполнения";
  for (let i= errList.length-1; i>=0; i--) {
        errList[i].remove();
    }
    if (!userName.value){
    userName.classList.add("errorList");
    userName.parentNode.insertBefore(item,userName.nextSibling);
    return false;
    } else{
    userName.classList.remove("errorList");
    item.remove();
  }
  if (!userPhone.value){
    userPhone.classList.add("errorList");
    userPhone.parentNode.insertBefore(item,userPhone.nextSibling);
    return false;
  }
  else{
    userPhone.classList.remove("errorList");
    item.remove();
  }
    
    form=document.entered;
    let login=isFullText(userName);
    let phone=isPhone(userPhone);
    return login&& phone;
}
function isFullText(fieldInp) {
  var letters = /^[A-Za-z]+$|^[А-Яа-я]+$/;

  if (fieldInp.value.match(letters)) {
    fieldInp.className = fieldInp.className.replace("alert", "");
    return true;
  } else {
    fieldInp.className = "alert";
    var item = document.createElement("span");
    item.innerHTML = "Имя должно состоять из букв латиницы или кириллицы";
    fieldInp.parentNode.insertBefore(item, fieldInp.nextSibling);
    return false;
  }
}

function isPhone(userPhone) {
  var pattern = /^(\+\d{3})(\d{2})(\d{3})(\d{2})(\d{2})$/;
  if (userPhone.value.match(pattern)) {
    userPhone.className = userPhone.className.replace("alert", "");
    return true;
  } else {
    userPhone.className = "alert";
    var item = document.createElement("span");
    item.innerHTML = "Телефон должен быть формата +375...";
    userPhone.parentNode.insertBefore(item, userPhone.nextSibling);
    return false;
  }
}
```