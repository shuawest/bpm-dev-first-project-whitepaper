
# Starting the Process via REST

curl -X POST -u {bpmuser}:{bpmpass} http://{bpm host and port}/business-central/rest/runtime/{groupId}:{artifactId}:{version}/process/{processId}/start

```
curl -X POST \
 -u 'testuser':'RedHat1!' \
    http://localhost:8080/business-central/rest/runtime/com.redhat.solutions.bpmtutorials:dev-first-kjar:1.6/process/com.redhat.solutions.bpmtutorials.SimpleProcess/start
```

# Uploading a maven Jar via a script

curl -X POST -u {bpmuser}:{bpmpass} -F filedata=@{file to upload} http://{bpm host and port}/maven2/{groupId with slashes}/{jar filename}

```
curl -X POST \
 -u 'testuser':'RedHat1!' \
 -F filedata=@dev-first-kjar-1.7.jar \
    http://localhost:8080/business-central/maven2/com/redhat/solutions/bpmtutorials/dev-first-kjar-1.7.jar
```

# Uploading an Ant/Eclipse Jar via a script

curl -X POST -u {bpmuser}:{bpmpass} -F groupId={groupId} -F artifactId={artifactId} -F versionId={version} \ -F filedata=@{file to upload} http://{bpm host and port}/maven2/{groupId with slashes}/{jar filename}

```
curl -X POST \
 -u 'testuser':'RedHat1!' \
 -F groupId=com.redhat.solutions.bpmtutorials \
 -F artifactId=dev-first-eclipse-project \
 -F versionId=2.3 \
 -F filedata=@dev-first-eclipse-project-2.3.jar \
    http://localhost:8080/business-central/maven2/com/redhat/solutions/bpmtutorials/dev-first-eclipse-project-2.3.jar
```

# Downloading a Jar via a script

curl -X POST -u {bpmuser}:{bpmpass} http://{bpm host and port}/business-central/maven2/{groupId with slashes}/{artifactId}/{version}/{jar filename}

```
curl -X GET \
 -u 'testuser':'RedHat1!' \
 -O http://localhost:8080/business-central/maven2/com/redhat/solutions/bpmtutorials/dev-first-kjar/1.7/dev-first-kjar-1.7.jar
```

# Deploying a KJar

curl -X POST -u {bpmuser}:{bpmpass} http://{bpm host and port}/business-central/rest/deployment/{groupId}:{artifactId}:{version}/deploy

```
curl -X POST \
 -u 'testuser':'RedHat1!' \
    http://localhost:8080/business-central/rest/deployment/com.redhat.solutions.bpmtutorials:dev-first-kjar:1.7/deploy
```

# Undeploying a KJar

curl -X POST -u {bpmuser}:{bpmpass} http://{bpm host and port}/business-central/rest/deployment/{groupId}:{artifactId}:{version}/undeploy

```
curl -X POST \
 -u 'testuser':'RedHat1!' \
    http://localhost:8080/business-central/rest/deployment/com.redhat.solutions.bpmtutorials:dev-first-kjar:1.6/undeploy
```

# Deactivating a KJar

curl -X POST -u {bpmuser}:{bpmpass} http://{bpm host and port}/business-central/rest/deployment/{groupId}:{artifactId}:{version}/deactivate

```
curl -X POST \
 -u 'testuser':'RedHat1!' \
    http://localhost:8080/business-central/rest/deployment/com.redhat.solutions.bpmtutorials:dev-first-kjar:1.7/deactivate
```

# Activating a KJar

curl -X POST -u {bpmuser}:{bpmpass} http://{bpm host and port}/business-central/rest/deployment/{groupId}:{artifactId}:{version}/activate

```
curl -X POST \
 -u 'testuser':'RedHat1!' \
    http://localhost:8080/business-central/rest/deployment/com.redhat.solutions.bpmtutorials:dev-first-kjar:1.7/activate
```














