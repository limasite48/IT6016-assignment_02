### 2. Getting Started
1. done
### 3. Setup
2. done
    * uv run python 'Starter Code\lib\keygen.py'
    my_private_key
        Private key: cP5VdA7kZhZRfiEp7cZUAFuFHA7in1MEZ1LxpGq4GiF91MN667zi
        Address: mmdekQCgsyD5YG8iiRyFXsemEPFqkNiyTn
    alice_secret_key_BTC
        Private key: cVZ1bWVvRKbnFUU9M6Dj8VL3qxajKQ6Ce34VSfBap27ULFQLqs3r
        Address: n44LJkPPckP2SGBqpZA3A1K2xwHBstNCUL
    bob_secret_key_BTC
        Private key: cSSCdPDnP8SiwWuvX6uKRzwYaMip4CSan4ogQaAVVNbvEV67fhLF
        Address: mh2gzMDfrMYAFtBaPjZuL6MDURcFSmWEfg
3. 
    (a) done
    (b) transaction hash / txid : c2ffc17c0f07fb4c9a5b8a48b9b7d344197cb33a29c6794fb1ec60afc142d395
        utxo index : 1
        received : 0.00144290 BTC
4.  
    (a) Token : b17c0b4936644867a537e979c933bf54
    (b) alice_secret_key_BCY
            "private": "c6bc92608dabc814b502ee887090029708f3ead475c35d62c7119e2be20edd42",
            "public": "02f8f38c107ce03e15e4fc6dd0515c8a941a91c72ed68115563a9c6c933d5fca16",
            "address": "CAofujYu7vvyM9Vntvga4gm4fo9Mqe7JRa",
            "wif": "BuzMBXP4rqcRFnM6dnm5UCr5AYQPPdncfRDPdnNMJmeSnTbj9xoW"
        bob_secret_key_BCY
            "private": "9711fcd1bb6ca41669afd684a9485273e321b0544c215711d8045e398cf82a28",
            "public": "024c2a77e4a998905b0c5fc90cf09c00406a00e2cdfceac3f9c582bd4c91098995",
            "address": "ByBgoKj4j8bZ3PR5EnVNRKVWSpYSCmqXu2",
            "wif": "BtPh4tVNMCnsZ1wn4Q3xcHd34ozCWAEQpEnzWoJNiiwpADURJ451"
5.  
    transaction hash / txid : 8bba0bb9fac6d9e2b8f7b591904248c9d4159fbbcb2ec84ee7f8a52e0513dcff
    utxo index : 0
    received : 100000 satoshis (0.001 BCY)
6.  
    transaction hash / txid : 8d48668219904acf656e4b7cbf72d6f6a24906dc0488ddf3a3f6b2dbda8b194b
    number of outputs (n) : 5
    amount per output : 0.0002 BTC (20,000 sats)
    fee : 0.00044290 BTC (44,290 sats)
7.  
    Bob BCY Coins Status:
        Bob already holds 2 unspent UTXOs on BCY Testnet (200,000 satoshis total), sufficient backup outputs for Question 4 without requiring additional split.
        UTXO 1: cd9b7fd253d0da374679e2bfefcb28e7c31963bdaacd56ca28f8308cbc8c6315 (output 0, 100000 sats)
        UTXO 2: 8bba0bb9fac6d9e2b8f7b591904248c9d4159fbbcb2ec84ee7f8a52e0513dcff (output 0, 100000 sats)
    Alice BTC Coins Status:
        Alice's keys and address are configured. Question 4 verifies locally via `broadcast_transactions = False` (offline evaluation), no live chain spend needed.

8.  
    Verification Checklist:
    - [x] Bitcoin Testnet addresses created for User, Alice, and Bob.
    - [x] User has 5 spendable UTXOs on Bitcoin Testnet (0.0002 BTC each).
    - [x] BlockCypher Testnet addresses created for Alice and Bob.
    - [x] Bob has 200,000 satoshis on BlockCypher Testnet.
    - [x] Setup completed successfully. Ready for Exercise 1 (Q1.py).
### 4. Questions
* exercise 1:
    transaction hash / txid : <04390b9e6b5207e30cf9bf56710ecafe94e9acfc1ccce9ad02146c0e85600a33>
    amount sent : 0.0001 BTC (10,000 sats)
    fee : 0.0001 BTC (10,000 sats)
    recipient : faucet_address (mohjSavDdQYHRYXcS3uS6ttaHP8amyvX78)
    status : 200 OK
* exercise 2:
    (a) Transaction ID (txid): 872b74e392fec699060beb5e3b8a5cd840bc7021bf5e7c6ed708dd72d6e559c7
        400 Bad Request
        sendrawtransaction RPC error -26: scriptpubkey
    (b) Transaction ID (txid): 49e721cc8fa890e34d3f7a32f42b42a40d1cd4cfeb63b97bb89da00a09f0cacd
        400 Bad Request
        sendrawtransaction RPC error -25: bad-txns-inputs-missingorspent
* exercise 3:
    (a) cust1_private_key : cPincwYEnMKyEPoLJnkYTxHAuDY55FDPg1u8SSc9GeXrPSv3AyS4
        cust2_private_key : cQM6uUnZrrppLoVfpF5wm9VLxUcqHru7NqTt4V9JdddgkBZx39yX
        cust3_private_key : cQ36KsTtzjtDYWpXQJrPfFiPuRofUNTxxEcNvmWVuDdcSYbAVPGH
        Transaction ID (txid): deb66423509c576b2e4596a3c9afdf9c7a5d9368f920c93e3477d2ebe61ec770
    (b) Transaction ID (txid): 71099ca3c8361d6112be508befdbd1c1fe99a03ec54d6ee8e4a8f2600e21f09a
* exercise 4:
    (a) Configuration & Scripts:
        - coinExchangeScript implemented in Q4.py (OP_IF with OP_HASH160 & OP_CHECKSIG; OP_ELSE with 2-of-2 OP_CHECKMULTISIG).
        - coinExchangeScriptSig1 implemented in Q4.py ([sig_recipient, secret, OP_TRUE]).
        - coinExchangeScriptSig2 implemented in Q4.py ([OP_0, sig_sender, sig_recipient, OP_FALSE]).
        - broadcast_transactions = False (offline evaluation mode per handout).
    (b) Test Case 1 (alice_redeems = True):
        - Status: PASSED
        - Output:
            Alice swap tx (BTC) created successfully!
            Bob swap tx (BCY) created successfully!
            Alice redeem from swap tx (BCY) created successfully!
            Bob redeem from swap tx (BTC) created successfully!
    (c) Test Case 2 (alice_redeems = False):
        - Status: PASSED
        - Output:
            Alice swap tx (BTC) created successfully!
            Bob swap tx (BCY) created successfully!
            Bob return coins (BCY) tx created successfully!
            Alice return coins tx (BTC) created successfully!
    (d) Design Document:
        - docs/Q4design_doc.txt completed explaining ScriptPubKey, atomic swap architecture, refund guarantees, and why 1-of-2 multisig is insufficient.