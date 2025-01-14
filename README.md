<img src="https://wattson.it/img/logo/wattson-white-blue.svg" width="50%"/>

Wattson is a research testbed that allows investigating and analyzing the effects of cyberattacks on power grids.

Project Website: https://wattson.it

## Disclaimer
Wattson comes without any warranty or guarantees to function.
Use at your own risk.
Wattson can mess up you computer's network configuration if used incorrectly.

Wattson is intended to be used for research enhancing the security of power grids.

## Cite
When you refer to Wattson in your publication, please cite our paper:

> Comprehensively Analyzing the Impact of Cyberattacks on Power Grids

in 8th IEEE European Symposium on Security and Privacy 2023 (Euro S&P).

https://wattson.it/cite


## Installation
For better performance, we suggest using a bare-metal installation instead of a virtual machine.

As the operating system, please use Ubuntu 22.04 LTS.  
Other distributions might work, but you have to install dependencies yourself.

### Install APT Dependencies
```bash
sudo apt update
sudo apt upgrade -y
sudo apt install -y python3-pip git gcc make perl
```


### Install Wattson
This automatically installs Wattson's system dependencies (OVS, Containernet, ...).  
If you do not want this, skip the second step (`python3 setup.py wattson`). 
Then, you have to install the dependencies manually.

```bash
git clone https://github.com/fkie-cad/wattson
sudo python3 wattson/setup.py wattson
sudo python3 -m pip install -e ./wattson
```

## Usage
To start a basic simulation of the cigre_mv scenario, run
```bash
sudo python3 -m wattson wattson/scenarios/cigre_mv
```

## Contributing
As Wattson (internally) is undergoing significant refactoring and this public repository does not contain all parts of Wattson due to ethical considerations, making contributions via this repository is not (yet) encouraged.

For problems or suggestions, please open a respective issue.
If you can point out the changes to be made to fix your problem, feel free to do so as well.

Patches are then applied to our internal version of Wattson and mirrored back into this repository.

## Acknowledgments
A special thank goes to [Martin Unkel](https://github.com/m-unkel) for his implementation of the C++-based Python bindings for the IEC104 protocol. The project is available at [PyPi](https://pypi.org/project/c104/) and on [Github](https://github.com/Fraunhofer-FIT-DIEN/iec104-python).