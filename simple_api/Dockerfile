# image de base
FROM python:2.7-stretch
# Mes informations
LABEL maintainer="Mamadou Bobo DIALLO (dionfo45@gmail.com)"
# Copie du code source de l'api dans l'image
COPY ./student_age.py /
# Installation des prerequis pour le fonctionnement de l'api
RUN apt-get update -y && apt-get install python-dev python3-dev libsasl2-dev python-dev libldap2-dev libssl-dev -y
RUN pip install flask==1.1.2 flask_httpauth==4.1.0 flask_simpleldap python-dotenv==0.14.0
# On monte un volume pour la persistence des donnes
VOLUME [ "/data" ]
# Le port d'ecoute de l'api est le port 5000
EXPOSE 5000
# commade lance au demarrage du container
CMD [ "python", "/student_age.py" ]