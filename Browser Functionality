## When a user enters an URL in the browser, how does the browser fetch the desired result? Explain this with the below in mind and Demonstrate this by drawing a diagram for the same.

## 1\. Main functionality of the browser

The main functionality of the browser is to serve the requested resource from the server and display it to the user. There are different forms of data the browser can show to a user. Mostly it is an HTML document, but the data can be PDF, Image, or some other data content type.  
The location of the resource can be specified by the user using a URI (Uniform Resource Identifier).  
The way the browser interprets and displays HTML files is specified in the HTML and CSS specifications. These specifications are maintained by W3C(World Wide Web Consortium) organization.

## **2\. Hight Level Components of a Browser**

**The Browser's main components are:**

1. **The UI (User Interface)**

UI includes the address bar, back/forward button, bookmarking menu, reloading button, and a display where you see the requested page. 

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

_**Figure: The Basic Flow of  a Rendering Engine.**_

![](https://user-images.githubusercontent.com/101351789/160368915-f92ee8cc-0f1e-491c-87ef-d57c3e5bd3bc.png)

_**Figure: The main flow of WebKit Rendering Engine.**_

## 4\. Parser(HTML & CSS etc.)

Parsing means analyzing and converting a program into an internal format that a runtime environment can actually run, for example, the JavaScript engine inside browsers.

The browser parses HTML into a DOM tree, HTML parsing involves tokenization and tree construction. If the document is well-formed, parsing it is straightforward and faster.

When the HTML parser finds non-blocking resources, such as an image, the browser will request those and continue parsing but `<script>` tags--particularly those without an `async` or `defer` attribute—blocks rendering, and pauses parsing of HTML. 

**CSS Parsing**

When the browser encounters CSS styles, it parses the text into the CSS Object Model (CSSOM), a data structure. It then uses for styling layouts and painting. The browser then creates a render tree from both these structures to be able to paint the content to the screen. 

![](https://user-images.githubusercontent.com/101351789/160385803-e5f77df9-5635-4045-909e-eb9a112b470b.png)

## Script Processor

The model of the web is synchronous. Authors expect scripts to be parsed and executed immediately when the parser reaches a \<script> tag. The parsing of the document halts until the script has been executed. If the script is external then the resource must first be fetched from the network–this is also done synchronously, and parsing halts until the resource is fetched. This was the model for many years and is also specified in HTML4 and 5 specifications. Authors can add the "defer" attribute to a script, in which case it will not halt document parsing and will execute after the document is parsed. HTML5 adds an option to mark the script as asynchronous so it will be parsed and executed by a different thread.

## Tree Construction

The first step is processing the HTML and building DOM(Document Object Model). The DOM tree describes the content of the document. The The `<html>` element is the first tag and root node of the document tree. The tree reflects the relationship and hierarchies between different tags. Tags nested within other tags are child nodes. The greater the number of DOM nodes, the longer it take to construct the DOM tree.

![](https://user-images.githubusercontent.com/101351789/160390787-bec22a22-0ab4-41d3-b821-6a54c971dda0.gif)

**Preload Scanner**

While the browser builds the DOM tree, this process occupies the main thread. As this happens, the preload scanner will parse through the content available and also request for the high priority resource like CSS, JavaScript, and web fonts. It will retrieve the resources in the background so that by the time the main HTML parser reaches the requested asset, they may possibly already be in flight, or have been downloaded. The optimizations the preload scanner provides reduce blockages. 

**Building the CSSOM**

The second step is processing CSS and building CSSOM tree. The CSS object model is similar to DOM. The DOM and CSSOM are both trees. They are independent data structures. The browser converts the CSS rules into a map of styles it can understand and work with. The browser goes through each rule set in the CSS, creating a tree of nodes with parent, child, and sibling relationships based on the CSS selectors.

Building the CSSOM is very, very fast and is not displayed in a unique colour in current developer tools.
