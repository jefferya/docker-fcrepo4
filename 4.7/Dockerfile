FROM tomcat:8.5

ENV FCREPO_VERSION 4.7.4.1

# Configuration for Fedora: 
#   https://wiki.duraspace.org/display/FEDORA47/Application+Configuration
#   https://wiki.duraspace.org/display/FEDORA45/Configuring+Logging+With+System+Properties
#   https://wiki.duraspace.org/display/FEDORA4x/Best+Practices+-+Fedora+Configuration
ENV JAVA_OPTS="${JAVA_OPTS} \
  -Dlogback.configurationFile=classpath:/logback.xml \
  -Dfcrepo.log=DEBUG \
  -Dfcrepo.log.directory=${CATALINA_HOME}/logs \
  -Dfcrepo.log.maxHistory=14 \
  -Dfcrepo.log.totalSizeCap=100000 \
  -Dfcrepo.modeshape.configuration=classpath:/config/minimal-default/repository.json \
  -Dfcrepo.modeshape.index.directory=/fcrepo4-data/modeshape.index \
  -Dfcrepo.home=/fcrepo4-data \
"

# Install Fedora with OAI-Provider
ADD https://github.com/ualbertalib/fcrepo4-oaiprovider/releases/download/fcrepo4-oaiprovider-${FCREPO_VERSION}/fcrepo-oaiprovider-${FCREPO_VERSION}.war ${CATALINA_HOME}/webapps/fcrepo.war
