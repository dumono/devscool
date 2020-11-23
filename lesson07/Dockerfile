FROM ubuntu:18.04
COPY webapp/app/requirements.txt /tmp/requirements.txt
RUN apt-get update
RUN DEBIAN_FRONTEND=noninteractive apt-get install -y -q python-all python-pip
RUN pip install -qr /tmp/requirements.txt
RUN mkdir /opt/webapp
COPY webapp/* /opt/webapp/
EXPOSE 5000
CMD  ["python", "/opt/webapp/app/app.py"]
