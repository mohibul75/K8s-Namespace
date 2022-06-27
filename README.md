<h1>Kubernetes Namespace</h1>

Kubernetes resources are orgranized in Namespace.<br/>

Most kubernetes resouces(example-pods,services,replication controller and others) are in same nameespace.But, low level resources suck as nodes and persistent volume are not in any namespace.

*******

Use cases of K8s namespace:
<br/>
 <li>
    <ol>Structure your component</ol>
    <ol>Avoid conflict between teams</ol>
    <ol>Share services between different environments</ol>
    <ol>Access and resource limits on Namespace level</ol>
 </li>


 *******

 Defaultly there are  namespaces in kubernetes cluster.<br/>

 By default components are created in default namespace.

 ********

 To see configmap-

    kubectl get coooonfigmap

To see configmap in specific namespace-

    kubectl get configmap -n default

