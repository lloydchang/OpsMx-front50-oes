FROM quay.io/opsmxpublic/ubifips:8.7
MAINTAINER sig-platform@spinnaker.io
COPY front50-web/build/install/front50 /opt/front50
RUN yum -y install java-17-openjdk-devel wget vim
RUN adduser spinnaker
RUN mkdir -p /opt/front50/plugins 
RUN chmod -R 777 /opt/front50/plugins/
RUN chown -R spinnaker:spinnaker /opt/
USER spinnaker
CMD ["/opt/front50/bin/front50"]
