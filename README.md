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
# first get the latest contribution
$ ls -1 ./participations | tail -n 1
4201_anoynmous.zkey

# do you contribution
# Feel free to put your name / twitter handler / keybase
$ snarkjs zkey contribute ./participations/00xx_anoynmous.zkey ./participations/4202_my_name.zkey --name="My Name" -v
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
| [0001_albttx.zkey](./participations/0000_setup.zkey)  | [@albttx](https://twitter.com/albttx) | `7e29e141 602f3279 3e5265e0 5c4ca815`<br /> `34a6c162 f03af37a 4da84674 0fe7673b` <br /> `959875b8 1b0ecad0 a33592fd f5b5ef52` <br /> `a96036dd 7c1889e9 f451ac6f 6e130a1a`|
