<div align="center">
  <img src="https://www.qmul.ac.uk/blizard/media/blizard/images/logos/QMUL_White.png" />

# School of Electronic Engineering and Computer  Science

## ECS521U - INTERACTIVE MEDIA DESIGN AND PRODUCTION</br>Lab 4
</div>

### About this Lab
The purpose of this lab session is basis of data persistance.

## A. Setup
1. Open [index.html](https://github.com/expertofvision/ECS521-Interactive-Media-Design-and-Production-Labs-Work-FALL-2020-/blob/master/lab-04/index.html) file in browser (chrome/firefox/ie).
2. Open [index.html](https://github.com/expertofvision/ECS521-Interactive-Media-Design-and-Production-Labs-Work-FALL-2020-/blob/master/lab-04/index.html) files in a text editor.

## B. Text Processing
Write a program to count the vowels in a text.

1. Open [process_text.js](https://github.com/expertofvision/ECS521-Interactive-Media-Design-and-Production-Labs-Work-FALL-2020-/blob/master/lab-04/process_text.js) file in a text editor
2. Add both the button and textarea elements: <br/>
    &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; let btn = document.getElementById('count_btn'); <br/>
    &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; let txt_field = document.getElementById('input_txt'); <br/>
3. Go to the onlick event definition for the button. <br/>
    &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; btn.onclick = function() { <br/>
    &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; }; <br/>
4. Add the value typed on the text area. <br/>
    &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; let txt = txt_field.value; <br/>
5. Create an array that contains the vowels. This will be used later to check if a character in the text is a vowel. <br/> 
    &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; let vowels = ['a', 'e', 'i', 'o', 'u']; <br/>
6. Traverse the input text and check if each character is a vowel or not. If it is, increase the counter by one. <br/> 
    &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; for (let i = 0; i < txt.length; i++) { <br/>
    &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; if (vowels.includes(txt.charAt(i).toLowerCase())) { <br/>
    &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; count++; <br/>
    &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; } <br/>
    &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; } <br/>
7. Get the element where the result is going to be displayed. <br/> 
    &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; let result = document.getElementById('display_result'); <br/>
8. Set a new value to the previous element, reflecting the number of vowels present in the input text. <br/> 
    &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; result.innerHTML = 'Your input contains ' + count + ' vowels'; <br/>

## C. HTML5 Web Storage
1. HTML web storage; better than cookies.
2. With web storage, web applications can store data locally within the user's browser.
3. Before HTML5, application data had to be stored in cookies, included in every server request. Web storage is more secure, and large amounts of data can be stored locally, without affecting website performance.
4. Unlike cookies, the storage limit is far larger (at least 5MB) and information is never transferred to the server.
5. Web storage is per origin (per domain and protocol). All pages, from one origin, can store and access the same data.
6. HTML web storage provides two objects for storing data on the client:
    * window.localStorage - stores data with no expiration date
    * window.sessionStorage - stores data for one session (data is lost when the browser tab is closed)
Before using web storage, check browser support for localStorage and sessionStorage: <br/>
    &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; if (typeof(Storage) !== "undefined") { <br/>
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; // Code for localStorage/sessionStorage. <br/>
    &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; } else { <br/>
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; // Sorry! No Web Storage support.. <br/>
    &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; } <br/>

### The localStorage Object
The localStorage object stores the data with no expiration date. The data will not be deleted when the browser is closed, and will be available the next day, week, or year.
1. Open [last_name.html](https://github.com/expertofvision/ECS521-Interactive-Media-Design-and-Production-Labs-Work-FALL-2020-/blob/master/lab-04/last_name.html) in browser (chrome/firefox/ie).
2. Open [last_name.html](https://github.com/expertofvision/ECS521-Interactive-Media-Design-and-Production-Labs-Work-FALL-2020-/blob/master/lab-04/last_name.html) in text editor.
3. Add following statement for storing last name. <br/>
    &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; localStorage.setItem("lastname", "Bilal"); <br/>
4. Add following statement to retrieve last name. <br/>
    &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; document.getElementById("result").innerHTML = localStorage.getItem("lastname"); <br/>

### Comparing localStorage Object and sessionStorage Object
The sessionStorage object is equal to the localStorage object, except that it stores the data for only one session. The data is deleted when the user closes the specific browser tab.
1. Open [local_vs_session.html](https://github.com/expertofvision/ECS521-Interactive-Media-Design-and-Production-Labs-Work-FALL-2020-/blob/master/lab-04/local_vs_session.html) in browser (chrome/firefox/ie).
2. Open [local_vs_session.html](https://github.com/expertofvision/ECS521-Interactive-Media-Design-and-Production-Labs-Work-FALL-2020-/blob/master/lab-04/local_vs_session.html) in text editor.
3. Add following function for localStorage. Close and Open tab/window multiple times and notice counter value. <br/>
    &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; function clickCounter() { <br/>
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; if (typeof(Storage) !== "undefined") { <br/>
        &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; if (localStorage.clickcount) { <br/>
          &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; localStorage.clickcount = Number(localStorage.clickcount)+1; <br/>
        &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; } else { <br/>
          &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; localStorage.clickcount = 1; <br/>
        &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; } <br/>
        &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; document.getElementById("result").innerHTML = "You have clicked the button " + localStorage.clickcount + " time(s)."; <br/>
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; } else { <br/>
        &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; document.getElementById("result").innerHTML = "Sorry, your browser does not support web storage..."; <br/>
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; } <br/>
    &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; } <br/>

4. Comment function for localStorage and add following function for sessionStorage. Close and Open tab/window multiple times and notice counter value. <br/>
    &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; function clickCounter() { <br/>
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; if (typeof(Storage) !== "undefined") { <br/>
        &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; if (sessionStorage.clickcount) { <br/>
          &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; sessionStorage.clickcount = Number(sessionStorage.clickcount)+1; <br/>
        &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; } else { <br/>
          &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; sessionStorage.clickcount = 1; <br/>
        &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; } <br/>
        &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; document.getElementById("result").innerHTML = "You have clicked the button " + sessionStorage.clickcount + " time(s) in this session."; <br/>
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; } else { <br/>
        &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; document.getElementById("result").innerHTML = "Sorry, your browser does not support web storage..."; <br/>
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; } <br/>
    &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; } <br/>















