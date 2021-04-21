# generator-knative-simple
Generator that creates a small set of Knative resource files for applications and it's dependent services

**Note:** - For all the generated manifests, please adjust the image name to the container registry in use
* For local K8s - manifests work as-is
* For GCR, for example - image: gcr.io/<project_name>/<image-name>

## Deploying to Knative
To deploy the service to Knative, select the image you wish to deploy, generated in the `kubernetes` folder:
* JVM - /kubernetes/jvm/service.yaml 
* Native - /kubernetes/native/service-native.yaml

To deploy the service, please execute:
```shell
$ kubectl apply -f /kubernetes/jvm/service.yaml 

$ kubectl apply -f /kubernetes/jvm/service-native.yaml
```

To delete the service, please execute:
```shell
$ kubectl delete -f /kubernetes/jvm/service.yaml 

$ kubectl delete -f /kubernetes/jvm/service-native.yaml
```

