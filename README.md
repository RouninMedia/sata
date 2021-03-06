# sata

**sata** is a *Sequential Alternative to Ajax*

Like *Ajax*, **sata** is a *client to server to client* data transfer process.

At the time of writing, **sata** does not have any obvious advantages over *Ajax*

(But I would be delighted if I could think of a couple...)

_____

**sata** is a quick and easy alternative to *Ajax* which sends data from a client-side script to a server-side script. The server-side script then processes the data before sending the server-side script's response to the client and redirecting the browser back to the originating URL (or to a new URL).

_____

Unlike *Ajax*, **sata** does not return a `.responseText` or `.responseXML`.

Instead, it can ***C**reate, **R**ead, **U**pdate, **D**elete (CRUD)* the following:

 - a Session Variable in PHP
 - a cookie
 - `localStorage` or `sessionStorage` in Javascript
 - a URI query string containing a series of coded (or uncoded) key-value pairs

_____

# Standard Approach (using a FormData Object and Ajax)

```
var myAjaxForm = new FormData();
myAjaxForm.append('ajax-data-1', 'Some other data here');
myAjaxForm.append('ajax-data-2', 'Some other data here');

var myAjaxXHR = new XMLHttpRequest();
myAjaxXHR.open('POST', '/server-side-script.php', true);
myAjaxXHR.send(myAjaxForm);

```
_____

# Sata (using a dynamically-built HTML Form)

```
var sataForm = document.createElement('form');
sataForm.setAttribute('method', 'post');
sataForm.setAttribute('action', '/server-side-script.php');

var sataData1 = document.createElement('input');
sataData1.setAttribute('type', 'hidden');
sataData1.setAttribute('name', 'sata-data-1');
sataData1.setAttribute('value', 'Some data here');
checkAccountStatusForm.appendChild(sataData1);

var sataData2 = document.createElement('input');
sataData2.setAttribute('type', 'hidden');
sataData2.setAttribute('name', 'sata-data-2');
sataData2.setAttribute('value', 'Some other data here');
checkAccountStatusForm.appendChild(sataData2);

document.body.appendChild(sataForm);
sataForm.submit();
```
