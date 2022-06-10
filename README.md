# WasmJuicer Zero Knowledge Phase-2 Ceremony

## How to participate

- Install [snarkjs](https://github.com/iden3/snarkjs)

```bash
npm install -g snarkjs
# or
yarn global install snarkjs
````

- Do your contribution

```bash
# first get the latest contribution number
$ ls -1 ./participations | tail -n 1
4201_anonymous.zkey

# add your contribution
# just add 1 to the previous contribution
# Feel free to put your name / twitter handler / keybase

# First set the name
$ CONTRIBUTION_ID=4202_myname

# then run the following command
$ snarkjs zkey contribute ./participations/4201_anonymous.zkey ./participations/$CONTRIBUTION_ID.zkey --name="My Name" -v
```

- Verify your contribution

```bash
$ wget https://hermez.s3-eu-west-1.amazonaws.com/powersOfTau28_hez_final_16.ptau
$ snarkjs zkey verify ./build/withdraw.r1cs ./powersOfTau28_hez_final_16.ptau "./participations/4202_my_name.zkey"
```

- Write your contribution

| Contribution File | Contributor | Contribution Hash |
|------------------ |-------------|--------------------------------------|
| [0000_setup.zkey](./participations/0000_setup.zkey)  | Anonymous | `0e4908e1 992c1b4b 34e84512 786f229e`<br /> `28d94625 c87d8739 1ccb1895 6310a0a9` <br /> `7f53236e 3f2a076b 43662f8d b7c85ed0` <br /> `858d18c0 6dfdb243 36aad7fb 584ece78` |
| [0001_albttx.zkey](./participations/0001_albttx.zkey)  | [@albttx](https://twitter.com/albttx) | `7e29e141 602f3279 3e5265e0 5c4ca815`<br /> `34a6c162 f03af37a 4da84674 0fe7673b` <br /> `959875b8 1b0ecad0 a33592fd f5b5ef52` <br /> `a96036dd 7c1889e9 f451ac6f 6e130a1a`|
| [0002_teddav.zkey](./participations/0002_teddav.zkey)  | [@0xteddav](https://twitter.com/0xteddav) | `7bd3b81e a11f7c3d ca53c866 7977d274`<br /> `403ef969 63de8d42 e0894fbd 53b2ff50` <br /> `6143dd40 371b10cc 463bbadf e15cb99d` <br /> `bb4fd70d 64abb7ef b0fe75aa 39d272df`|
| [0003_astaluego.zkey](./participations/0003_astaluego.zkey)  | [@astaluego](https://github.com/astaluego) | `1fe365de e5188405 0cb2ba4c 8a3d97bd`<br /> `93bb8418 caa15b4c 0f7be942 b2b0c2a5`<br />`cdc5d49c 7045c8b0 7656fc56 63e48921`<br />`65946004 c1ad9a59 427913d9 c78b944b` |
| [0004_whiskey.zkey](./participations/0004_whiskey.zkey) | [@whiskeydev_](https://twitter.com/whiskeydev_) | `56fa7552 08c8930c ab57d7dd f375d6ac`<br/>`3bd0902a a291784f 9a29458c 40c7156f`<br/>`42b4ee12 e728ca03 ab7de3a9 569b411e`<br/>`f68f075f ca3602b6 da0fe0e7 1d4cb24b` |
