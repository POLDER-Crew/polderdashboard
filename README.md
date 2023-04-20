# POLDER Dashboard

- The POLDER Dashboard displays KPI'S like unique users, bounce, sources of users, distinct search terms etc of the polder federated search.
- This Dashboard also shows the user behaviour of the polder federated search.




# Features


# Setup and Configuration
This dashboard is built with Flask a python framework. The front end dependencies are HTML, Javascript and css.
The data are pulled via python from google analytics. The authentication (login) portal is handled using sqlalchemy database.

# To access the dashboard;
- Open up your terminal 
- Clone this github repository
- Install all the packages from the requirements.txt `pip install -r requirements.txt`
- Activate the virtual environment `dashboard\Scripts\activate`
- Assuming you are starting from this directory  run `python app.py`
- open the local host url on your browser (This should take you to the login panel below)
![image](https://user-images.githubusercontent.com/116196967/233242980-bbf7b3ee-f65f-4686-90a7-93cbddea9b75.png)
- The login information of this dashboard are private and are accessible to the ITO (International Technology Office)
- Once you've logged in, you should be able to see the dashboard below
![image](https://user-images.githubusercontent.com/116196967/228676560-a56e3323-32df-4da2-a210-eb4ad4322601.png)



# SQLALCHEMY Database
`pip install sqlalchemy` → to install
## To see the user information (username and password)
- Open up your terminal 
- Clone this github repository
- Install all the packages from the requirements.txt `pip install -r requirements.txt`
- Activate the virtual environment `dashboard\Scripts\activate`
-  `python`
-  `from app import db`
-  `from app import User`
-  `User.query.all()` - > This should display all user information.

## To delete a user 
If you delete a user, you need to add another user, because we need one user for the login system to work.
Assuming you are still on the virtual environment with all the packages installed.
Follow the following steps;
-  `python`
-  `from app import db`
-  `from app import User`
-  `User.query.filter(User.username=='username').delete()`

## To add a user
Assuming you are still on the virtual environment with all the packages installed.
Follow the following steps;
-  `python`
-  `from app import db`
-  `from app import User`
-  `user1 = User(username='username', password='password')`
-  `db.session.add(user1) `
-  `db.session.commit()`






