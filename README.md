<h1>Kubernetes Namespace</h1>

Kubernetes resources are orgranized in Namespace.<br/>

Most kubernetes resouces(example-pods,services,replication controller and others) are in same nameespace.But, low level resources such as nodes and persistent volume are not in any namespace.

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

    kubectl get config -o wide

    kubectl get configmap -o yaml

*******************

<h3>Creating new namespace </h3>

There are two way to create new namespace. one is create by kubectl command and another one is create by yml file.

<br/>

created by command 

    kubectl apply -f <yml file name> --namespace=<namespace name>

created by yml file<br/>

create new yml file with kind: namespace<br/>


creating namespace with yml file is recommanded by experts.

***********

<h3>Namespace Switching </h3>

Defaultly , every resource creates on default namespace. To create resource in a specific namespace , switching is neccessary.<br/>

namespace switching by command 

    kubectl config set-context $(kubectl config current-context) --namespace=<ns name>

 using kubens is another way to switching namespace.

 kubens command to see namespace
   
    kubens

kubens command to switsching namespace

    kubens <ns name>

*************

<h3>Kubens & kubectx Installation</h3>

    sudo git clone https://github.com/ahmetb/kubectx /opt/kubectx

    sudo ln -s /opt/kubectx/kubectx /usr/local/bin/kubectx

    sudo ln -s /opt/kubectx/kubens /usr/local/bin/kubens


