FROM ubuntu:xenial-20160818
RUN apt-get update && \
	apt-get install \
        nmap \
        net-tools \
		netcat \
		python \
		python-pip \
		python-openssl \
		git \
		zip \
		nano \
		curl \
		-y
RUN cd / && \
	git clone https://github.com/mdsecactivebreach/SharpShooter.git
RUN cd /SharpShooter && \
	pip install -r ./requirements.txt
RUN chmod +x /SharpShooter/SharpShooter.py
RUN cd /tmp && \
	curl https://raw.githubusercontent.com/rapid7/metasploit-omnibus/master/config/templates/metasploit-framework-wrappers/msfupdate.erb > msfinstall && \
	chmod 755 msfinstall && \
	./msfinstall
