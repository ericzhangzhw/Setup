# Setup
## Linux
### zsh
* zsh

	```
	sudo yum install zsh
	```
* oh-my-zsh

	```
	sh -c "$(curl -fsSL https://raw.github.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
	```
* Setup

	Update `ZSH_THEME="dallas"` | `ZSH_THEME="fino-time"` in `~/.zshrc` 
	
### aws
* Install

	```
	curl "https://s3.amazonaws.com/aws-cli/awscli-bundle.zip" -o "awscli-bundle.zip"
	unzip awscli-bundle.zip
	sudo ./awscli-bundle/install -i /usr/local/aws -b /usr/local/bin/aws
	```
* Setup

	```
	aws configure
	```
	Enter aws config info:
	
	```
	AWS Access Key ID [None]: {Access ID}
	AWS Secret Access Key [None]: {Access Key}
	Default region name [None]: us-west-2
	Default output format [None]: json
	```
	
### git
* Install

	```
	sudo yum install git-all
	```
* Setup 
	1. Generate new ssh key: `ssh-keygen -t ed25519 -C "{email}"`
	2. Start agent: `eval "$(ssh-agent -s)"`
	3. Add ssh private key: `ssh-add ~/.ssh/id_ed25519`
	4. Copy output from : `cat ~/.ssh/id_ed25519.pub` to github account setting

### postgresql client

```
sudo yum install postgresql
```
### terraform
* Install
	1. Download terraform: `wget https://releases.hashicorp.com/terraform/0.14.9/terraform_0.14.9_linux_amd64.zip`
	2. Unzip terraform package: `unzip terraform_0.14.9_linux_amd64.zip`
	3. Make executable command: `chmod +x terraform` and `sudo mv terraform /usr/local/bin/`
	4. Check version: `terraform --version`

### serverless
* Install
	1. Download serverless: `curl -o- -L https://slss.io/install | VERSION=2.28.0 zsh`
	2. Add `export PATH="$HOME/.serverless/bin:$PATH"` to `~/.zshrc` and run `source ~/.zshrc`
	3. Check version: `serverless --version`

## Mac