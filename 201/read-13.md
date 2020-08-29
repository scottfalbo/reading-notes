## 201 Read-13. Local Storage
[Local Storage for Web Apps](http://diveinto.html5doctor.com/storage.html)

### HTML 5 Storage
> HTML 5 storage is a way for web pages to store named kay/value pairs locally, within the client web browser.  Like cookies the data persists even after you navigate away from the site, or close your browser.
Unlike cookies this data is never transmitted to the remote web server.

+ Check to see if the browser allows local storage.
  + `if (!supportsLocalStorage()) { return false; }`

+ Store: `localStorage.setItem('name', 'value');`
+ Retrieve: `document.getElementById('elementId').innerHTML = localStorage.getItem('name');`
  + Remove: `localStorage.removeItem('name');
+ *name/value pairs are stored as a string and need to be coerced into other types.*

+ `sessionStorage` acts the same as `localStorage` but only holds the data for one session.  When the tab is closed the data is removed.

#### tracking Changes to HTML5 Storage Area
+ To track storage area changes you can **trap** the **storage event**.  The storage event is included everywhere the `localStorage` object is supported.  
  + The `Storage Event` holds:
    + `key` the named key that was added, removed or modified.
    + `oldValue` the previous, now overwritten, value.
    + `newValue` the new value.
    + `url` the page that called the method which triggered the change.




[Back to the main page](../README.md) 
