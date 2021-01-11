# Static Code Analysis

## Preparations
```bash
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

## Modules

 * badger-geyser
 * badger-hunt
 * badger-sett
 * badger-timelock
 * digg-core
 * digg-oracles

Besides that there are various contract-drafts (not covered in this analysis since not production-ready):
 * BadgerGeyser.sol  
 * BadgerTree.sol  
 * BaseStrategy.sol  
 * BaseStrategyV2.sol  
 * Farmer.sol  
 * StrategyDiggLpMetaFarm.sol  
 * StrategySushiBadgerWbtc.sol


## Slither Summary

Due to the project's complexity only high findings are covered and the json output stored in the static_code_analysis folder:
```bash
slither contracts/$MODULE --exclude-low --exclude-informational --exclude-medium --exclude-optimization --exclude-dependencies --json $MODULE.json
```


| Module        | Findings (Confirmed/Potential) |
| ------------- |:---------------:|
| Badger-Geyser  |  0/10         |
| Badger-Hunt  |    0/1      |
| Badger-Sett  |    0/5      |
| Badger-Timelock  |    0/1      |
| Digg-Core  |    0/6      |
| Digg-Oracles (without ConstantOracle) |  0/0        |


## Dependencies
No known vulnerabilities present for contract-dependencies:

 * OpenZeppelin/openzeppelin-contracts@3.2.0

Different compiler-versions used depending on each module, i.e. solidity 0.4.24, 0.6.0, and 0.6.2.
