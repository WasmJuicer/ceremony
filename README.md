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
RECENT_ZKEY=$(cd ./participations && ls -1 *.zkey | tail -n 1 && cd ..)
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

## Now what?

Create a secret gist using the github account you used to create the PR with your Juno address in it and send the link over to [@JunoJuicer](https://twitter.com/JunoJuicer) on Twitter or DM whiskey#5193 on Discord with the link!

More info via this [Twitter post](https://twitter.com/JunoJuicer/status/1544733705297707016?s=20&t=Ty0CUVDZExKIKqD6lbDDKA)

## Write your contribution

Add your contribution to the [/participations/README.md](/participations/README.md) file.
