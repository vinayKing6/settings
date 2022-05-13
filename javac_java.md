#compile java with jar
    javac -classpath .:lib/[your jar files for each] javafile.java -d [output classes directory (strongly suggested)]
#run java with jar
    cd classes
    java -classpath .:../lib/[your jar files for each] java.class(like com.king.hello)
#compile java with jar but no -classpath:
    1 unzip <path to jars> -d <classes path>
    2 javac -cp .:classes <path to java file> -d <classes path>
    3 cd <classes path>
    4 java <path to java class>(like com.king.hello)

