FROM python:3.6
ADD . /srv/foodlord
WORKDIR /srv/foodlord
RUN pip install --upgrade pip
RUN pip3 install -r requirements.lock
RUN sed -i 's/localhost/foodlord-db/g' /srv/foodlord/src/__init__.py
CMD uwsgi --ini foodlord.ini