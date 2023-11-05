# Pallet
The `Kogarashi Network` supports privacy-preserving transactions. These functionalities are powered by `pallets`. Followings are short summary of pallets.

## [Pallet Functionalities](https://github.com/KogarashiNetwork/Kogarashi/tree/master/pallets)

|Name|Documentation|Description|
|----|-------------|-----------|
| [`pallet-plonk`] | [Plonk Tutorial](https://kogarashinetwork.github.io/Kogarashi/plonk_pallet/) |$gen(d) \rightarrow srs,\ com(f, srs) \rightarrow commitment,\ V_{PC} \rightarrow acc\ or\ rej$|
| [`pallet-encrypted-balance`] |-|$get(address) \rightarrow (g^{r + r'}, g^{a + c} * b^{r + r'})$|
| [`confidential_transfer`] | [Confidential Transfer Tutorial](https://kogarashinetwork.github.io/Kogarashi/confidential_transfer/) |$C = g^{b^\star}y^r \land \hat C = g^{b^\star} \hat y^r \land D = g^r \land C_L/C = g^{b'}(C_R/D)^{sk} \land y = g^{sk} \land b^\star \in [0, MAX] \land b' \in [0,MAX] $|

## [pallet-plonk](https://github.com/KogarashiNetwork/Kogarashi/tree/master/pallets/plonk) [![crates.io badge](https://img.shields.io/crates/v/plonk-pallet.svg)](https://crates.io/crates/plonk-pallet)


The `pallet-plonk` pallet is a wrapper of plonk library and in charge of proving and verifying the validity of computation.

You can find tutorial [here](https://kogarashinetwork.github.io/Kogarashi/tutorial/plonk_pallet/).

## [pallet-encrypted-balance](https://github.com/KogarashiNetwork/Kogarashi/tree/master/pallets/encrypted_balance)

The `pallet-encrypted-balance` pallet provides balance encryption by default. This replaces balance storage value with encrypted value.

## [confidential_transfer](https://github.com/KogarashiNetwork/Kogarashi/tree/master/pallets/confidential_transfer)

The `confidential_transfer` pallet provides transfer function with hiding transfer amount. This pallet is coupling `pallet-plonk` and `pallet-encrypted-balance`, and changes the balance with encryped and checks the validity of computation.

You can find tutorial [here](https://kogarashinetwork.github.io/Kogarashi/tutorial/confidential_transfer_pallet/).

[//]: # (pallet functionalities)

[`pallet-plonk`]: https://github.com/KogarashiNetwork/Kogarashi/tree/master/pallets/plonk
[`pallet-encrypted-balance`]: https://github.com/KogarashiNetwork/Kogarashi/tree/master/pallets/encrypted_balance
[`confidential_transfer`]: https://github.com/KogarashiNetwork/Kogarashi/tree/master/pallets/confidential_transfer
