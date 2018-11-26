# kubeha

## ssh setting on all hosts

```bash
    ssh-copy-id  root@xxx
```

## install all

Config your own hosts

```bash
vim hosts
```

```bash
ansible-playbook roles/install-all.yaml
```

## uninstall all

```bash
ansible-playbook roles/uninstall-all.yaml
```

## usage

```bash
docker run --rm -v $(pwd):/data/kube1.11.3.tar.gz -v $(pwd)/hosts:/etc/ansible/hosts  -v /root/.ssh/:/root/.ssh/ -it kubeha:1.11.3 bash
```
