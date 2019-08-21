<!-- PART ONE  -->
<!-- 1.Use the same approach to select the element that contains the photo of the sky and change the src attribute to another picture URL of your choosing. -->
let profileImage = document.querySelector('.profile-image'); 
undefined
profileImage.src = "https://placebear.com/200/300"
"https://placebear.com/200/300"

<!-- 2. Select the heading that says "Panda the Bear" and change it to your own name -->

let name = document.querySelector('h1');

name.innerText= "Abigail Cudjoe";
"Abigail Cudjoe"

<!-- 3. Select the heading that says "Employment" and change it to something else.  -->
let hobbies = document.querySelector('#employment .info-title')
undefined
hobbies.innerText = "Hobbies";
"Hobbies"

<!-- 4. Change the colour of the body -->

let bodyColour = document.querySelector('body');
undefined
bodyColour.style.backgroundColor = '#B0E977';
"#B0E977

<!-- 5. Change the colour of each element using the highlight class. Use a for loop to do this. -->
let highlightClass = document.querySelectorAll('.highlight');
>>undefined
highlightClass
>>NodeList(8) [aside.highlight, h1.highlight, div#sleep.bar-filled.highlight, div#eat.bar-filled.highlight, div#time-travel.bar-filled.highlight, div#cry.bar-filled.highlight, h2.highlight, h2.highlight]

for (let high = 0; high < highlightClass.length; high ++) {
    highlightClass[high].style.color = 'red';
}
>>"red"



<!-- 6. change the h1 font tomonospace -->

let font = document.querySelector('h1'); 
undefined
font.style.fontFamily = 'monospace';
"monospace"

<!-- 7.Find a way to select the round icons in the sidebar and then change their colour. -->
let roundIcons = document.querySelectorAll('.action-icon-bg');
roundIcons
>> NodeList(2) [a.action-icon-bg, a.action-icon-bg]
for (let icon = 0; icon <roundIcons.length; icon ++) {
    roundIcons[icon].style.backgroundColor = "black";
}
>>"black"

<!-- 8. Scroll down to the contact form. Change the placeholder attribute of the name field to "identify yourself". -->
let placeHolder = document.querySelector('#name')
placeHolder.placeholder = "Identify Yourself";

<!-- 9. Change the placeholder attribute of the message field to "state your business". -->
let messagePlaceHolder = document.querySelector('#message');
>>undefined
messagePlaceHolder
>><textarea name=​"message" id=​"message" placeholder=​"Message">​</textarea>​
messagePlaceHolder.placeholder = "State your business";
>>"State your business"

<!-- 10. Give the name field a "value" attribute of "your nemesis". -->

placeHolder.placeholder = "Your Nemesis";
>>"Your Nemesis"

<!-- 11. Change the value attribute of the email field to "koalathebear@gmail.com". -->

let emailPlaceHolder = document.querySelector('#email');
>>undefined
emailPlaceHolder
>><input type=​"email" name=​"email" class=​"contact-info" id=​"email" placeholder=​"Email">​
emailPlaceHolder.placeholder = "koalathebear@gmail.com";
>> "koalathebear@gmail.com" 

<!-- 12. Change the value of the submit button on the contact form to "En garde!". -->

let submitValue = document.querySelector('#submit');
>>undefined
submitValue
>><input type=​"submit" name=​"submit" id=​"submit" value=​"Submit">​
submitValue.value = "EN GARDE!";
>>"EN GARDE!"
<!-- 13. We should stop Koala from sending an email to Panda that they might regret! Find a way to disable the submit button (hint: familiarize yourself with the disabled attribute). -->
submitValue.disabled = true
true

<!-- 14. We should help Panda protect their privacy by erasing their personal details from the sidebar.  -->
$$(".bio-info-value")
>> (3) [span.bio-info-value.bio-info-name, span.bio-info-value.bio-info-location, span.bio-info-value.bio-info-phone]

$$(".bio-info-value")[1].remove();
undefined
$$(".bio-info-value")[1].remove();
undefined

<!-- NB: jQuery selectors $() : returns a single object $$() : returns a collection of objects   -->

<!-- PART TWO -->
<!-- 1. Panda the Bear is lying about their skills! Take the "time travel" skill off the page to satisfy your personal sense of justice. -->
$("#time-travel").remove()

<!-- 2. cloning pikachu -->
let pikaPic = document.querySelector ('#right-image > img')
let clone = pikaPic.cloneNode(true);
let section = document.querySelector('.portfolio-container');
section.appendChild(clone);

<!-- 3. cloning pikachu many times -->

for (pika = 0; pika < 10; pika ++) {
    let newPikaClone = document.createElement('img');
    newPikaClone.src = 'images/pikachu-drawing.jpg';
    section.appendChild(newPikaClone); 
}

<!-- 4. adding update with time -->
const listItem = document.createElement('li');
>>undefined
const leftSpan = document.createElement('span');
>>undefined
var lastUpdated = document.createTextNode('Page last update on');
>>undefined
leftSpan.appendChild(lastUpdated);
>>"Page last update on"
listItem.appendChild(leftSpan);
>><span>​Page last update on​</span>​
const rightSpan = document.createElement('span');
>> undefined
let dateUpdate = new Date()
let date = document.createTextNode(dateUpdate);
undefined
date 
>>"Tue Aug 20 2019 21:04:27 GMT-0400 (Eastern Daylight Time)"
rightSpan.appendChild(date);
>>"Tue Aug 20 2019 21:04:27 GMT-0400 (Eastern Daylight Time)"

listItem.appendChild(rightSpan);
let bioInfo = document.querySelector('.bio-info');
>> undefined
bioInfo.appendChild(listItem);
>> <li>​…​</li>​


