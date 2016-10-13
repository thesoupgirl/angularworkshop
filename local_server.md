# Local Server

To see what the web application looks like (aside from the code), we'll need a server.  A very simple way to locally host it is to use Python's server.  To use it, you'll need to make sure you have Python on your computer.  

To check if you have Python on your computer...
For Mac/Linux:
Open up the Terminal app (for Mac) or a command line (for Linux) and type the following: ```python --version```

If it doesn't tell you what version of Python you're running, then you'll need to download it...

Download Python using [this](https://www.python.org/downloads/).  (You can skip this step if you already have Python.)

Now that you have Python, we can run our local server using this command line command here:  ```python -m SimpleHTTPServer 8000```
*Note:  Make sure you do so in whatever directory that holds your code.  If you downloaded the zip file, it'll most likely be called angularworkshop-master.*

Now you can few your site by going to localhost:8000 in your browser!

*Note:  This defaults to your index.html (if it can be found) within the directory that you issued the Python server command.  If you wish to specifically see a page, you can do localhost:8000/index.html (replacing index.html with whatever page you wish to view).*

To stop running the server, use the shortcut keys `control + c`.