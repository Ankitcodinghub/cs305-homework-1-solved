# cs305-homework-1-solved
**TO GET THIS SOLUTION VISIT:** [CS305 Homework 1 Solved](https://www.ankitcodinghub.com/product/cs305-solved-3/)


---

📩 **If you need this solution or have special requests:** **Email:** ankitcoding@gmail.com  
📱 **WhatsApp:** +1 419 877 7882  
📄 **Get a quote instantly using this form:** [Ask Homework Questions](https://www.ankitcodinghub.com/services/ask-homework-questions/)

*We deliver fast, professional, and affordable academic help.*

---

<h2>Description</h2>



<div class="kk-star-ratings kksr-auto kksr-align-center kksr-valign-top" data-payload="{&quot;align&quot;:&quot;center&quot;,&quot;id&quot;:&quot;124333&quot;,&quot;slug&quot;:&quot;default&quot;,&quot;valign&quot;:&quot;top&quot;,&quot;ignore&quot;:&quot;&quot;,&quot;reference&quot;:&quot;auto&quot;,&quot;class&quot;:&quot;&quot;,&quot;count&quot;:&quot;2&quot;,&quot;legendonly&quot;:&quot;&quot;,&quot;readonly&quot;:&quot;&quot;,&quot;score&quot;:&quot;5&quot;,&quot;starsonly&quot;:&quot;&quot;,&quot;best&quot;:&quot;5&quot;,&quot;gap&quot;:&quot;4&quot;,&quot;greet&quot;:&quot;Rate this product&quot;,&quot;legend&quot;:&quot;5\/5 - (2 votes)&quot;,&quot;size&quot;:&quot;24&quot;,&quot;title&quot;:&quot;CS305 Homework 1 Solved&quot;,&quot;width&quot;:&quot;138&quot;,&quot;_legend&quot;:&quot;{score}\/{best} - ({count} {votes})&quot;,&quot;font_factor&quot;:&quot;1.25&quot;}">

<div class="kksr-stars">

<div class="kksr-stars-inactive">
            <div class="kksr-star" data-star="1" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="2" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="3" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="4" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="5" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>

<div class="kksr-stars-active" style="width: 138px;">
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>
</div>


<div class="kksr-legend" style="font-size: 19.2px;">
            5/5 - (2 votes)    </div>
    </div>
MDN docs

RFC9110: HTTP Semantics

RFC7230 : HTTP/1.1 Message Syntax and Routing

Chapter 3 : Message Format

Chapter 6 : Connection Management RFC7231 : HTTP/1.1 Semantics and Content

Chapter 4 : Request Methods

Chapter 6 : Response Status Codes

Only 200, 300, 301, 400, 404 RFC7232 : HTTP/1.1 Conditional Requests

RFC7233 : HTTP/1.1 Range Requests RFC7234 : HTTP/1.1 Caching

If you are confused about syntax in RFCs, you can try to read the Syntax Notation chapter of each RFC. Here are some instances for that notation.

SP: whitespace

CRLF: ‘ ‘

Tips: About how to read RFC, here is an article about it. How to Read RFC

Tasks

Task 1: HTTP Message encapsulation and de-encapsulation (20 pts)

In task1, you need to complete the code in the framework, and directly manipulate of binary data and sockets to handle HTTP messages.

The methods that need to complete:

framework.py -&gt; class HTTPResponse -&gt; write_all() class HTTPRequest -&gt; read_headers().

After finishing this part, you can use curl to test your HTTP server.

Run the server with command python3 main.py and run curl -v

http://127.0.0.1:8080 in a new terminal. After that, you should get 404 Not Found as intended.

To simplify the implementation of the HTTP server, we add header Connection: close to require clients not to reuse TCP connections.

$ curl -v http://127.0.0.1:8080/ * Trying 127.0.0.1:8080…

* Connected to 127.0.0.1 (127.0.0.1) port 8080 (#0)

&gt; GET / HTTP/1.1

&gt; Host: 127.0.0.1:8080

&gt; User-Agent: curl/7.85.0 &gt; Accept: */*

&gt;

* Mark bundle as not supporting multiuse

&lt; HTTP/1.1 404 Not Found &lt; Connection: close

&lt;

* Closing connection 0

At last, we provide the unit-test TestTask1.py for you to check your implementation.

Task 2: Basic Static Content Server (20 pts)

In task 2, you are required to write handler to serve local files when clients GET for any files under /data/.

For example, if clients GET for http://127.0.0.1:8080/data/index.html, the server should respond with the content of file data/index.html . If clients GET for a nonexistence file, such as http://127.0.0.1:8080/data/nosuchfile, the server should respond HTTP 404 Not Found.

You should reject the POST requests of them, and respond properly to GET and HEAD requests. Also, you should set the Content-Type and Content-Length in Response Headers properly.

Task 3: Handle POST Request (20 pts)

&gt; User-Agent: curl/7.85.0

&gt; Accept: */*

&gt; Content-Length: 18

&gt; Content-Type: application/x-www-form-urlencoded

&gt;

* Mark bundle as not supporting multiuse

&lt; HTTP/1.1 200 OK

&lt; Connection: close

&lt;

* Closing connection 0

$ curl -v http://127.0.0.1:8080/post –get * Trying 127.0.0.1:8080…

* Connected to 127.0.0.1 (127.0.0.1) port 8080 (#0)

&gt; GET /post HTTP/1.1

&gt; Host: 127.0.0.1:8080

&gt; User-Agent: curl/7.85.0 &gt; Accept: */*

&gt;

* Mark bundle as not supporting multiuse

&lt; HTTP/1.1 200 OK

&lt; Connection: close &lt; Content-Type: application/json

&lt; Content-Length: 16

&lt;

* Closing connection 0

{“data”: “test”}

At last, we provide the unit-test TestTask3.py for you to check your implementation.

Task 4: HTTP 302 Found: URL Redirection (10 pts)

If you are not so familiar with what Redirection is, please refer to this document. https://d eveloper.mozilla.org/en-US/docs/Web/HTTP/Redirections.

URL Redirection is used to redirect browsers to another URL. The HTTP Server should set status code to 30x and set the Location attribute in Header.

After implementation, when the client GETs/HEADs http://127.0.0.1:8080/redirect, the HTTP server generates 302 and redirects to

http://127.0.0.1:8080/data/index.html.

Curl Result

$ curl -v http://127.0.0.1:8080/redirect * Trying 127.0.0.1:8080… * Connected to 127.0.0.1 (127.0.0.1) port 8080 (#0)

&gt; GET /redirect HTTP/1.1

&gt; Host: 127.0.0.1:8080

&gt; User-Agent: curl/7.85.0 &gt; Accept: */*

&gt;

* Mark bundle as not supporting multiuse

&lt; HTTP/1.1 302 Found

&lt; Connection: close

&lt; Location: http://127.0.0.1:8080/data/index.html

&lt;

* Closing connection 0

At last, we provide the unit-test TestTask4.py for you to check your implementation.

Task 5: HTTP Cookie and Session (30 pts)

If you are not so familiar with what Cookie is, please refer to this document.https://develo per.mozilla.org/en-US/docs/Web/HTTP/Cookies

In task 5, you are required to protect a image file that only authenticated users can access.

In the first step, the client will POST their credential to a login API, you should verify it and mark them as authenticated or not. Since HTTP protocol is stateless, Cookie is used to keep the state of clients.

In the second step, the client will request the protected image with Cookie set by server in the first step, you should only respond the protected image to authenticated client.

In this part, you don’t need to care CORS problem, and you can just ignore Domain, Path attributes in Cookie.

Cookie (15 pts)

After receiving an HTTP request, a server can send one or more Set-Cookie headers with the response. After receiving the cookie, browser usually stores the cookie and sends it with requests made to the same server inside a Cookie HTTP header.

Step 1. Login Authentication

The client will POST http://127.0.0.1:8080/api/login with the following json structure, the server should verify whether the username and password are equal to admin, admin.

{“username”:”admin”, “password”:”admin”}

If they are equal, the server should return HTTP 200 OK and set cookie Authenticated=yes. Otherwise, it should return HTTP 403 Forbidden.

To simplify code, we could ignore any other attributes of Cookie.

Step 2. Access Protected Resources

The client will GET/HEAD http://127.0.0.1:8080/api/getimage.

If the client authorizes in Step1, it requests this URL with Cookies specified in the last Response, i.e., the Authenticated field in Request Cookie should be yes.

If the Authenticated field is yes, the server should return the image data/test.jpg and set Content-Length and Content-Type properly. Otherwise, if the Authenticated Cookie doesn’t exist or isn’t yes, it should return HTTP 403 Forbidden.

You should pass unittest TestTask5Cookie.py if you implement this part properly. You can also open http://127.0.0.1:8080/api/test in browser to test.

Curl Result

$ curl -v http://127.0.0.1:8080/api/login –data

‘{“username”:”admin”, “password”:”admin”}’ * Trying 127.0.0.1:8080…

* Connected to 127.0.0.1 (127.0.0.1) port 8080 (#0)

&gt; POST /api/login HTTP/1.1

&gt; Host: 127.0.0.1:8080

&gt; User-Agent: curl/7.85.0

&gt; Accept: */*

&gt; Content-Length: 40

&gt; Content-Type: application/x-www-form-urlencoded

&gt;

* Mark bundle as not supporting multiuse

&lt; HTTP/1.1 200 OK

&lt; Connection: close

&lt; Set-Cookie: Authenticated=yes

&lt;

* Closing connection 0

$ curl -v http://127.0.0.1:8080/api/getimage * Trying 127.0.0.1:8080…

* Connected to 127.0.0.1 (127.0.0.1) port 8080 (#0)

&gt; GET /api/getimage HTTP/1.1

&gt; Host: 127.0.0.1:8080

&gt; User-Agent: curl/7.85.0 &gt; Accept: */*

&gt;

* Mark bundle as not supporting multiuse

&lt; HTTP/1.1 403 Forbidden

&lt; Connection: close

&lt;

* Closing connection 0

$ curl -v http://127.0.0.1:8080/api/getimage –header “Cookie:

Authenticated=yes” * Trying 127.0.0.1:8080…

* Connected to 127.0.0.1 (127.0.0.1) port 8080 (#0)

&gt; GET /api/getimage HTTP/1.1

&gt; Host: 127.0.0.1:8080

&gt; User-Agent: curl/7.85.0

&gt; Accept: */* &gt; Cookie: Authenticated=yes

&gt;

* Mark bundle as not supporting multiuse

&lt; HTTP/1.1 200 OK

&lt; Connection: close

&lt; Content-Length: 44438

&lt; Content-Type: image/jpeg

&lt;

* Closing connection 0

After that, you should pass unit-test TestTask5Cookie.py. You can open http://127.0.0.1:8080/api/test in browser to play with your server.

Session (15 pts)

The authentication method in the above method is not secure, a malicious client can access the protected resources by just setting the cookie Authenticated=yes without knowing the real username and password credential.

To implement a session, the server initializes a dictionary, which uses a random string as a key, and stores data in the dictionary that is not accessible to clients.

The server will set this random string as session key in response’s Set-Cookie, the client will bring the given cookie in future requests, and the server will find the stored data via the key in Cookie.

Step 1. Login Authentication

The client POSTs http://127.0.0.1:8080/apiv2/login with the following json structure, The server should verify whether both the username and password are equal to

admin.

{“username”:”admin”, “password”:”admin”}

If they are equal, the server should generate a random string as SESSION_KEY, and make sure it’s unique in stored session keys. The server should return HTTP 200 OK and set cookie SESSION_KEY=&lt;random string&gt;. Otherwise, it should return HTTP 403 Forbidden.

Step 2. Access Protected Resources

The client will GET/HEAD http://127.0.0.1:8080/apiv2/getimage with or without SESSION_KEY in Cookies.

If the client authorizes successfully in Step1, it requests this URL with Cookies included in the last response.

If the SESSION_KEY field exists and server recognizes it as valid, the server should return the image data/test.jpg and set Content-Length and Content-Type properly. Otherwise, the server should return HTTP 403 Forbidden.

You should pass unit-test TestTask5Session.py if you implement this part properly. You can also open http://127.0.0.1:8080/apiv2/test in browser to test.

Curl Result

$ curl -v http://127.0.0.1:8080/apiv2/getimage * Trying 127.0.0.1:8080…

* Connected to 127.0.0.1 (127.0.0.1) port 8080 (#0)

&gt; GET /apiv2/getimage HTTP/1.1

&gt; Host: 127.0.0.1:8080

&gt; User-Agent: curl/7.85.0 &gt; Accept: */*

&gt;

* Mark bundle as not supporting multiuse

&lt; HTTP/1.1 403 Forbidden

&lt; Connection: close

&lt;

* Closing connection 0

$ curl -v http://127.0.0.1:8080/apiv2/login –data ‘{“username”:”admin”, “password”:”admin”}’ * Trying 127.0.0.1:8080…

* Connected to 127.0.0.1 (127.0.0.1) port 8080 (#0)

&gt; POST /apiv2/login HTTP/1.1

&gt; Host: 127.0.0.1:8080

&gt; User-Agent: curl/7.85.0

&gt; Accept: */*

&gt; Content-Length: 40

&gt; Content-Type: application/x-www-form-urlencoded

&gt;

* Mark bundle as not supporting multiuse

&lt; HTTP/1.1 200 OK

&lt; Connection: close &lt; Set-Cookie: SESSION_KEY=DJK5LAFTY8NEQN6JNRIA

&lt;

* Closing connection 0

$ curl -v http://127.0.0.1:8080/apiv2/getimage –header “Cookie:

SESSION_KEY=DJK5LAFTY8NEQN6JNRIA” * Trying 127.0.0.1:8080…

* Connected to 127.0.0.1 (127.0.0.1) port 8080 (#0)

&gt; GET /apiv2/getimage HTTP/1.1

&gt; Host: 127.0.0.1:8080

&gt; User-Agent: curl/7.85.0

&gt; Accept: */*

&gt; Cookie: SESSION_KEY=DJK5LAFTY8NEQN6JNRIA

Run &gt;

* Mark bundle as not supporting multiuse

&lt; HTTP/1.1 200 OK

&lt; Connection: close

&lt; Content-Length: 44438

&lt; Content-Type: image/jpeg

&lt;

* Closing connection 0

At last, we also provide the unit-test TestTask5Session.py for you to check your implementation in this part. Please notice that, the test files in the /data directory will be different in our testing environment.

You can open http://127.0.0.1:8080/apiv2/test in browser to play with your server.

How to run the code

Server

python main.py in the root directory of the project, then run curl -v

http://127.0.0.1:8080 in new terminal.

Unit Test

VSCode

Run python -m unittest tests.TestTask1 in the root directory of the project to execute TestTask1.py .

For other tests, the execution commands are similar.

PyCharm

Go to the root directory of the assignment, then execute tests.

What to submit

You must provide a zip file of your implementation, including main.py, framework.py and other files if needed.

A PDF file that includes some necessary screenshots to show your code works and some brief explanations.

Score

The score of your assignment will be determined by an extended set of given unittests. You can use the given unittests to check the correctness of your implementation. But you still might not get 100 points, even if you pass all the given unittests.

ATTENTION!!!

Please modify YOUR_STUDENT_ID = 12010000 to your SID in main.py, this field is used in automated testing. Otherwise, SAs will be painful to handle your submission.

Score Environment

Please notice that your code will eventually be tested and scored on a platform based on the following environments.

Python 3.9

LIB LIMITATION: You can only use The Python Standard Library, excluding the http module.

Dockerfile to build the test environment (You don’t need to build this environment locally):

FROM python:3.9-bullseye

RUN apt update &amp;&amp; apt install -y curl RUN pip3 install requests

VOLUME /score

WORKDIR /score

CMD [“/bin/bash”, “-c”, “python3 -m tests.TestAll &gt;result.txt

2&gt;stderr.txt”]

# Build : docker build . -t ass1

# Run : docker run -v $PWD:/score -it ass1:latest

Q&amp;A Link

If you have any question about this assignment, please go to the link above to raise your question. And we will check and reply in time.

https://github.com/yuk1i/cs305-2022fall-homework1-student/issues

Enjoy yourselves!
