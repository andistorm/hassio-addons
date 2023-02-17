FROM ubuntu:22.04
RUN apt-get update \
    && apt-get install tesseract-ocr -y \
    python3 \
    libjpeg-dev \
    zlib1g-dev \
    #python-setuptools \
    python3-pip \
    && apt-get clean \
    && apt-get autoremove

COPY requirements.txt /

RUN pip3 install -r /requirements.txt

VOLUME ["/data"]
EXPOSE 5000 5000
CMD ["python3" ,"app.py"]
