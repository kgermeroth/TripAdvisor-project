# PopWatch

## Table of Contents

* [Summary](#summary)
* [Tech Stack](#tech-stack)
* [Features](#features)
* [Setup/Installation](#setup)

## <a name="summary"></a>Summary
**PopWatch** is an easy-to-use tool for hoteliers to track TripAdvisor ranking, average score, and number of reviews for an unlimited number of user-defined competitive sets.

## <a name="tech-stack"></a>Tech Stack
__Front End:__ HTML5, Jinja2, CSS, JavaScript, AJAX, React, Bootstrap, chart.js<br/>
__Back End:__ Python, Flask, PostgreSQL, SQLAlchemy <br/>

## <a name="features"></a>Features

Log in to create as many views of hotels (aka competitive sets, or comp sets for short!) as desired:

![Create Set](/static/videos/createset4.gif)
<br/><br/><br/>

Once at least one set is created, visit the Dashboard page to see data in chart format. Just click the inputs to change the chart!
![Dashboard](/static/videos/dashboard.gif)
<br/><br/><br/>

You can even download the data as csv to manipulate on your own:
![csv](/static/videos/downloadcsv.png)
<br/><br/><br/>

If you want to modify a comp set you created, head on over to the Manage Existing Comp Set page and make any needed changes:
![modify](/static/videos/modifyset.gif)
<br/><br/><br/>

If a hotel you'd like to shop isn't yet available it can be added on the Add Hotel page:
![add](/static/videos/addhotel.gif)


## <a name="setup"></a>Setup/Installation

#### Requirements:

- Python 3.6.8
- PostgreSQL

To have this app running on your local computer, please follow the below steps:

Clone repository:
```
$ git clone https://github.com/kgermeroth/PopWatch.git
```

Create a virtual environment:
```
$ virtualenv env
```

Activate the virtual environment:
```
$ source env/bin/activate
```

Install dependencies:
```
$ pip3 install -r requirements.txt
```

Create database 'hotels':
```
$ createdb hotels
```

Create your database tables:
```
$ python3 model.py
```

Seed database with data (optional - provided data is from a selection of San Francisco hotels):
```
$ python3 seed.py
```

Data collection: the code in web-scraping.py needs to be run on a daily basis. Allow 60 seconds between hotels to be shopped. To run manually:
```
$ python3 web-scraping.py
```

Consider scheduling with cronjobs or similar.

Run app from the command line:
```
$ python3 server.py
```

Visit localhost:5000 on your browser and enjoy!