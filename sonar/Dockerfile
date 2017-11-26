#
# Creates a docker container with SonarQube, incl. several plugins
#

FROM sonarqube:6.7-alpine

MAINTAINER Marcel Birkner <marcel.birkner@codecentric.de>

ENV SONARQUBE_HOME /opt/sonarqube

# Plugin Versions
ENV SONAR_JAVA_PLUGIN 4.15.0.12310
ENV SONAR_WEB_PLUGIN 2.5.0.476
ENV SONAR_SCM_GIT_PLUGIN 1.3.0.869

# Add plugins
RUN mkdir -p $SONARQUBE_HOME/extensions/plugins/

ADD https://sonarsource.bintray.com/Distribution/sonar-java-plugin/sonar-java-plugin-${SONAR_JAVA_PLUGIN}.jar $SONARQUBE_HOME/extensions/plugins/sonar-java-plugin-${SONAR_JAVA_PLUGIN}.jar

ADD https://sonarsource.bintray.com/Distribution/sonar-web-plugin/sonar-web-plugin-${SONAR_WEB_PLUGIN}.jar $SONARQUBE_HOME/extensions/plugins/sonar-web-plugin-${SONAR_WEB_PLUGIN}.jar

ADD https://sonarsource.bintray.com/Distribution/sonar-scm-git-plugin/sonar-scm-git-plugin-${SONAR_SCM_GIT_PLUGIN}.jar $SONARQUBE_HOME/extensions/plugins/sonar-scm-git-plugin-${SONAR_SCM_GIT_PLUGIN}.jar
