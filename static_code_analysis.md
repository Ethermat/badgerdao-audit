# Static Code Analysis

## Preparations
```
git clone https://github.com/Badger-Finance/badger-system.git

docker pull trailofbits/eth-security-toolbox
docker run -it -v $(pwd):/audit trailofbits/eth-security-toolbox:latest

sudo apt-get update
sudo apt-get install python3-pip python3-dev vim git -y

sudo npm install -g ganache-cli
pip3 install wheel

cd /audit/badger-system
pip3 install -r requirements.txt
```

## Slither
slither --compile-force-framework brownie .

## Visible Functions
TODO

## Brownie
TODO Property-based and stateful testing

## Dependencies
TODO
OpenZeppelin/openzeppelin-contracts@3.2.0

## Compiler
TODO
solidity ^0.6.0
solidity ^0.6.2

## TODO: Much More
