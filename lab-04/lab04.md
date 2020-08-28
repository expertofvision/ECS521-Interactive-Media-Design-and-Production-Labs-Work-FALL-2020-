<div align="center">
  <img src="https://www.qmul.ac.uk/blizard/media/blizard/images/logos/QMUL_White.png" />

# School of Electronic Engineering and Computer  Science

## ECS521U - INTERACTIVE MEDIA DESIGN AND PRODUCTION</br>Lab 4
</div>

### About this Lab
The purpose of this lab session is basis of data persistance.

## A. Setup
1. Open index.html file in browser (chrome/firefox/ie).
2. Open index.html files in a text editor.

## B. Text Processing
Write a program to count the vowels in a text.

1. Open process_text.js file in a text editor
2. Add both the button and textarea elements: 
    let btn = document.getElementById('count_btn');
    let txt_field = document.getElementById('input_txt');
3. Go to the onlick event definition for the button. 
    btn.onclick = function() {
    };
4. Add the value typed on the text area.
    let txt = txt_field.value;
5. Create an array that contains the vowels. This will be used later to check if a character in the text is a vowel 
    let vowels = ['a', 'e', 'i', 'o', 'u'];
6. Traverse the input text and check if each character is a vowel or not. If it is, increase the counter by one 
    for (let i = 0; i < txt.length; i++) {
    if (vowels.includes(txt.charAt(i).toLowerCase())) {
    count++;
    }
    }
7. Get the element where the result is going to be displayed. 
    let result = document.getElementById('display_result');
8. Set a new value to the previous element, reflecting the number of vowels present in the input text: 
    result.innerHTML = 'Your input contains ' + count + ' vowels';

## C. HTML5 Web Storage.

The rest of the lab will be focused on achieving data persistence using a web storage. 
“With web storage, web applications can store data locally within the user’s browser” [1]. The storage limit is at least 5MB. There
are two properties that can be used: localStorage and sessionStorage. The difference between them is that “localStorage
has no expiration time, whilst data stored in sessionStorage gets cleared when the page session ends — that is, when the page
is closed” [2].

The lab will focus on using localStorage property.

## D. Create a greeting message with your name
1. Open greet_user.js file in browser (chrome/firefix/ie).
2. Open greet_user.js file in a text editor.
3. Go to the definition of update_greet_message() functionCheck if the item name exists in the localStorage and if it does, update the message to display: 
    if (localStorage.name) {
    greetings.innerHTML = 'Hello ' + localStorage.name + '!';
    }

4. Go to the definition of greet_user() function
5. Add the event onclick for the button. The goal is to get the name entered by the user and display the greeting message 
    btn.onclick = function() {
    localStorage.name = name_field.value;
    update_greet_message();
    };
6. Close the browser and open it once again
Note the greet message displays the name given by the user.

## E. Persistance using XML files 
Check for reference: * Lab #2 * XML HttpRequest * How to create a DOM tree. 
1. Following the first exercise, given an input text, try to count the occurrences of each vowel independently.
2. Save these results into a XML file.










