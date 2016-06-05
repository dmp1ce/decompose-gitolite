# decompose Gitolite environment
Decompose environment for running Gitolite

## Requirements

- [decompose](https://github.com/dmp1ce/decompose)

## How to use

0. Install decompose
1. `decompose --init https://github.com/dmp1ce/decompose-gitolite.git`
2. Copy your public ssh key to `admin.pub` so you can admin gitolite. For example: `cat ~/.ssh/id_rsa.pub > admin.pub`
3. `decompose build && decompose up`
4. Access gitolite using `git clone ssh://git@localhost:10022/gitolite-admin` or `ssh -p 10022 git@localhost:10022`

# SSH Port

The default port is `10022`. To change the value change the `PROJECT_SSH_PORT` element in the `elements` file. 

# SSH key name

For the initial setup of Gitolite the default SSH key name is `admin`. The value can be changed by changing the `PROJECT_SSH_KEY_NAME` element in the `elements` file.
