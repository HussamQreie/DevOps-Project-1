# Vagrant

## Ensure GitBash is Installed
URL: https://github.com/git-for-windows/git/releases/download/v2.49.0.windows.1/Git-2.49.0-64-bit.exe
## Vagrant Releases
URL: https://releases.hashicorp.com/vagrant/
## Vagrant Boxes
URL: https://portal.cloud.hashicorp.com/vagrant/discover

---

```sh
vagrant init <box>
```

```sh
vagrant up
```

```sh
vagrant box list
```

```sh
vagrant status
```
-> running 

check Virtualbox

```sh
vagrant ssh
```

```sh
sudo -i
```

```sh
vagrant halt
```

```sh
vagrant status
```
-> power off

```sh
vagrant up
```

```sh
vagrant reload
```

```sh
vagrant destroy
```

```sh
vagrant status
```
-> not created

```sh
vagrant up
```

```sh
vagrant global-status
```
```sh
vagrant global-status --prune
```

---

## VagrantFile Configurations - Set VM Resources (RAM, CPU, NET ADP, etc)

- e.g. Specify CPUs and RAM
```sh
vb.memory="2048"
vb.cpus="2"
```
```sh
vagrant up # for new vm 

vagrant reload # for current vm -> apply changes
```
validate
```sh
vagrant ssh
free -m
cat /proc/cpuinfo
```

