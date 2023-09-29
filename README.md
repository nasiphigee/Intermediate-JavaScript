# Intermediate-JavaScript-Week-1
DAY 1
Popups and Window Methods

Popups and window methods
A popup window is one of the oldest methods to show additional document to user.

Basically, you just run:

window.open('https://javascript.info/')

…And it will open a new window with given URL. Most modern browsers are configured to open url in new tabs instead of separate windows.

Popups exist from really ancient times. The initial idea was to show another content without closing the main window. As of now, there are other ways to do that: we can load content dynamically with fetch and show it in a dynamically generated <div>. So, popups is not something we use everyday.

Popups Blocking 

Most browsers block popups if they are called outside of user-triggered event handlers like onclick.
For example:
// popup blocked
window.open('https://javascript.info');

// popup allowed
button.onclick = () => {
window.open('https://javascript.info');
};

CLOSING POPUPS 
The window.close() method is technically available for any window, but git clone is ignored by the majority of the browsers in case the window is not created using window.open() . So, that will operate only on a popup.

Window.open 

Window.open()
It is a pre-defined window method of JavaScript used to open the new tab or window in the browser. This will depend on your browser setting or parameters passed in the window.open() method that either a new window or tab will open.

Syntax:
This function accepts four parameters, but they are optional.
window.open(URL, name, specs, replace);
Or
You can also use this function without using the window keyword as shown below:
open(URL, name, specs, replace)

FOCUS/ BLUR ON A WINDOW 
Consider the following code:

window.onblur = () => window.focus();
When the user tries to switch out of the window (blur), it returns the focus. The aim “locking” the user inside the window. But, the existing limitations forbid such a code. It mostly depends on the browser.

DAY 2
SAME ORIGIN
The term "Same Origin" refers to a security concept in web development and browsing. It's a fundamental policy enforced by web browsers to ensure the security and privacy of users when interacting with web pages and web applications.

The Same Origin Policy (SOP) dictates that web pages can only make requests to resources on the same origin as the original web page. An origin is defined by the combination of three components:

Scheme: This is the protocol used, such as HTTP or HTTPS.
Host: This is the domain name of the server hosting the resource.
Port: This is the port number on the server (usually omitted and assumed to be the default HTTP or HTTPS port).

Windows on subdomains: document.domain

 The document.domain property is a security feature in web browsers that allows you to relax the Same Origin Policy (SOP) for communication between windows or iframes of different subdomains of the same parent domain. `
It can be used to enable cross-origin communication between web pages or iframes that share the same parent domain but have different subdomains.

Iframe: wrong document pitfall

Suppose you have two subdomains, sub1.example.com and sub2.example.com, and you want to enable cross-origin communication between them using document.domain. 




