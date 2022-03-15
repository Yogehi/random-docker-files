FROM httpd:latest
RUN apt-get update && \
	apt-get install -y \
	wget \
	zip

RUN wget -O /usr/local/apache2/htdocs/yay.zip https://gchq.github.io/CyberChef/CyberChef_v9.28.0.zip
RUN unzip /usr/local/apache2/htdocs/yay.zip -d /usr/local/apache2/htdocs/
RUN cp /usr/local/apache2/htdocs/CyberChef_v9.28.0.html /usr/local/apache2/htdocs/index.html
# to run
# docker run -dit -p 8080:80 yogehi/cyberchef_docker
