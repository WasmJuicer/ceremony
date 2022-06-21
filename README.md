# WasmJuicer Zero Knowledge Phase-2 Ceremony

## DISCLAIMER

If there is an open PR, please fork off of that branch to preserve the circuit/chain.  Otherwise, any later PRs will be rejected and you will need to redo your entry if you wish to participate.

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
RECENT_ZKEY=$(ls -1 ./participations | tail -n 1)
echo $RECENT_ZKEY
# 4201_anonymous.zkey

# add your contribution
# just add 1 to the previous contribution
# Feel free to put your name / twitter handler / keybase
# Set the name of zkey file. Then set your contributor name
CONTRIBUTION_ID=4202_myname
CONTRIBUTION_NAME="My Name"

# then run the following command
snarkjs zkey contribute ./participations/$RECENT_ZKEY ./participations/$CONTRIBUTION_ID.zkey --name="$CONTRIBUTION_NAME" -v

```

- Verify your contribution

```bash

wget https://hermez.s3-eu-west-1.amazonaws.com/powersOfTau28_hez_final_16.ptau
snarkjs zkey verify ./build/withdraw.r1cs ./powersOfTau28_hez_final_16.ptau "./participations/$CONTRIBUTION_ID.zkey"

```

## Write your contribution

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
| [0011_bongo.zkey](./participations/0011_bongo.zkey) | [@bongo5991](https://twitter.com/bongo5991) | `7696866a 9e7f9278 6fe9b5d7 1ccd67a8`<br/>`433a978d 9de0673d cc69e95e 29907790`<br/>`a7d24fa5 6a0e117f 6b31f9f2 01f5429e`<br/>`8d9ab07a e0f918ab d679433a 32c85afb` |
| [0012_franckwertel.zkey](./participations/0012_franckwertel.zkey) | [@franckwertel](https://twitter.com/franckwertel) | `2a3fe593 c5ad4e6a 83f001e9 ec039d3d`<br/>`c2f8a1e4 71e48d7c b19231b3 758c8d71`<br/>`818ac0d7 d1421adf 0e6047a6 5ff5437e`<br/>`39d87620 f46d449c 1089595b 41029cdc` |
| [0013_poroburu.zkey](./participations/0013_poroburu.zkey) | [@poroburu](https://twitter.com/poroburu) | `274e88b9 03246785 42aacc69 2c02e3a6`<br/>`5dbcb030 722a8841 1728e11e 7cd01434`<br/>`0244b9e1 6471eb6d a95458b2 dc51cb89`<br/>`3e17977a bfa58d37 76b7406b cfe15c47` |
| [0014_stepyt.zkey](./participations/0014_stepyt.zkey) | [@\_stepyt\_](https://twitter.com/_stepyt_) | `e3fbdfe8 68d93782 f60277fe d2d4cc79`<br/>`e10caaad daa96f71 2bef0a7b 313b019e`<br/>`0df19781 584986a1 c98ff682 11cc4a81`<br/>`44ea62ff a6716ebf 6d3c517e cdad3646`
| [0015_elsehow.zkey](./participations/0015_elsehow.zkey) | [@elsehow](https://twitter.com/_elsehow) | `f5bb0bbe 55af18db e921e305 9bdf4b6b` <br/> `3f78c243 5dc60aa1 187150ea 294d438e` <br/> `a4da64b1 d6fc34ea 8f766424 a8fd70c1` <br/> `3ecfc3fd 49970baa 06fd3847 275e2b46`
| [0016_netadev.zkey](./participations/0016_netadev.zkey) | [@netadev](https://github.com/netadev) | `65bf1d29 41f7d05b 6ed21e6c 329bd089` <br/> `4a3f4587 ce9d347f 8ea12a38 1de0a2f3` <br/> `d35bea95 4cadd611 c017fe83 154b8961` <br/> `bb921be1 93408a29 0ce28fa1 8e942ef4`
| [0017_joeabbey.zkey](./participations/0017_joeabbey.zkey) | [@joeabbey](https://github.com/joeabbey) | `a9647982 a57bfea3 c58f84b1 1491dd4b` <br/> `b5155f93 13cadd0f 280f1dd1 c7351b77` <br/> `95d13025 e0233317 a2fa5165 7da79154` <br/> `1f79e712 ac5d5a2d 64d64dca c5e8dabf`
| [0018_nullmames.zkey](./participations/0018_nullmames.zkey) | [@nullmames](https://github.com/nullmames) | `3716bb92 601c64fb 4b1ed247 d492a244` <br/> `fb004999 d9767432 f1d9dc5f 309dcf9d` <br/> `19947958 9c6d278d c9358984 fa68338d` <br/> `d993be47 1a06b4be 7b4789d1 f2f7d851`
| [0019_callum.zkey](./participations/0019_callum.zkey) | [@callum](https://github.com/callum-a) | `ada4288c a006245c 7d866b27 579c3b50` <br/> `2933f1af e72d30eb 464e0d69 e45d3220` <br/> `42de7829 4667a003 415ddbd6 6128b09e` <br/> `7afee047 0e3a2a96 b744b6f1 b99b712a`
| [0020_caneryy.zkey](./participations/0020_caneryy.zkey) | [@caneryy](https://github.com/caneryy) | `6a977644 92633e92 a1590d63 d9603451` <br/> `7f014b83 e931dbeb 402e598d 19526a7c` <br/> `38d6793c 157e99e8 8c18d338 ffcb9645` <br/> `222b57fc 98facb2a ba5ba385 5f285869`
| [0021_aquaonjuno1337.zkey](./participations/0021_aquaonjuno1337.zkey) | [@sascha1337](https://github.com/sascha1337) | `f44ab7be 7816d4ed dbe71b50 d8820ba3` <br/> `273826e5 3d204454 f9346096 982bda2f` <br/> `90978297 54c97f25 b82a27fd 5e746f9b` <br/> `0531c2bd 01864470 9e44a305 1bd4bcb9`
| [0022_nana.zkey](./participations/0022_nana.zkey) | [@nanabonobo7000](https://github.com/nanabonobo7000) | `c1227fda ce4ed6b0 4869b073 544f4744` <br/> `a2b72deb 5979db80 58073b52 b26d063d` <br/> `31627653 ee7de7ec 81af4987 e0fb12d9` <br/> `c00e84dc 7e567ca7 bf928f96 714238c8`
| [0023_dstake.zkey](./participations/0023_dstake.zkey) | [@donadel01](https://github.com/donadel01) | `80300d87 09a2c708 aedb2183 9e24ad88` <br/> `7391b624 0cd8e453 9bb5bd98 ff68989d` <br/> `9b39601d 1702a7e9 b3b4c311 953a35c3` <br/> `48088da7 10038f5a 965d9d58 0e9f006b`
