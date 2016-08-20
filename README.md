# ansible-rbenv-centos
- This is Ansible playbook + Vagrantfile to install rbenv on CentOS.
- Please refer to the following articles in the Japanese tech blog Qiita , if you want description in Japanese.
  - http://qiita.com/tbuchi888/items/fd2e8d7e1790d398b281

## Features
You can do the following in root account for CentOS6 by ansible and Vagrant(ansible provisioner).

1. Install rbenv
2. Install ruby ver.2.2.3 on rbenv
  - The version of ruby is modifiable.

## Verification Environment
Ansible provisioner and Vagrant,Virtulbox Host

- OS：OSX yosemite
- Virtulbox：5.0.10 r104061
- Vagrant： Vagrant 1.8.1
- Ansible： 2.1.0 (devel c600ab81ee)  last updated 2016/04/20

rbenv install Server (Remote hosts)
- OS: CentOS6.8 on Virtulbox

## Usage
- You can replace `ruby_ver: 2.2.3` of vars in the  `install_rbenv_without_proxy.yml` for your version.
- If you use Only Ansible, you must make Your_Inventoryhosts and,
  you run `ansible-playbook -i Your_Inventoryhosts site.yml` commands.
- If you use environment of Vagrant, you only run `vagrant up` commands.
But Please replace it with a `config.vm.box = "geerlingguy/centos6"` of box name in Vagrantfile for one's own 32bit when your host is 32bit machine.

## Caution

**License and WITHOUT ANY WARRANTY**

This program is free software; you can redistribute it and/or modify it under the terms of the GNU General Public License as published by the Free Software Foundation; either version 2 of the License, or (at your option) any later version.

This program is distributed in the hope that it will be useful, but WITHOUT ANY WARRANTY; without even the implied warranty of MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE. See the GNU General Public License for more details.

You should have received a copy of the GNU General Public License along with this program. If not, see http://www.gnu.org/licenses/.
