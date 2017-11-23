FROM tomcat:8.5

ENV FCREPO_VERSION 4.7.1

# Configuration for Fedora: https://wiki.duraspace.org/display/FEDORA47/Application+Configuration
ENV JAVA_OPTS="${JAVA_OPTS} -Dfcrepo.modeshape.configuration=classpath:/config/file-simple/repository.json -Dfcrepo.home=/fcrepo4-data"

# Install Fedora
#ADD https://github.com/fcrepo4/fcrepo4/releases/download/fcrepo-${FCREPO_VERSION}/fcrepo-webapp-${FCREPO_VERSION}.war ${CATALINA_HOME}/webapps/fcrepo.war
# Install Fedora with OAI-Provider
ADD https://github.com/ualbertalib/fcrepo4-oaiprovider/releases/download/fcrepo4-oaiprovider-${FCREPO_VERSION}/fcrepo-oaiprovider-${FCREPO_VERSION}.war ${CATALINA_HOME}/webapps/fcrepo.war
