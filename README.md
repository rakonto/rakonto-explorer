# Rakonto Explorer

## About

This is the front-end to be able to search and verify Rakonto transactions. This front-end makes use of an open-source nodejs based back-end service called **Insight**. We run this on the same production server as this front-end code. Insight makes use of a full Litecoin node (again on the same machine).

See the following for more info on Insight:

- <https://github.com/litecoin-project/insight-lite-api>
- <https://github.com/litecoin-project/insight-lite-ui>
- <https://github.com/litecoin-project/litecore-node>


## Running the site

Local development environment:

```
npm run dev
```

Build for production:

```
npm run build
```


## Insight API endpoints

<https://explorer.rakonto.net/api>

#### Get address details

Example get request:

<https://explorer.rakonto.net/api/addr/mseL2Hyf8N1dLu1wTMdRgKTVrmJdn5eBoG/?noTxList=1>

Returns:

```json
{
    "addrStr": "mseL2Hyf8N1dLu1wTMdRgKTVrmJdn5eBoG",
    "balance": 0.0003,
    "balanceSat": 30000,
    "totalReceived": 0.0003,
    "totalReceivedSat": 30000,
    "totalSent": 0,
    "totalSentSat": 0,
    "unconfirmedBalance": 0,
    "unconfirmedBalanceSat": 0,
    "unconfirmedTxApperances": 0,
    "txApperances": 2
}
```

#### Get transactions by address

Example get request:

<https://explorer.rakonto.net/api/txs?address=mseL2Hyf8N1dLu1wTMdRgKTVrmJdn5eBoG&pageNum=0>

```json
{
    "pagesTotal": 1,
    "txs": [
        {
            "txid": "dc21c22c927690b879a3505fe20a99d53970af5e708f25e76f73410ea693e14c",
            "version": 1,
            "locktime": 0,
            "vin": [
                {
                    "txid": "87fcef986a16f470096c14a906c0755c8420e311449989c81c1f27c08ffd53f0",
                    "vout": 2,
                    "sequence": 4294967295,
                    "n": 0,
                    "scriptSig": {
                        "hex": "483045022100e7b60bf83e32dd76e64e9c721e737d61e0a742e204d02bf2a771aba96aa557f102207a14fa8c8d79c119f0be443fff2a21e771485df94e15dc30e06ee2435450ca88012102aefb2d558f356681b7970b831b07ee01ee1d191ddb8ea5af03cbecc08b56b3b8",
                        "asm": "3045022100e7b60bf83e32dd76e64e9c721e737d61e0a742e204d02bf2a771aba96aa557f102207a14fa8c8d79c119f0be443fff2a21e771485df94e15dc30e06ee2435450ca88[ALL] 02aefb2d558f356681b7970b831b07ee01ee1d191ddb8ea5af03cbecc08b56b3b8"
                    },
                    "addr": "n4ozPoV7gQo9mgia8mJGHax2HpmyjKpePU",
                    "valueSat": 999885000,
                    "value": 9.99885,
                    "doubleSpentTxID": null
                }
            ],
            "vout": [
                {
                    "value": "0.00015000",
                    "n": 0,
                    "scriptPubKey": {
                        "hex": "76a91485068f1970a315bb453ebec47f3a7ee3c52abd1488ac",
                        "asm": "OP_DUP OP_HASH160 85068f1970a315bb453ebec47f3a7ee3c52abd14 OP_EQUALVERIFY OP_CHECKSIG",
                        "addresses": [
                            "mseL2Hyf8N1dLu1wTMdRgKTVrmJdn5eBoG"
                        ],
                        "type": "pubkeyhash"
                    },
                    "spentTxId": null,
                    "spentIndex": null,
                    "spentHeight": null
                },
                {
                    "value": "0.00000000",
                    "n": 1,
                    "scriptPubKey": {
                        "hex": "6a0a68656c6c6f776f726c64",
                        "asm": "OP_RETURN 68656c6c6f776f726c64"
                    },
                    "spentTxId": null,
                    "spentIndex": null,
                    "spentHeight": null
                },
                {
                    "value": "9.99770000",
                    "n": 2,
                    "scriptPubKey": {
                        "hex": "76a914ff83b774b0e8cf82f80bb5ea17342b5a67bf9d6088ac",
                        "asm": "OP_DUP OP_HASH160 ff83b774b0e8cf82f80bb5ea17342b5a67bf9d60 OP_EQUALVERIFY OP_CHECKSIG",
                        "addresses": [
                            "n4ozPoV7gQo9mgia8mJGHax2HpmyjKpePU"
                        ],
                        "type": "pubkeyhash"
                    },
                    "spentTxId": null,
                    "spentIndex": null,
                    "spentHeight": null
                }
            ],
            "blockhash": "c3aee3ea845d8997b2bab9fd96f2cf97a381f1b55613eb823d623198cc802679",
            "blockheight": 287241,
            "confirmations": 38,
            "time": 1513180960,
            "blocktime": 1513180960,
            "valueOut": 9.99785,
            "size": 247,
            "valueIn": 9.99885,
            "fees": 0.001
        },
        {
            "txid": "87fcef986a16f470096c14a906c0755c8420e311449989c81c1f27c08ffd53f0",
            "version": 1,
            "locktime": 0,
            "vin": [
                {
                    "txid": "3e692c5bf3b364a4ad098231e1c5b5c7deb06c6176e35971804d3c63d742f166",
                    "vout": 0,
                    "sequence": 4294967295,
                    "n": 0,
                    "scriptSig": {
                        "hex": "483045022100930f0a06fc0c142f738533b502d7cf9398a894f91d33a55d01380372830b88190220682f75077748ef562c6365314b965ceee8e5cc9db958c2fde75324c9db452a47012102aefb2d558f356681b7970b831b07ee01ee1d191ddb8ea5af03cbecc08b56b3b8",
                        "asm": "3045022100930f0a06fc0c142f738533b502d7cf9398a894f91d33a55d01380372830b88190220682f75077748ef562c6365314b965ceee8e5cc9db958c2fde75324c9db452a47[ALL] 02aefb2d558f356681b7970b831b07ee01ee1d191ddb8ea5af03cbecc08b56b3b8"
                    },
                    "addr": "n4ozPoV7gQo9mgia8mJGHax2HpmyjKpePU",
                    "valueSat": 1000000000,
                    "value": 10,
                    "doubleSpentTxID": null
                }
            ],
            "vout": [
                {
                    "value": "0.00015000",
                    "n": 0,
                    "scriptPubKey": {
                        "hex": "76a91485068f1970a315bb453ebec47f3a7ee3c52abd1488ac",
                        "asm": "OP_DUP OP_HASH160 85068f1970a315bb453ebec47f3a7ee3c52abd14 OP_EQUALVERIFY OP_CHECKSIG",
                        "addresses": [
                            "mseL2Hyf8N1dLu1wTMdRgKTVrmJdn5eBoG"
                        ],
                        "type": "pubkeyhash"
                    },
                    "spentTxId": null,
                    "spentIndex": null,
                    "spentHeight": null
                },
                {
                    "value": "0.00000000",
                    "n": 1,
                    "scriptPubKey": {
                        "hex": "6a0568656c6c6f",
                        "asm": "OP_RETURN 68656c6c6f"
                    },
                    "spentTxId": null,
                    "spentIndex": null,
                    "spentHeight": null
                },
                {
                    "value": "9.99885000",
                    "n": 2,
                    "scriptPubKey": {
                        "hex": "76a914ff83b774b0e8cf82f80bb5ea17342b5a67bf9d6088ac",
                        "asm": "OP_DUP OP_HASH160 ff83b774b0e8cf82f80bb5ea17342b5a67bf9d60 OP_EQUALVERIFY OP_CHECKSIG",
                        "addresses": [
                            "n4ozPoV7gQo9mgia8mJGHax2HpmyjKpePU"
                        ],
                        "type": "pubkeyhash"
                    },
                    "spentTxId": "dc21c22c927690b879a3505fe20a99d53970af5e708f25e76f73410ea693e14c",
                    "spentIndex": 0,
                    "spentHeight": 287241
                }
            ],
            "blockhash": "6d8a6bfaed14832259f68472c6876eade00073a974ab49ac00351cadbbbb20bb",
            "blockheight": 287232,
            "confirmations": 47,
            "time": 1513179239,
            "blocktime": 1513179239,
            "valueOut": 9.999,
            "size": 242,
            "valueIn": 10,
            "fees": 0.001
        }
    ]
}
```

