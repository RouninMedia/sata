# sata

**sata** is a *Synchronous Alternative to Ajax*

**sata** is a quick and easy (and *Ajax*-free) way to send data from a client-side script to be processed by a server-side script which then redirects the browser to a URL which contains the server-side script's response.

Unlike *Ajax*, **sata** returns a response in the URI as a series of coded or uncoded key-value pairs in the URL, rather than returning a `.responseText` or `.responseXML`.

# Sata (using dynamically generated HTML Form)

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
