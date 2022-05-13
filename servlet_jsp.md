#create project with maven:
    project
       |
       |---src/servlet.java
       |
       |---classes/servlet.class
       |
       |---etc/web.xml
#compile:
    javac -classpath /path/to/tomcat/lib/servlet-api.jar -d classes /path/to/servlet.java
#run:
    put classes/servlet.class in tomcat/webapps/project/WEB-INF/classes
    put web.xml in tomcat/webapps/project/WEB-INF
