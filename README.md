<h1>Kubernetes Namespace</h1>

Kubernetes resources are orgranized in Namespace.<br/>

Most kubernetes resouces(example-pods,services,replication controller and others) are in same nameespace.But, low level resources suck as nodes and persistent volume are not in any namespace.

*******

Use cases of K8s namespace:
<br/>
 <ol>
    <li>Structure your component</li>
    <li>Avoid conflict between teams</li>
    <li>Share services between different environments</li>
    <li>Access and resource limits on Namespace level</li>
 </ol>


 *******

 Defaultly there are  namespaces in kubernetes cluster.<br/>

 By default components are created in default namespace.

 ********

 To see configmap-

    kubectl get configmap

To see configmap in specific namespace-

    kubectl get configmap -n default

