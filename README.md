# Maven archetype
- Template para gerar outros projetos
- Gerar um archetype
```
mvn archetype:generate -B \
-DarchetypeGroupId=org.apache.maven.archetypes \
-DarchetypeArtifactId=maven-archetype-archetype \
-DarchetypeVersion=1.4 \
-DgroupId=com.github.fabriciolfj \
-DartifactId=maven-archetype-spring \
-Dversion=1.0-SNAPSHOT

mvn archetype:create-from-project
```  
- Modelo spring
```
git clone https://github.com/Romeh/spring-boot-quickstart-archtype.git
cd spring-boot-quickstart-archtype
mvn clean install

mvn archetype:generate \
     -DarchetypeGroupId=com.romeh.spring-boot-archetypes \
     -DarchetypeArtifactId=spring-boot-quickstart \
     -DarchetypeVersion=1.0.0 \
     -DgroupId=com.github.fabriciolfj \
     -DartifactId=product \
     -Dversion=1.0.0-SNAPSHOT \
     -DinteractiveMode=false
```
- Nova versão
```
mvn archetype:generate   \
   -DarchetypeGroupId=com.github.fabriciolfj   \
   -DarchetypeArtifactId=spring-boot-quickstart   \
   -DarchetypeVersion=1.0.0  \
   -DgroupId=com.github.fabriciolfj   \
   -DartifactId=product  \
   -Dversion=1.0.0-SNAPSHOT  -DinteractiveMode=false
``