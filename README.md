# mac

Update `PATH` for running brew:
```bash
vim ~/.zshrc
```

```bash
export PATH=$PATH:/opt/homebrew/bin
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
  node \
  helm \
  iproute2mac \
  wget \
  bat \
  azure-cli \
  tree \
  packer \
  terraform \
  rke \
  kubebuilder \
  htop \
  nmap \
  jq \
  teleport \
  velero \
  kubeseal \
  kops \
  bash \
  jsonnet \
  gnupg
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

