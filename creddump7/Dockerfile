FROM ubuntu:xenial-20160818
RUN apt-get update && \
	apt-get install \
        nmap \
        net-tools \
		netcat \
		python \
		python-pip \
		python-openssl \
		python-crypto \
		git \
		zip \
		nano \
		curl \
		-y
RUN cd / && \
	git clone https://github.com/Neohapsis/creddump7
RUN chmod +x /creddump7 pwdump.py
