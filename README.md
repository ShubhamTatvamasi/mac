# mac

Update `PATH` for running brew:
```bash
vim ~/.zshrc
```

```bash
export PATH=/opt/homebrew/bin:$PATH
```

Update all packages:
```bash
brew update
brew upgrade
```

Install regular tools:
```bash
brew install \
  go \
  multipass \
  ansible \
  hugo \
  kubectx \
  awscli \
  aws-cdk \
  node@22 \
  helm \
  iproute2mac \
  wget \
  bat \
  azure-cli \
  tree \
  packer \
  rke \
  kubebuilder \
  htop \
  nmap \
  jq \
  ffind \
  teleport \
  velero \
  kubeseal \
  kops \
  bash \
  jsonnet \
  gnupg \
  ripgrep \
  git \
  pwgen \
  wireguard-tools \
  minikube \
  yq \
  telnet \
  checkov \
  poppler
```

link node:
```bash
brew unlink node@22
brew link --overwrite node@22
```

Link node:
```bash
ln -s /opt/homebrew/Cellar/node@22/22.13.0 /opt/homebrew/opt/node
```

link python:
```bash
ln -s /opt/homebrew/Cellar/python@3.11/3.11.11 /opt/homebrew/opt/python@3
ln -s /opt/homebrew/Cellar/python@3.11/3.11.11/bin/python3.11 /opt/homebrew/bin/python3
```

Set Go Path:
```bash
mkdir -p ~/go/{bin,pkg,src}
echo 'export GOPATH="$HOME/go"' >> ~/.zshrc
echo 'export PATH="$PATH:${GOPATH//://bin:}/bin"' >> ~/.zshrc
source ~/.zshrc
```

Flush DNS records:
```bash
sudo dscacheutil -flushcache; sudo killall -HUP mDNSResponder
```

Delete windscribe data:
```bash
rm ~/Library/Preferences/com.windscribe.Windscribe.plist
```

Check system info:
```bash
alias free="top -l 1 -s 0 | head"
```

