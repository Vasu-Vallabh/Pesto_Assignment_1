## When a user enters an URL in the browser, how does the browser fetch the desired result? Explain this with the below in mind and Demonstrate this by drawing a diagram for the same.

## 1\. Main functionality of the browser

The main functionality of the browser is to serve the requested resource from the server and display it to the user. There are different forms of data the browser can show to a user. Mostly it is an HTML document, but the data can be PDF, Image, or some other data content type.  
The location of the resource can be specified by the user using a URI (Uniform Resource Identifier).  
The way the browser interprets and displays HTML files is specified in the HTML and CSS specifications. These specifications are maintained by W3C(World Wide Web Consortium) organization.

## **2\. Hight Level Components of a Browser**

**The Browser's main components are:**

1. The UI (User Interface)

UI includes the address bar, back/forward button, bookmarking menu, and a display where you see the requested page. 

2. **The Browser Engine**

It assembles and arranges actions between the UI and the rendering engine. 

3. **The Rendering Engine**

It is responsible for displaying the requested content.

The rendering engine parses the HTML and CSS and displays the parsed content on the screen/browser's display.

4. **Networking**

For network calls such as HTTP requests. It uses different implementations for different platforms behind a platform-independent interface.

5. **UI Backend**

It is for drawing basic widgets like Combo boxed and windows. It is not platform-specific. Underneath it uses OS (Operating system) UI methods.

6. **JavaScript Interpreter**

As the name suggests, it is for parsing and executing JS code.

7. **Data Storage**

It is a persistence layer for saving and storing data locally as cookies, session storage, local storage, etc.

![](https://user-images.githubusercontent.com/101351789/160363782-1ddaf12a-428f-4b2a-ba4c-ce20be2a62f2.png)

## 3. **Rendering Engine & its use**

The responsibility of the rendering engine is to display the requested page on the browser screen.

The browsers use different rendering engines.

a. Firefox -> Gecko

b. Safari -> WebKit

c. Chrome & Opera -> Blink (a fork of WebKit).

![](https://user-images.githubusercontent.com/101351789/160368334-12eaf79a-6b4d-4ed3-a5be-15d32c0cb2ca.png)

_Basic Flow of any Rendering Engine_
