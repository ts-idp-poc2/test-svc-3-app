FROM python:buster

RUN groupadd -r microsvc -g 433 && \
    mkdir /usr/local/microsvc && \
    useradd -u 431 -r -g microsvc -d /usr/local/microsvc -s /sbin/nologin -c "Micro Service User" microsvc

ADD requirements.txt /usr/local/microsvc/requirements.txt
ADD test-svc-3.py /usr/local/microsvc/test-svc-3.py

WORKDIR /usr/local/microsvc


RUN pip3 install -r ./requirements.txt

USER 431

CMD ["python3","test-svc-3.py"]