# url-shortener-ui

[Reference Website](https://s.dsce.in/), i.e, make it work like this.

The above website is the official URL Shortener of Dayananda Sagar College of Engineering which is under active developement right now under @AmanL04.

## Input fields shown for various options

Option Chosen | Selector Name | Changes to be made
------------- | ------------- | ------------------
New | #passwordUrl | Placeholder-> Enter Password
New | #shortUrl | Placeholder-> Enter Desired Short URL
New | #longUrl | Placeholder-> Enter Long URL
New | #submitUrl | Text-> Shorten URL
New | #new-update-search-url .horizontal-divider h3 | Text-> Optional Fields
New | #current-option span | Text-> Shorten New URL
--- | --- | ---
Update | #passwordUrl | Placeholder-> Enter Old Password
Update | #shortUrl | Placeholder-> Enter Old Short URL
Update | #longUrl | Placeholder-> Enter New Long URL
Update | #submitUrl | Text-> Update URL
Update | #new-update-search-url .horizontal-divider h3 | Text-> Credentials
Update | #current-option span | Text-> Update Existing Short URL
--- | --- | ---
Search | #longUrl | Placeholder-> Key to Search
Search | #submitUrl | Text-> Search
Search | #current-option span | Text->  Search from Existing URLs

## TO DO List (to make the front-end interactive)

1.  Add click event listener to **_#hamburger input_**. The callback function should:
    1.  Remove class ___show___ from **_#search-result_**
    2.  Toggle class ___checked___ to **_#hamburger-menu ul_** based on the condition "_e.target.checked == true_"

    **OUTCOME**- On clicking the hamburger menu on the top right, the menu opens.

2.  Add click event listener to each li selected by **_#hamburger-menu li_**. The callback function should: 
    1.  Store innerText of the e.target in lowercase in a variable named **option** \[e.target.innerText.toLowerCase()\].
    2.  Remove class **_checked_** from the parent element of the target.
    3.  Make className property of element with id **_#new-update-search-url_** equal to **option**.
    4.  Make className property of element with id **_#new-update-result_** equal to **option**.
    5.  Make value of element with id **_#shortenedResult_** as **empty string**.
    6.  Make checked property of element with selector **_#hamburger input_** as **false**.
    7.  Make value of **all input fields** in the form **empty string**. (Search and learn how to do).
    8.  Paste this code (inside the callback function only)
        ```javascript
        switch(option){
          case "new": newUrlFn();break;
          case "update": updateUrlFn();break;
          case "search": searchUrlFn();break;
        }
        ```
    9.  Outside the callback function define these 3 functions
        ```javascript
        function newUrlFn(){
          // Some code
        }
        function updateUrlFn(){
          // Some code
        }
        function searchUrlFn(){
          // Some code
        }

        // Some code - This you should think and do.
        // Hint 1: Change placeholder values of the input fields according to the option.
        // Hint 2: Show/Hide certain input fields based on the chosen option (Mentioned at the start).
        ```

      **OUTCOME** - On clicking anyone of the menu options, accordingly the form will change.

## MORE TASKS WILL BE ADDED SOON TO MAKE THIS A FULLY FUNCTIONAL APPLICATION.