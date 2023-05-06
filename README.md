Advent of Code 2022, in Ansible!
================================

Whatever I write here, it won't be as good as what GitHub Copilot suggested.  
![Spoiler: this is not a good idea](./copilot.png)

---

This repository contains my solutions to the [Advent of Code 2022](https://adventofcode.com/2022) challenges!  

To challenge myself a bit, I decided to write these the "programming language" of the gods, and my golden hammer, [Ansible](https://www.ansible.com/). I will regret this! :D  

## Goals

I want this to actually be solving Advent of Code in Ansible, not using Ansible to call Python modules, shell scripts or other external programs. For this reason I will try to use only `ansible.builtin.*`, `ansible.utils.*` and `community.general.*` modules and filters as much as possible.  

This means the bulk of the operations will be done with `ansible.builtin.set_fact` combined with many loops, whens, untils and other Ansible magic! This repository will likely end up containing a lot of Jinja2 statements that I hope will end up being useful to know outside of this challenge.

I started this back in December of 2022 but did not get around to finishing it. My goal is to finish it before the 2023 edition starts. Maybe I'll do something even worse for that one! Terraform, maybe? :D  

## How to run
The Ansible code will run completely in memory on the local machine, so no need to configure hosts.  

To run the code, you will need to have Ansible installed. You can install it with `pip install ansible`.  

Then, you can run the code with `ansible-playbook playbooks/all.yml`.  

This will only use the example inputs given by advent of code, these are quite small and shouldn't take too long to run.  
To use the real inputs I was given, run the command again and add `-i inputs`. The inputs are located in files in `inputs/group_vars/all/day*.yml`.  

| :exclamation:  Real inputs are very large and may take several hours to process   |
|-----------------------------------------------------------------------------------|

Then, you can run the code with `ansible-playbook playbooks/all.yml -i inputs`.  


#### Limit
To limit it to specific days you can use tags. Some days can take a while, Ansible was never meant to be used like this! :)  

For example, to run only day 1, you can run `ansible-playbook playbook.yml --tags day1`.  

## License
The code is licensed under the MIT license, feel free to take inspiration and learn from my awful Jinja2 statements! I regularly use this repository as a cheat sheet for Jinja2 and Ansible filters so I hope it can be useful to others as well.  
