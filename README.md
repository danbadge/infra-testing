Testing Infrastructure
======================

## Installation

There are three main technologies in use here:

- Serverspec
- Ansible
- Vagrant

You will need the following installed locally:
- Ansible
- Vagrant
- Virtualbox

Once they're installed you will need to install these vagrant serverspec plugins:
```
vagrant plugin install vagrant-serverspec
vagrant plugin install vagrant-hostmanager
```

And then run:
```
bundle install
```

## Developer workflow
This details the basic developer workflow to get into the classic red-green-refactor cycle using these tools:

1. ``` vagrant up ``` - Bring up the server 

2. Write a test

3. ``` rake spec ``` - Run the tests (red) 

4. Make the simpliest change to get your tests to pass

5. ``` vagrant provision ``` - Apply those changes 

6. ``` rake spec ``` - Run the tests (green)

7. Refactor and then repeat 2-7! 