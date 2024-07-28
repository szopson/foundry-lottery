# Proveably Random Raffle Contracts

## About  
This code is to create a proveable random smart contract lottery.

## What we want it to do?

1. Users can enter by paying for a ticket.
    1. The ticket fees are going to go to the winner during the draw.
2. After X period of time, the lottery will automatically draw a winner.
    1. And this will be done programatically.
3. Using Chainlink VRF & Chainlink Automation.
    1. Chainlink VRF => Randomness
    2. Chainlink Automation => Time based trigger

## Tests!
1. Write deploy scripts
    1. Note, these will not work on zkSync
2. Write tests
    1. Local chain
    2. Forked testnet
    3. Forked mainnet

# INSTEAD OF PRIVATE KEY PASSINV IN .ENV FILE WE CAN SET IT UP HERE, LIKE THIS:   
 cast wallet import defaultKey --interactive

!remember the password!

## IF CONTRACT WAS NOT VERIFIED AUTOMATICALLY AFTER DEPLOYMENT TO SEPOLIA YOU CAN USE BELOW COMMAND(use your own contract address!):
forge verify-contract 0xe9D52cB94987eB686351B642479C688797A54cb9 src/Raffle.sol:Raffle --etherscan-api-key $ETHERSCAN_API_KEY --rpc-url $SEPOLIA_RPC_URL --show-standard-json-input > json.json
# YOU CAN MANUALLY UPLOAD json.json into the etherscan contract page 

##### DEPLOYED CONTRACT ADDRESS #####
0xe9D52cB94987eB686351B642479C688797A54cb9