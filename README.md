# WasmJuicer Zero Knowledge Phase-2 Ceremony

## How to participate

- Install [snarkjs](https://github.com/iden3/snarkjs)

```bash
sudo npm install -g snarkjs
# or
sudo yarn global add snarkjs
````

- Clone repository
```bash
cd $HOME
git clone https://github.com/WasmJuicer/ceremony.git
cd ceremony
```

- Do your contribution

```bash
# first get and set the latest contribution number to the RECENT_ZKEY var
$ RECENT_ZKEY=$(ls -1 ./participations | tail -n 1)
$ echo $RECENT_ZKEY
4201_anonymous.zkey

# add your contribution
# just add 1 to the previous contribution
# Feel free to put your name / twitter handler / keybase
# Set the name of zkey file. Then set your contributor name
$ CONTRIBUTION_ID=4202_myname
$ CONTRIBUTOR_NAME="My Name"

# then run the following command
$ snarkjs zkey contribute ./participations/$RECENT_ZKEY ./participations/$CONTRIBUTION_ID.zkey --name="$CONTRIBUTOR_NAME" -v
```

- Verify your contribution

```bash
$ wget https://hermez.s3-eu-west-1.amazonaws.com/powersOfTau28_hez_final_16.ptau
$ snarkjs zkey verify ./build/withdraw.r1cs ./powersOfTau28_hez_final_16.ptau "./participations/$CONTRIBUTION_ID.zkey"
```

- Write your contribution

| Contribution File | Contributor | Contribution Hash |
|------------------ |-------------|--------------------------------------|
| [0000_setup.zkey](./participations/0000_setup.zkey)  | Anonymous | `0e4908e1 992c1b4b 34e84512 786f229e`<br /> `28d94625 c87d8739 1ccb1895 6310a0a9` <br /> `7f53236e 3f2a076b 43662f8d b7c85ed0` <br /> `858d18c0 6dfdb243 36aad7fb 584ece78` |
| [0001_albttx.zkey](./participations/0001_albttx.zkey)  | [@albttx](https://twitter.com/albttx) | `7e29e141 602f3279 3e5265e0 5c4ca815`<br /> `34a6c162 f03af37a 4da84674 0fe7673b` <br /> `959875b8 1b0ecad0 a33592fd f5b5ef52` <br /> `a96036dd 7c1889e9 f451ac6f 6e130a1a`|
| [0002_teddav.zkey](./participations/0002_teddav.zkey)  | [@0xteddav](https://twitter.com/0xteddav) | `7bd3b81e a11f7c3d ca53c866 7977d274`<br /> `403ef969 63de8d42 e0894fbd 53b2ff50` <br /> `6143dd40 371b10cc 463bbadf e15cb99d` <br /> `bb4fd70d 64abb7ef b0fe75aa 39d272df`|
| [0003_astaluego.zkey](./participations/0003_astaluego.zkey)  | [@astaluego](https://github.com/astaluego) | `1fe365de e5188405 0cb2ba4c 8a3d97bd`<br /> `93bb8418 caa15b4c 0f7be942 b2b0c2a5`<br />`cdc5d49c 7045c8b0 7656fc56 63e48921`<br />`65946004 c1ad9a59 427913d9 c78b944b` |
| [0004_whiskey.zkey](./participations/0004_whiskey.zkey) | [@whiskeydev_](https://twitter.com/whiskeydev_) | `56fa7552 08c8930c ab57d7dd f375d6ac`<br/>`3bd0902a a291784f 9a29458c 40c7156f`<br/>`42b4ee12 e728ca03 ab7de3a9 569b411e`<br/>`f68f075f ca3602b6 da0fe0e7 1d4cb24b` |
| [0005_polkachu.zkey](./participations/0005_polkachu.zkey)   | [@polka_chu](https://twitter.com/polka_chu)      | `f4bd4491 c4ef1051 28dae50c 4952e845`<br/>`18bbbcd3 aef6ed2a e4d84ec0 0ca64614`<br/>`47d0828b f851c191 b8534415 8566e8a1`<br/>`12fee31f 30326d38 2190ca69 65cb3605`         |
| [0006_dimi.zkey](./participations/0006_dimi.zkey)   | [@dimiandre](https://twitter.com/dimiandre)      | `5b3cb795 d54411b7 dd05c166 d786d6c6`<br/>`e72e2dbf d41e9498 fa6e5bbe c2ae881e`<br/>`a8de2439 f83bd3d9 5c3a257e b246e84d`<br/>`c3158266 9a6d60a7 3be8e30f 1b2eb84c`         |
| [0007_nodesguru.zkey](./participations/0007_nodesguru.zkey) | [@NodesGuru](https://twitter.com/NodesGuru) | `cb26d431 af0e8d35 571a04c7 b7586aeb`<br/>`e0c60715 e5403f03 872cadec c09ecc2b`<br/>`96048dcb 2f10c6c7 11281f69 562f6e97`<br/>`dbf56110 4d96d06b 3a5b41aa 42e402c3` |
| [0008_NodeStake.zkey](./participations/0008_NodeStake.zkey) | [@Nodestake_top](https://twitter.com/Nodestake_top) | `71e92dab 5a4aa956 e0fdccdc 1e77738c`<br/>`0c5be377 88d3b590 cae58956 377a10eb`<br/>`ed5418d8 eb0492a1 2532d09f 2c66ea78`<br/>`d9e633b6 c566a99c 73c357c6 8bac1746` |
| [0009_massv.zkey](./participations/0009_massv.zkey) | [@Massv](https://github.com/Massvdev) | `026de6ce 89798905 cd11d4ad fadb48d5`<br/>`d00db0e4 8361f974 f1367a56 91d2c49e`<br/>`4f48f46c 2cbf8978 dbe25bd0 a1832967`<br/>`2a682458 49544e64 185a6bd6 c3b14013` |
| [0010_wtrsld.zkey](./participations/0010_wtrsld.zkey) | [@beholdidols](https://twitter.com/beholdidols) | `f7300bbe ea1486b5 1abcabe0 1334826f`<br/>`3c541f50 49bfcf3a 03d7c39a 40ba9163`<br/>`0c6fe256 36f4f73a c5dc7bd2 1e327fe0`<br/>`b4cf11b2 e173f2cb 344070c4 0989262e` |
