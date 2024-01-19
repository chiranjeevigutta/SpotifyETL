Install all the packages in requirements.txt using below command

pip install -r requirements.txt

To schedule celery tasks, open two terminals and run the below commands

Terminal 1:
celery -A tasks beat --loglevel=info 

Terminal 2:
celery -A tasks worker --pool=solo -l info



The main goal of this project is to create a system that automatically extracts listening data from Spotify API called Spotipy, transforms it into spark dataframes using python, and loads it into a PostgreSQL database. This database can then be used to generate a summary email with metrics related to the user's listening habits. The objectives of this project are to:
•	Successfully extract listening data using Spotipy API.
•	Transform the data into a format suitable for analysis.
•	Load the transformed data into a Postgresql database.
•	Generate a summary email with relevant metrics.
•	Automate the entire process using Celery.


Summary generation:
Summary consists of the following insights from the listening history of the user.
o	Most listened tracks.
o	Most listened to artists.
o	Tracks that a user spent most time on.
•	To achieve these results, SQL functions are used and called upon. 
o	Function to calculate total time spent listening to Spotify.
