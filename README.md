### Ordinal Demo


The `token.json` looks like:

```js
p: Protocol name (brc-20).
op: Operation type (deploying a token, minting, or transferring).
tick: Token ticker (up to 4 characters).
max: Maximum supply of tokens.
lim: Maximum tokens a single user can mint per transaction.
```

#### Note: Make sure you have `ord` installed:

```sh
curl --proto '=https' --tlsv1.2 -fsLS https://ordinals.com/install.sh | bash -s
```


### Ord command

```sh
ord wallet inscribe token.json --fee-rate 10 --destination bc1q4hgfz3teart92zxcgr6xduj4uj8xkwzg6r28k2 
```

```js
ord wallet inscribe: Instructs the ord tool to create an inscription.
token.json: Path to your JSON manifest file.
--fee-rate: Sets the fee rate (higher ensures faster confirmation).
--destination: Your Bitcoin wallet address to receive the inscription.
```

- After the inscription is mined into a Bitcoin block, you’ll receive a unique Ordinal inscription ID.
- Use the Ordinals explorer (like https://ordinals.com) to track your inscription and verify it on-chain.

- One example of an ordinal with an ID `f7fbabb618a35ea2f733ea89a6fd51864d4d58f38eb3bbb1ce67685d4b3a921ci0` is:
https://ordinals.com/inscription/f7fbabb618a35ea2f733ea89a6fd51864d4d58f38eb3bbb1ce67685d4b3a921ci0

By clicking this you can check the ordinal on the ordinal explorer.


#### Inscribe the mint

```sh
ord wallet inscribe mint.json --fee-rate 10 --destination <your_wallet_address>
``` 

#### Transferring the BRC-20 Tokens

```sh
ord wallet inscribe transfer.json --fee-rate 10 --destination <recipient_wallet_address>
```