FROM python:3.10-slim-buster

#Inside Container
#make a new folder inside container
WORKDIR /backend-flask

#Outside Containter -> Inside Containter
#this containt the libraries want to install to run the app
COPY requirements.txt requirements.txt
#Inside Container
#Install the python libraries used for the app
RUN pip3 install -r requirements.txt

#Outside Containter -> Inside Containter
# . means everything in the current directory
# primu . - /backend-flask (outside containter)
#al doile . - /backend-flash (inside containter)
COPY . .

#Set Env Vars
#Inside Container
ENV FLASK_ENV=development

EXPOSE ${PORT}

#CMD(Command)
# python3 -m flask run --host=0.0.0.0 --port=4567
CMD ["python3", "-m","flask","run", "--host=0.0.0.0", "--port=4567"]