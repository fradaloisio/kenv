# kenv

This repo install git, curl, vim and then install some tools to work/play with Kubernetes such as  kubeclt, krew, kubectx (as krew plugin), kubens (as krew plugin).  

Creates the ~/.kube folder and sets the KUBECONFIG and KREW_ROOT env variable, adds the kubectl autocompletion, and sets the aliases below.

```sh
alias k=kubectl
alias kns=kubectl-ns
alias kctx=kubectl-ctx
```

## How to use it

In order to avoid changing an inventory file, the playbooks are configured to run against all the hosts.

```yml
  hosts: all
```

The user and the host can be passed using the -u and -i options.

```sh
ansible-playbook -u remote_user -i remote_host, playbooks/some.yaml
```

Or run it locally.

```sh
ansible-playbook -c local -u dude -i localhost, playbooks/install_ktools.yaml
```
