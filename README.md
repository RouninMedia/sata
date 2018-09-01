# sata

**sata** is a *Sequential Alternative to Ajax*

**sata** is a quick and easy (and *Ajax*-free) way to send data from a client-side script to be processed by a server-side script which then redirects the browser back to the originating URL (or to a new URL) with the server-side script's response.

Unlike *Ajax*, **sata** does not return a `.responseText` or `.responseXML`.

Instead, it can:

 - return a response as `localStorage` or `sessionStorage` in Javascript
 - return a response as a Session Variable in PHP
 - return a response as a URI query string containing a series of coded (or uncoded) key-value pairs
 - return a response as a cookie

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
document.body.removeChild(sataForm);
```
