---
title: 'Installation'
date: 2019-09-24T14:51:12+2:00
---

{{<content>}}

{{<content/main>}}
You will need a Kubernetes instance in order to deploy this package. If you haven't done so already, take a look at our [Kubernetes installation]({{<relref "/prereqs.md#kubernetes-cluster">}}) page. Any Kubernetes compatible cluster will do, as long as
it meets the requirements.

## Check access

Be sure that you are logged in into your Kubernetes cluster. For example, the following command
should list all namespaces that you have access to:

{{<clipboard>}}
    kubectl version
{{</clipboard>}}

This should print out the version of the client, but must also print out the version of the server.

<details>
<summary>Example output</summary>
<pre>
Client Version: version.Info{Major:"1", Minor:"16", GitVersion:"v1.16.1", GitCommit:"d647ddbd755faf07169599a625faf302ffc34458", GitTreeState:"clean", BuildDate:"2019-10-02T17:01:15Z", GoVersion:"go1.12.10", Compiler:"gc", Platform:"linux/amd64"}
Server Version: version.Info{Major:"1", Minor:"13+", GitVersion:"v1.13.4+c2a5caf", GitCommit:"c2a5caf", GitTreeState:"clean", BuildDate:"2019-09-21T02:12:52Z", GoVersion:"go1.11.13", Compiler:"gc", Platform:"linux/amd64"}
</pre>

</details>

## Clone repository

Clone the repository with the deployment scripts:

{{<clipboard>}}
    git clone https://github.com/eclipse/packages.git
    cd packages
{{</clipboard>}}

Change into the directory of this package:

{{<clipboard>}}
    cd packages/package-zero
{{</clipboard>}}

All further commands assume that you are operating from this directory.

## Run the deployment

{{</content/main>}}

{{<content/aside preserve="true">}}
{{<cluster-req "CPUs=4" "Memory=8192 MiB" "Disk=40 GiB">}}Will require cluster admin privileges.{{</cluster-req>}}
{{</content/aside>}}

{{</content>}}