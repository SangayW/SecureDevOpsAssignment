**Task 1: Set Up Initial Infrastructure**

1.  **Create a Kubernetes Cluster on GKE (or equivalent tool)**

<!-- -->

1.  Log in to your Google Cloud Console

- <https://console.cloud.google.com/>

> Step 1: Create project after logging into the google cloud console.
>
> <img src="./media/image1.png"
> style="width:6.26806in;height:3.00903in" />
>
> Step 2: Select the project that was created in Step 1

<img src="./media/image2.png" style="width:6.26806in;height:1.9625in"
alt="A screenshot of a computer Description automatically generated" />

2.  Navigate to the Kubernetes Engine section and click "Create
    Cluster."

<!-- -->

1.  Click on
    <img src="./media/image3.png" style="width:0.2626in;height:0.16456in" />
    at the left corner of the page and select **Kubernetes Engine** and
    then select **Clusters** option.

<img src="./media/image4.png" style="width:4.1076in;height:3.10694in" />

2.  Click on **ENABLE** button to enable Kubernetes Engine API

<img src="./media/image5.png"
style="width:6.26806in;height:3.08194in" />

3.  Click on the **CREATE** button to create the cluster.

<img src="./media/image6.png" style="width:6.26806in;height:2.08819in"
alt="A screenshot of a computer Description automatically generated" />

4.  Configure your cluster settings, such as the cluster name, location,
    and node pool configuration.

<!-- -->

1.  Switch to Standard Cluster by selecting **SWITCH TO STANDARD
    CLUSTER** button.

<img src="./media/image7.png"
style="width:6.26806in;height:2.83819in" />

2.  Click on **CREATE** Button after entering the cluster names and
    selecting the cluster locations to provision GKE cluster.

<img src="./media/image8.png" style="width:6.26806in;height:3.51667in"
alt="A screenshot of a computer Description automatically generated" />

1.  Cluster details are as follows:

- Cluster name: saleorcluster1

- Location: us-central1-c

<img src="./media/image9.png" style="width:6.26806in;height:1.38056in"
alt="A screenshot of a computer Description automatically generated" />

2.  Node Pools Details

- Node pool name: default-pool

- Autoscaling enabled and maximum number of nodes are configured to 5.

<img src="./media/image10.png" style="width:6.26806in;height:2.18264in"
alt="A screenshot of a computer Description automatically generated" />

2.  **Install and configure kubectl to manage your Kubernetes cluster.**

<!-- -->

1)  Installing kubectl on the Local Machines

    1.  curl -LO
        https://dl.k8s.io/release/v1.27.4/bin/linux/amd64/kubectl

<img src="./media/image11.png"
style="width:6.10448in;height:0.68059in" />

     2.  install -o root -g root -m 0755 kubectl /usr/local/bin/kubectl

<img src="./media/image12.png"
style="width:6.26806in;height:0.18264in" />

2)  Installing **gcloud cli** on the local machine

    1.  Follow instructions given in this url
        [**https://cloud.google.com/sdk/docs/install#linux**](https://cloud.google.com/sdk/docs/install#linux)

> Run below commands:

- curl -O
  https://dl.google.com/dl/cloudsdk/channels/rapid/downloads/google-cloud-cli-444.0.0-linux-x86_64.tar.gz

<img src="./media/image13.png"
style="width:6.30345in;height:0.42812in" />

- tar -xf google-cloud-cli-444.0.0-linux-x86_64.tar.gz

- ./google-cloud-sdk/install.sh

- ./google-cloud-sdk/bin/gcloud init

> Follow the onscreen instructions:

- Select the project that we have created in the GKE cluster i.e.,
  option 1 in my case.

<img src="./media/image14.png"
style="width:6.26806in;height:2.07569in" />

- Select the region that was created earlier i.e., option 7 in my case.

<img src="./media/image15.png"
style="width:6.22254in;height:5.84058in" />

<img src="./media/image16.png"
style="width:6.26806in;height:2.54722in" />

- Connecting to the GKE cluster

<img src="./media/image17.png"
style="width:6.26806in;height:3.43542in" />

- Copy the below command which was shown when clicking on the CONNECT
  menu as shown above and run on the terminal to connect.

> gcloud container clusters get-credentials saleorcluster-1 --zone
> us-central1-c –project salelorclusterassignment

1.  Installing kubectl using gcloud

<img src="./media/image18.png" style="width:4.53496in;height:4.17383in"
alt="A screenshot of a computer Description automatically generated" />

<img src="./media/image19.png"
style="width:5.04887in;height:4.19466in" />

- Run **kubectl get deployments** to verify whether local machine could
  communicate with the GKE cluster

3.  **Set up a private GitHub repository to store your project files.**

<!-- -->

1)  Go to <https://github.com/> and login if you already have an account
    otherwise, register for new account.

2)  <img src="./media/image20.png" style="width:6.26806in;height:2.12639in"
    alt="A screenshot of a computer Description automatically generated" />Click
    on the '+' icon at the top right corner of the GitHub dashboard and
    select "New repository."

3)  Choose a meaningful repository name for your ISEC6000 Secure DevOps
    project.

4)  Select "Public" for the repository visibility.

5)  You need to add a description and choose whether to initialize the
    repository with a README. (Bonus marks if you have a proper README
    file.

6)  Click "Create repository."

<img src="./media/image21.png" style="width:6.08365in;height:5.84752in"
alt="A screenshot of a computer Description automatically generated" />

Output after clicking on Create repository.

<img src="./media/image22.png"
style="width:6.26806in;height:2.74583in" />
