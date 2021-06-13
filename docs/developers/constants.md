---
id: constants
title: Constants
---

Elrond uses some constants, which are specific to each chain (mainnet, testnet or devnet). The updated values can be found at these sources:

**Mainnet**:
- https://gateway.elrond.com/network/config
- https://github.com/ElrondNetwork/elrond-config-mainnet

**Testnet**:
- https://testnet-gateway.elrond.com/network/config
- https://github.com/ElrondNetwork/elrond-config-testnet

**Devnet**:
- https://devnet-gateway.elrond.com/network/config
- https://github.com/ElrondNetwork/elrond-config-devnet

At the time of writing, the most used constants values for mainnet were:

- Round duration: 6 seconds
- Epoch duration: 14400 rounds, 24 hours
- Min gas price: 1000000000
- Min gas limit: 50000
- Chain ID: `1` (`T` for Testnet, `D` for Devnet)
- Min deposit for the creation of a system delegation smart contract: 1250 EGLD
- Min deposit for a validator: 2500 EGLD
- Number of eligible validators per shard: 400 validators
- Number of eligible validators per metachain: 400 validators
- Max number of active (eligible + waiting) validators: 3200 validators
- Consensus group size on shard: 63 validators
- Consensus group size on metachain: 400 validators
- Min deposit for staking provider: 1 EGLD
- Min deposit for legacy delegation: 10 EGLD
- Unbonding duration for legacy delegation: 144000 blocks
- Unbonding duration for staking providers: 10 epochs
- EGLD denomination: 18
