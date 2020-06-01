# Lab 0. Installing Helm on IBM Cloud Kubernetes Service

There are two parts to installing Helm: the client (helm) and the server (Tiller). Helm can be installed from source or pre-built binary releases. In this lab, we are going to use the pre-built binary release (Linux amd64) from the Helm community. Refer to the [Helm install docs](https://v2.helm.sh/docs/using_helm/#install-helm) for more details. 

# Prerequisites

Create a Kubernetes cluster with [IBM Cloud Kubernetes Service](https://cloud.ibm.com/docs/containers/cs_tutorials.html#cs_cluster_tutorial), following the steps to also configure the IBM Cloud CLI with the Kubernetes Service plug-in.

# Installing the Helm Client (helm)

1. Download the [latest release of Helm v2](https://github.com/helm/helm/releases) for your environment, which in this case is `Linux amd64`.

2. Unpack it: `$ tar -zxvf helm-v2.<x>.<y>-linux-amd64.tgz`.

3. Find the helm binary in the unpacked directory, and move it to its desired location: `mv linux-amd64/helm /usr/local/bin/helm`. It is best if the location you copy to is pathed, as it avoids having to path the helm commands.

4. The Helm client is now installed and can be tested with the command, `helm help`. Refer to the doc [installing Client](https://v2.helm.sh/docs/using_helm/#installing-the-helm-client) for more details.

# Installing the Helm Server (Tiller)

1. Run the command: `$ helm init`. This will initialize the Helm CLI and also install Tiller into the Kubernetes cluster under the `tiller-namespace`.

2. You can verify that the client and server are installed correctly by running the command, `helm version`. This should return both the client and server versions. Refer to the doc [installing Tiller](https://v2.helm.sh/docs/using_helm/#installing-tiller) for more details.

# Conclusion

You are now ready to start using Helm.
