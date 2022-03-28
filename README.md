# When a user enters an URL in the browser, how does the browser fetch the desired result? Explain this with the below in mind and Demonstrate this by drawing a diagram for the same.

# 1\. What is the main functionality of the browser?

The main functionality of the browser is to serve the requested resource from the server and display it to the user. There are different forms of data the browser can show to a user. Mostly it is an HTML document, but the data can be PDF, Image, or some other data content type.  
The location of the resource can be specified by the user using a URI (Uniform Resource Identifier).  
The way the browser interprets and displays HTML files is specified in the HTML and CSS specifications. These specifications are maintained by W3C(World Wide Web Consortium) organization.

**2\. Hight Level Components of a Browser.**

The Browser's main components are:

1. **The UI** (User Interface)

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

6. **JavaScript Interperter**

As the name suggests, it is for parsing and executing JS code.

7. **Data Storage**

It is a persistence layer for saving and storing data locally as cookies, session storage, local storage, etc.
