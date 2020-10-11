# Covid19-Patient-Record-App
Covid19 Patients Records App Using Streamlit and Heroku
Link:- https://covid19-patients-record-app.herokuapp.com/
It's my first Heroku deployment app using Streamlit and Python.
In this app, I used POSTMAN API to track the covid19 patient data from web.

## Steps for Deployment
1. Make a file named coronapatientrecord.py(Your Python main file)
2. Make a file named Procfile and paste this

	web: sh setup.sh && streamlit run app.py

3. Make a file named requirements.txt
4. Make a file named setup.sh and paste this	

	mkdir -p ~/.streamlit/

	echo "\
	[server]\n\
	headless = true\n\
	port = $PORT\n\
	enableCORS = false\n\
	\n\
	" > ~/.streamlit/config.toml


5. i) 	heroku login
   ii)	heroku create
   iii)	git add .
   iv)	git commit -m "Some message Which you want"
   v)	git push heroku master
