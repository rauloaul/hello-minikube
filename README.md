# Tutorial 11 - Hello Minikube

## Reflection

#### 1. Compare the application logs before and after you exposed it as a Service. Try to open the app several times while the proxy into the Service is running. What do you see in the logs? Does the number of logs increase each time you open the app?

Once the deployment is set up as a service, it becomes accessible externally, enabling connections from outside sources. Consequently, accessing the provided service URL will lead to a surge in log entries due to the influx of incoming HTTP requests.
 
#### 2. Notice that there are two versions of `kubectl get` invocation during this tutorial section. The first does not have any option, while the latter has `-n` option with value set to `kube-system`. What is the purpose of the `-n` option and why did the output not list the pods/services that you explicitly created?

The `-n` option is used to specify the namespace to list the resources from. The output did not list the pods/services that I explicitly created because the pods/services were created in the default namespace and not in the `kube-system` namespace.