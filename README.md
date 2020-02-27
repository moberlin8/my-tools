# my-tools
A list of command line tools, with a focus on Kubernetes

- [brew](https://brew.sh/) - The Missing Package Manager for macOS
- [kubectl](https://kubernetes.io/docs/tasks/tools/install-kubectl/) - Command Line Interface (CLI) for kubernetes.
- [kubectx kubens](https://github.com/ahmetb/kubectx) - Two handy command line tools, kube context and kube namespace.
- [popeye](https://github.com/derailed/popeye) - A Kubernetes cluster resource sanitizer
- [stern](https://github.com/wercker/stern) - Multi pod and container log tailing for Kubernetes
- [oc](https://docs.openshift.com/container-platform/4.3/cli_reference/openshift_cli/getting-started-cli.html) - OpenShift Container Platform command-line interface (CLI)
- [minikube](https://kubernetes.io/docs/setup/learning-environment/minikube/) - Run Kubernetes locally
- [crc](https://cloud.redhat.com/openshift/install/crc/installer-provisioned) - Code Ready Containers - Red Hat Open Shift 4 for your laptop
- [powerlevel9k](https://github.com/Powerlevel9k/powerlevel9k) - oh-my-zsh theme.
- [powerlevel10k](https://github.com/romkatv/powerlevel10k) - faster than powerlevel9k zsh theme.
- [tektoncd-cli](https://github.com/tektoncd/cli) - A CLI for interacting with Tekton
- [kind](https://github.com/kubernetes-sigs/kind) - Kubernetes in Docker
- [spekt8](https://github.com/spekt8/spekt8) - Visualize your Kubernetes cluster in real time
- [docker-image-tag](https://github.com/stefanwalther/docker-image-tag) - Search docker hub by tags

- [jq](https://stedolan.github.io/jq/) - Like sed for JSON data
- [yq](https://github.com/mikefarah/yq) - A portable command-line YAML processor
- [inlets](https://github.com/inlets/inlets) - Cloud Native Tunnel written in Go

Other stuff:

- [TektonCD Catalog](https://github.com/tektoncd/catalog) - Catalog of shared Tasks and Pipelines.
- [Buildah](https://github.com/containers/buildah/) - A tool that facilitates building Open Container Initiative (OCI) container images
- [kubectl-fzf](http://bit.ly/2Nf6Ktq) - A fast kubectl autocompletion with fzf

Other other stuff:

- [tldr](https://tldr.sh/) - Simplified man pages
- [trailer](https://github.com/ptsochantaris/trailer) - Alerts for Pull Requests and Issues For GitHub & GitHub Enterprise
- [JHipster](https://www.jhipster.tech/) Quickstart for creating a Java Spring app
- [asciinema](https://asciinema.org/) asciinema is a free and open source solution for recording terminal sessions and sharing them on the web.

### A few configuration notes (for zsh and byobu)

- [Moving to zsh](https://scriptingosx.com/2019/06/moving-to-zsh/) Excellant set of articles about moving to zsh on a Mac
- [byobu](https://byobu.org/news.html) Byobu is a text-based window manager and terminal multiplexer.

#### Install needed software (debian or Ubuntu)
`sudo apt install -y git zsh byobu`

#### Set zsh as my shell
`chsh -s /bin/zsh`

#### Install oh-my-zsh
`sh -c "$(wget -O- https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"`

#### Install powerlevel10k
`git clone --depth=1 https://github.com/romkatv/powerlevel10k.git $ZSH_CUSTOM/themes/powerlevel10k`

#### Install zsh-autosuggestions plugin
`git clone https://github.com/zsh-users/zsh-autosuggestions ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-autosuggestions`

#### edit `~/.zshrc`
```
export ZSH_AUTOSUGGEST_HIGHLIGHT_STYLE='fg=3'

ZSH_THEME="powerlevel10k/powerlevel10k"
plugins=(zsh-autosuggestions git kube-ps1 kubectl)
```

#### edit `~/.p10k.zsh`
```
typeset -g POWERLEVEL9K_TIME_FORMAT='%D{%L:%M}'

#############[ kubecontext: current kubernetes context (https://kubernetes.io/) ]#############
# Show kubecontext only when the the command you are typing invokes one of these tools.
# Tip: Remove the next line to always show kubecontext.
###typeset -g POWERLEVEL9K_KUBECONTEXT_SHOW_ON_COMMAND='kubectl|helm|kubens|kubectx|oc'

```

#### edit `~/.byobu/.tmux.conf`
```
# mao 2020-02-18 https://gist.github.com/ziwon/5874217
# enable 256-colors
set -g default-terminal "screen-256color"
```
