# AJAX Chat

The goal of this project is to create an online chat service using
AJAX, Bootstrap, PHP and MySQL.

## How To

Belove are the steps to follow to create an awesome chat:

1. create `index.html` with at least:
    - a `div` to display the messages
    - a `form` to colect user input with a least:
        - an `input` to get the message
        - a `button` to submit the form
2. add a `script` element to `index.html` which:
    - register an event on the `form` submisson
    - stop the event default action (`preventDefault`)
    - read user message from the `input`
    - send the message using AJAX to `new-message.php`
3. create a page `new-message.php` which:
    - read an incoming message from `$_POST`
    - create a `Message` object with at least two properties: `content` and `time`
    - echo the message content
4. since we looooove MVC, let's edit `index.html`:
    - add a new Javascript array to store `messages`
    - make sure that when the user submit a new `message` an object is added to `messages`
    - create a function `displayMessages` wich update the `div` with the content of `messages`
    - call `displayMessages` each time you add an element to the array
5. now that we are MVC proof, we will connect `new-message.php` to the database:
    - create a file `ajax-chat.sql` in which you __MUST__ save all your SQL request
    - create a new database call `ajax-chat`
    - create a new database user `ajax-chat-user` wich can only access to the `ajax-chat` database
    - create a `message` table in the database, the message must at least have: a timestamp and a text.
    - connect `new-message.php` to the `ajax-chat` database
    - insert the message in the database
6. _More is comming!_

