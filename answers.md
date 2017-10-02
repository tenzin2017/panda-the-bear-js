1. changing the img src of panda bear
   var image = document.querySelector('img');
   image
   image.src = 'https://placebear.com/400/400';

2. changing the img src of sky
   var imageSky = document.querySelecor('#left-image');
   imageSky
   var sky = imageSky.querySelecor('img');
   sky.src = 'https://unsplash.it/325/225';
3. changing h1 to my name
    var h1 = document.querySelector('h1');
    h1.innerText = 'Lobsang Tenzin';

4. changing the element colour using highlight class
   var highlight = document.querySelectorAll('.highlight');
   for(var i=0; i<highlight.length; i++){
     highlight[i].style.backgroundColor = '#2c7c9a';
   }


5. changing the background color of body
   document.body.style.backgrounColor = '#2d507b';

6. changing the font family of h1
   var h1 = document.querySelector('h1');
   h1.style.fontFamily = 'monospace';

7. changing the aside circle icon colour
   var circle = document.querySelectorAll('.action-icon-bg');
   for(var i=0; i<circle.length; i++){
     circle[i].style.backgrounColor = 'yellow';
   }

8. changing the placeholder name in the form to 'identify yourself'
   var namePlaceHolder = document.querySelector('form input');
   namePlaceHolder.placeholder = 'Identify Yourself';

9. message field placeholder changed to 'state your business'
   var messageField = document.querySelector('form textarea');
   messageField.placeholder = 'state your business';

10. giving the name field a value attribute as 'your nemesis'
    var nameValue = document.querySelector('form input');
    nameValue.value = 'your nemesis';

11. email value attribute changed to 'koalathebear@gmail.com'
    var emailValue = document.querySelector('#email');
    emailValue.value = 'koalathebeer@gmail.com';

12. value of submit button changed to 'En garde!'
    var submitValue = document.querySelector('#submit').value = 'En garde!';

13. submit button disabled
    var submitDisabled = document.querySelector('#submit').disabled = true;

14. Erase personal details from the sidebar
    var bioInfo = document.querySelectorAll('.bio-info');
    bioInfo[0].style.display = 'none';

**REMOVING ELEMENTS FROM THE DOM***********
15. Removing elements from the DOM
    var timeTravelSkill = document.querySelector('#time-travel');
    timeTravelSkill.parentElment    // this is not a method , so we didnt use (), selects parent element
    timeTravelSkill.parentElemnt.remove()

**ADDING ELEMENTS TO THE DOM***********
16. (1). using cloneNode(), clone the pikachu img and insert after the .portfolio-container class
    var pikachu = document.querySelector('#right-image img');
    pikachuCloned = pikachu.cloneNode();

    //selects the .portfolio-container
    var div = document.querySelector('.portfolio-container');
    div.appendChild(pikachuCloned);

    (2).adding cloned image of pikachu 10 times using for loop
      for(var i=0; i<10; i++){
        div.appendChild(pikachuCloned);
      }

Adding a new list Item at the end of the list on the sidebar with same css style
// selects ul element where we have to append child (li)
var div = document.querySelector('.bio-info');   

var listItem = document.createElement('li');  // create Element type li
var leftSpan = document.createElement('span'); // create element type span
var lastUpdated = document.createTextNode('Page last Updated on')  // text msg inside span

leftSpan.append(lastUpdated);     // adding text inside span
leftSpan.className = 'bio-info-title';  // assign class same as other other spans in the ul

listItem.append(leftSpan);   // adding leftSpan at the end and inside listItem
listItem.className = 'bio-info-item';  // assigned classname inside li tag

div.append(listItem);

var rightSpan = document.querySelector('span');
rightSpan.className = 'bio-info-value bio-info-date';

var date = new Date(Date.now());
rightSpan.innerText = date;

listItem.append(rightSpan);
