FROM debian:latest

WORKDIR /app

ADD my-app.py /app

RUN apt-get update -y && \
    apt-get install -y make build-essential libssl-dev zlib1g-dev libbz2-dev \
	libreadline-dev libsqlite3-dev libbz2-dev libreadline-dev libsqlite3-dev \
	wget curl llvm libncurses5-dev libncursesw5-dev xz-utils tk-dev

RUN wget https://www.python.org/ftp/python/3.6.3/Python-3.6.3.tgz && \
	tar xvf Python-3.6.3.tgz && \
	cd Python-3.6.3 && \
	./configure && \
	make -j8 && \
	make install

CMD python3.6 my-app.py
