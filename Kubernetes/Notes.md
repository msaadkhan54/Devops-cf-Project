**CLUSTER DOWNLOADING:**


first install **DOCKER AND GIT on EC2.**



Then go in: **cd /etc/containerd**



Here delete: **rm config.toml**



Then do: **sudo containerd config default | sudo tee /etc/containerd/config.toml**



Then do: **nano config.toml**



In it find '**SystemdCgroup: false'**



**and make it true.**

Then do: **sudo systemctl restart containerd**



Then do: **sudo systemctl daemon-reload**



Then : **sudo swapoff -a**

Then : **swapon --show**



Then run commands from documentation link: **https://kubernetes.io/docs/setup/production-environment/tools/kubeadm/install-kubeadm/**

then run : '**kubeadm init'** on only master node



Then run the following giving commands on terminal and then add token given on master node to the workerNode

Then on Master Node: **curl https://raw.githubusercontent.com/projectcalico/calico/v3.28.0/manifests/calico.yaml -O**



&#x20; **''       ''      :  kubectl apply -f calico.yaml**

