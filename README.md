# dev-oops-2022

[Download Artipie](https://github.com/artipie/artipie/releases)

[Artipie wiki](https://github.com/artipie/artipie/wiki)

$ java -jar ./artipie-v0.27.1-jar-with-dependencies.jar \
	--config-file={path}/artipie/private/my-artipie-83.yaml \
	--port=8083


$ java -jar ./artipie-v0.27.1-jar-with-dependencies.jar \
	--config-file={path}/artipie/proxy/my-artipie-84.yaml \
	--port=8084

$ mvn deploy:deploy-file \
	-DgroupId={group-id} \
	-DartifactId={artifact-id} \
	-Dversion={version} \
	-Dfile={path-to-jar} \
	-Durl={host}:{port}/{repo-name}/

$ mvn -s {path}/my-maven-settings.xml compile

$ mvn compile jib:build

$ docker login --username artipie --password artipie {host}:{port}
