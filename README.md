# Java-tomcat-sample  

## Java setup
install dmg  

## Setup Maven
### 1.download from https://maven.apache.org/download.cgi  
### 2.execute the following command  
cd /usr/local  
mv Downloads/apache-maven-3.3.9-bin.tar.gz .  
tar zxvf apache-maven-3.3.9-bin.tar.gz  
rm apache-maven-3.3.9-bin.tar.gz  
### 3.edit bash_profile  
cd ~  
vi .bash_profile  
.bash_profileの内容  
 export M3_HOME=/usr/local/apache-maven-3.3.3  
 M3=$M3_HOME/bin  
 export PATH=$M3:$PATH  
4.reflect 3.modification  
source .bash_profile  
export MAVEN_HOME=$M3_HOME  

##  IntelliJ setup
https://github.com/shinyay/intellij-with-maven-tomcat-plugin  

## take care of the following  
set ```<scope>provided</scope>``` of javax.servlet pom.xml  
**java.lang.LinkageError: loader constraint violation: loader (instance of org/apache/jasper/servlet/JasperLoader) previously initiated loading for a different type with name "javax/servlet/http/HttpServletRequest"**  
http://stackoverflow.com/questions/11145710/tomcat7-maven-plugin-tomcat7run-java-lang-linkageerror-previously-initiated-loa  