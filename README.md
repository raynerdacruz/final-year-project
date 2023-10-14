**Note:**
- This project was built using Python 3.8, so to be on the safe side it would be best to have this version of Python installed or anything above Python 3.8.
- If you have only one version of python installed then you can use the prefix "python" instead of "py -3" for the commands below, however using the latter should do no harm.
- After you've entered the virtual environment all commands start with the prefix "python" instead of "py -3", as the virutal environment only has one version of Python available.

---


## Instructions for setting up the development environment and running the Django project.

<br>

**1. Create the Virtual Environment & Install the dependencies for the Django project**\
&nbsp;&nbsp;&nbsp;&nbsp;1.1 Open up your preferred terminal program. *The [ path | directory ] where the terminal program opens does not matter.*

&nbsp;&nbsp;&nbsp;&nbsp;1.2 Install the pipenv package if it is not already installed using the pip utility that ships with Python.

> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**Command:** `py -3 -m pip install pipenv`

**2. Create the Virtual Environment & Install the dependencies for the Django project**\

&nbsp;&nbsp;&nbsp;&nbsp;2.1 After the pipenv package is installed. In the terminal program CD into the Django project folder /Back-End wherever it may be located on your filesystem. You will need to use the absolute path of this folder | directory.

&nbsp;&nbsp;&nbsp;&nbsp;2.2 Relative to the /Back-End folder run the command to create a virtual environment & dependencies specific for this project folder.

> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**Command:** `py -3 -m pipenv install`

&nbsp;&nbsp;&nbsp;&nbsp;Note: During the dependency installation you might get 2 warnings saying that the msvc-runtime and pygraphviz could not be installed. You can safely ignore them as those dependencies are not used within the web application.

**3. Activate | Enter  the Virtual Environment**\
&nbsp;&nbsp;&nbsp;&nbsp;3.1 To activate | enter the virtual environment, run the following command relative to the /Back-End folder.

> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**Command:** `py -3 -m pipenv shell`

**4. Run the development web server**\
&nbsp;&nbsp;&nbsp;&nbsp;4.1 To run the development web server first CD one level down into the /lrebs folder.

> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**Command:** `cd ./lrebs/`

&nbsp;&nbsp;&nbsp;&nbsp;4.2 Now you can run the command to launch the development web server.

> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**Command:** `python manage.py runserver 0.0.0.0:8000`

**5. Test the LREBS web application**\
&nbsp;&nbsp;&nbsp;&nbsp;5.1 Open up your preferred web browser and type *127.0.0.1:8000/* in the URL box.\
&nbsp;&nbsp;&nbsp;&nbsp;5.2 You will be asked to login. The login credentials are \[eradicated\]:\[erdicated].\
&nbsp;&nbsp;&nbsp;&nbsp;5.3 Once logged in, you will be able to use the web application.

**6. Manage data in the database using the Django Admin web application**\
&nbsp;&nbsp;&nbsp;&nbsp;You can manage the data in the database through the Django Admin web app.

&nbsp;&nbsp;&nbsp;&nbsp;6.1 To access the Django admin web app head over to URL: 127.0.0.1:8000/admin. *Note: If you have already logged in to the LREBS web app you wont need to login again.*\
&nbsp;&nbsp;&nbsp;&nbsp;6.2 The login credentials for LREBS are \[eradicated\]:\[eradicated\].\
&nbsp;&nbsp;&nbsp;&nbsp;6.3 Once logged in, you will see the tables of the Admin web app as well as the LREBS web app. You can click on each table to explore the data within that table.

**Note**
- Step 1 only needs to be run once when you first download the source code files.
- You can stop the development web server by simply using the keyboard interrupt CTRL+C or by terminating | closing the terminal program.
- If at any point you close the terminal program this will result in terminating the development web server and you will also exit the virtual environment.
- To run the development server again you need to perform steps 2 and 3 (in that order).
<br>

---

## Instructions for setting up the development environment and running the notification script.

<br>

**1. Create the Virtual Environment & Install the dependencies for the Notification System project folder: Notification-System**\
&nbsp;&nbsp;&nbsp;&nbsp;1.1 In the terminal program, CD into the Django project folder /Notification-System wherever it may be located on your filesystem. You will need to use the absolute path of this folder.\
&nbsp;&nbsp;&nbsp;&nbsp;1.2 Relative to the /Notification-System folder run the command to create a virtual environment & install the dependencies specific for this project folder.

> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**Command:** `py -3 -m pipenv install`

**2. Activate | Enter the Virtual Environment**\
&nbsp;&nbsp;&nbsp;&nbsp;2.1 To enter the virtual environment run the following command relative to the /Back-End folder.

> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**Command:** `py -3 -m pipenv shell`

**3. Run the Notification Script**\
&nbsp;&nbsp;&nbsp;&nbsp;3.1 To run the notification script run the following command relative to the /Notification-System folder.

> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**Command:** `python ./notifications_non_multi-threaded.py`


**Note:**
- Step 1 only needs to be run once when you first download the source code files.
- For the notification script to "send out" notifications, as in write notification to the log file, there must be upcoming bookings present in the database related to LREBS web application. You can create the bookings through the LREBS web application.