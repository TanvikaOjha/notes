# Ethereum Accounts

Ethereum has two types of accounts:

1. **Externally Owned Accounts(EOAs)**: An EOA is an account comprising a cryptographic pair of keys: public and private. The public key is used to verify that the EOA transaction was signed by the sender, and the private key is used to sign the transaction.Access to private key gives access to and control of the account(funds and assests too). Metamask, Coinbase wallet are examples of EOA. 
   - no batching of transaction
   - an ETH balance always required to pay transaction fees.


2. **Smart Contract Accounts(CAs)**: These are programmable accounts on the blockchain. They are deployed as smart contracts. Safe and Argent are some examples of CAs.
   yet these stil depend on EOAs to initiate transactions.
   - define your own flexible security rules
   - recover your account if you loose the key
   - multi-sig
   - batch transaction together
   - better UX
   - pay each others' gas fees(gas sponsorship)


It is still too complex to use ethereum for most people.There must be a frictionless way for a user to take custody of their own assets and keep control of their data whithout having to understand public-private key cryptography and key management.

 Athough smart contract wallet exixts today, they are awkward to use build because the ethereum protool needs to support them better. This additional support is known as account abstraction.

 Account abstraction allows smart contracts to initiate transaction themselves, so any logic that the user wishes to implement can be coded in the SM wallet itself and executed on ethereum.