# kubeha

## usage

```bash
docker run --rm -v /data/kube1.11.3.tar.gz:/data/kube1.11.3.tar.gz  -v /root/.ssh/:/root/.ssh/ -it -w /etc/ansible kubeha:1.11.3 bash
```

## ssh setting on all hosts

```bash
    ssh-copy-id  root@xxx
```

## install all

Config your own hosts

```bash
cd /etc/ansible
vim hosts
```

```bash
ansible-playbook roles/install-all.yaml
```

## uninstall all

```bash
ansible-playbook roles/uninstall-all.yaml
```