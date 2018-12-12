# Contracts

## Graph Protocol Contracts
### Graph DAO Contract ([Governance.sol](./Governance.sol))
- Multi-sig contract governance contract
- Upgrades all Graph smart contracts
- Sets all parameters which are set via governance
- Can be irreversibly replaced or upgraded on it's own authority (i.e. can replace itself).

### Graph Token Contract ([GraphToken.sol](./GraphToken.sol))
- Implements ERC-20 (and what else?)
- Has approved `treasurers` with permission to mint the token (i.e. Payment Channel Hub and Rewards Manager).
- Has `owner` which can set `treasurers`, upgrade contract and set any parameters controlled via governance.

### Staking Contract ([Staking.sol](./Staking.sol))
- Indexing Nodes stake Graph Tokens to participate in the data retrieval market for a specific subgraph, as identified by `subgraphId` .
- Curators stake Graph Tokens to participate in a specific curation market, as identified by `subgraphId`
- Staking amounts must meet criteria specified in technical spec, mechanism design section.

## (WIP...)

## Supporting Contracts
### SafeMath ([SafeMath.sol](./SafeMath.sol))
- Math operations with safety checks that revert on error

### Ownable ([Ownable.sol](./Ownable.sol))
- Owned contract from ERC20 Token Standard