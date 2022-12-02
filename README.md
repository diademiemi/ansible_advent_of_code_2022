# Advent of Code 2022, in Ansible!

Whatever I write here, it won't be as good as what GitHub Copilot suggested.  
![Spoiler: this is not a good idea](./copilot.png)

---

This repository contains my solutions to the [Advent of Code 2022](https://adventofcode.com/2022) challenges!  

To challenge myself a bit, I decided to write these the programming language of the gods, and my golden hammer, [Ansible](https://www.ansible.com/). I will regret this! :D  

## How to run
The Ansible code will run completely in memory on the local machine, so no need to configure hosts.  

To run the code, you will need to have Ansible installed. You can install it with `pip install ansible`.  

Then, you can run the code with `ansible-playbook playbook.yml`.  

To limit it to specific days you can use tags. Some days can take a while, Ansible was never meant to be used like this! :)  

For example, to run only day 1, you can run `ansible-playbook playbook.yml --tags day1`.  

## License
The code is licensed under the MIT license, feel free to take inspiration and learn from my awful Jinja2 statements!  
