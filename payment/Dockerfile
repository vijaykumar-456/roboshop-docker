FROM python:3.9
WORKDIR /app/
COPY *.ini .
COPY *.py .
COPY *.txt .
RUN pip3 install -r requirements.txt
EXPOSE 8080
CMD ["uwsgi","--ini", "payment.ini"]