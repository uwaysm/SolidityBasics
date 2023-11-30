# Deploying a contract via Ganache:

1. `cat /etc/resolv.conf`

To get the 'nameserver'

forge create --rpc-url http://[nameserver]:[Ganache Port] [Contract Name] --interactive

forge script script/DeploySimpleStorage.s.sol --rpc-url http://172.23.144.1:8545 --broadcast --private-key 0xd5156970b62d718079f49944ea7f9dbb8f8b6099cbc2a4c884ed5258091aa0f0

# Using functions:

source .env

cast send 0x683192e5C0d276c6d023837db6BfE5877ee2A8ea "store(uint256)"
--rpc-url $RPC_URL --private-key $PRIVATE_KEY

cast call 0xD949ba04e0E63750915C3Bfe18a33D3829723a2e "retrieve()" --rpc-url $RPC_URL
