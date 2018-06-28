******************
Setting up Docker
******************

`Docker <https://docs.docker.com/get-started/>`_ is a platform for developers and sysadmins to develop, deploy, and run applications with containers.
The use of Linux containers to deploy applications is called containerization.
Containers are not new, but their use for easily deploying applications is.

Containerization is increasingly popular because containers are:

  - Flexible: Even the most complex applications can be containerized.
  - Lightweight: Containers leverage and share the host kernel.
  - Interchangeable: You can deploy updates and upgrades on-the-fly.
  - Portable: You can build locally, deploy to the cloud, and run anywhere.
  - Scalable: You can increase and automatically distribute container replicas.
  - Stackable: You can stack services vertically and on-the-fly.


Downloading Docker
-------------------

Please visit the `Docker Download link <https://docs.docker.com/install/>`_ to download the
latest Stable Docker Community Edition. There are downloads for use on local hardware (macOS, Win), Cloud (AWS and Azure), or Server (CentOS, DEbian, Fedora, or Ubuntu)
I chose the `macOS <https://docs.docker.com/docker-for-mac/install/>`_ version.


Installing Docker
------------------

#.
  Open the installer you just downloaded from Docker's site, and drag the application to the Applications Directory.
#.
  Double click on Docker.app and follow the directions posted on `Docker's site <https://docs.docker.com/docker-for-mac/install/>`_.
  They are good.


Getting Started after Docker install
--------------------------------------

Again, Docker's site is well documented.  `Click here <https://docs.docker.com/docker-for-mac/>`_ for some commands to get you started.

Kubernetes
-----------

`Kubernetes <https://docs.docker.com/docker-for-mac/#kubernetes>`_ is only available in Docker for Mac 17.12 CE and higher, on the `Edge channel <https://docs.docker.com/docker-for-mac/kubernetes/>`_. Kubernetes support is not included in Docker for Mac Stable releases.
To find out more about Stable and Edge channels and how to switch between them, see `General configuration <https://docs.docker.com/docker-for-mac/#explore-the-application>`_.

Docker for Mac 17.12 CE (and higher) Edge includes a standalone Kubernetes server that runs on your Mac, so that you can test deploying your Docker workloads on Kubernetes.
