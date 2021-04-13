# Frontier Chain Testnet: Black Mamba 0

This will be the first public testnet for Frontier Chain, a public blockchain for managing DeFi positions across various protocols without compromising safety or security.

Please put gentxs in the `gentxs` folder within this directory.


## TLDR to submit a gentx:

```
chain-id: frontchain-testnet-1
gentx-amount: 1000000000000front
front version: v0.1.0
genesis-time: 2021-04-14T15:00:00Z
```

## Instructions to install Frontier Chain and submit a gentx:

__Note__: Requires golang 1.15+

```
# clone the frontier chain repo
git@github.com:frontierdotxyz/frontier.git
# install
cd frontier && git checkout v0.1.0 && make install

# initialize chain
frontd init my_node --chain-id frontchain-testnet-1

# Add validator key
frontcli config keyring-backend test
frontcli keys add validator

# Create gentx
frontd add-genesis-account $(frontcli keys show validator -a) 1000000000000front
frontd gentx --name validator --amount 1000000000000front --keyring-backend test
```

## Genesis Details

```
genesis hash: PLACEHOLDER
seeds: PLACEHOLDER
persistent peers: PLACEHOLDER
```