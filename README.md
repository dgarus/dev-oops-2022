# dev-oops-2022

[Download Artipie](https://github.com/artipie/artipie/releases)

$ java -jar ./artipie-v0.27.1-jar-with-dependencies.jar \
	--config-file={path}/artipie/private/my-artipie-83.yaml \
	--port=8083


$ java -jar ./artipie-v0.27.1-jar-with-dependencies.jar \
	--config-file={path}/artipie/proxy/my-artipie-84.yaml \
	--port=8084

$ mvn deploy:deploy-file \
	-DgroupId=org.example \
	-DartifactId=hello-lib \
	-Dversion=1.0-SNAPSHOT \
	-Dfile={path-to-jar} \
	-Durl=http://localhost:8083/my-maven/

$ mvn -s {path}/my-maven-settings.xml compile

$ mvn compile jib:build

$ docker login --username artipie --password artipie {host}:{port}
