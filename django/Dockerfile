FROM python:3.9

ENV PYTHONDONTWRITEBYCODE 1

ENV PYTHONUNBUFFERED 1

WORKDIR /app

COPY . /app

COPY requirements.txt .
RUN apt-get install -y python3
RUN pip3 install django
RUN pip3 install --upgrade pip && pip install -r requirements.txt
RUN pip3 install django-cors-headers



EXPOSE 8000

ENTRYPOINT ["sh" , "script.sh"]
