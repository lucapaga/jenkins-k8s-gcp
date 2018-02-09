FROM gcr.io/cloud-solutions-images/jenkins-k8s-slave

RUN 	apt-get update && \
	curl -sL https://deb.nodesource.com/setup_8.x | bash - && \
	apt-get install -y nodejs && \
	apt-get install -y build-essential && \
	apt-get install -y zip && \
	apt-get install -y software-properties-common && \
	curl -fsSL https://download.docker.com/linux/$(. /etc/os-release; echo "$ID")/gpg | apt-key add - && \
	add-apt-repository \
   "deb [arch=amd64] https://download.docker.com/linux/$(. /etc/os-release; echo "$ID") \
   $(lsb_release -cs) \
   stable" && \
	apt-get update && \
	apt-get install -y docker-ce

