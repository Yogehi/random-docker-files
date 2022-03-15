FROM ubuntu:focal-20201106

ENV TZ=US/Eastern
RUN ln -snf /usr/share/zoneinfo/$TZ /etc/localtime && echo $TZ > /etc/timezone

# install appropriate programs
RUN apt-get update && \
	apt-get install -y \
	curl \
	apt-utils \
	git \
	python3 \
	build-essential \
	python3-pip \
	android-tools-adb \
	aapt \
	apksigner \
	wget \
	zipalign

RUN pip3 install frida
RUN pip3 install frida-tools
RUN pip3 install objection

RUN wget https://raw.githubusercontent.com/iBotPeaches/Apktool/master/scripts/linux/apktool -O /bin/apktool
RUN wget https://bitbucket.org/iBotPeaches/apktool/downloads/apktool_2.5.0.jar -O /bin/apktool.jar

RUN chmod +x /bin/apktool

#docker run --privileged -it -v /dev/bus/usb:/dev/bus/usb yogehi/objection_docker bash
