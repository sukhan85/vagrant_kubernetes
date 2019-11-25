# vagrant_kubernetes
Kubernetes Environment Setup via Ansible and Vagrant

### Environment Structure

This test environment will create x3 virtual machines. One instance will act as a `master` and remaining two will act as a `worker`

```
- k8s-master
- node-1
- node-2
```

### Pre-requistis 

In order for you to start this environment you need to install the following on your laptop

- Vagrant
- Virtual Box
- Ansible

### Installation

1 - Clone the repo on your local laptop.
2 - Type `sudo vagrant up` inside `vagrant_kubernetes/` directory. It will take some time to spin up the environment initially.
3 - Once you have succesfully installed the environment, you can then `sudo vagrant ssh k8s-master` and run `kubectl get nodes`. You should get the following output

```
NAME         STATUS   ROLES    AGE     VERSION
k8s-master   Ready    master   12m     v1.16.3
node-1       Ready    <none>   9m30s   v1.16.3
node-2       Ready    <none>   6m57s   v1.16.3
```

Well done! Now you are ready to test the Kubernetes in your local laptop.


### Reference

This environment is created with reference from the following link;
- https://kubernetes.io/blog/2019/03/15/kubernetes-setup-using-ansible-and-vagrant/
