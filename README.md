# mac

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
  kubebuilder
```

Set Go Path:
```bash
mkdir -p ~/go/{bin,pkg,src}
echo 'export GOPATH="$HOME/go"' >> ~/.zshrc
echo 'export PATH="$PATH:${GOPATH//://bin:}/bin"' >> ~/.zshrc
source ~/.zshrc
```


Delete windscribe data:
```bash
rm ~/Library/Preferences/com.windscribe.Windscribe.plist
```
