## if you are here then you've come faced problem in deploying the seismic contract. Here is how you can resolve that problem
Follow the steps below and run these commands in your terminal. 

### step 1
    sed -i 's/\bscast\b/cast/g' ../common/wallet.sh

### step 2 
    curl -L foundry.paradigm.xyz | bash

### step 3
    foundryup

### step 4
    export PATH="$HOME/.foundry/bin:$PATH"

### step 5
    echo 'export PATH="$HOME/.foundry/bin:$PATH"' >> ~/.bashrc

### step 6
    source ~/.bashrc

### step 7
    cast --version

if this step doesn't produce an error then you are on the right track

### step 8
    cd ~/try-devnet/packages/contract

### step 9
    bash script/deploy.sh

if you followed all steps carefully you should see a prompt on your screen. 
Follow the guides on your terminal to deploy. Then go back here to interact with the contract

[Seismic interaction](https://github.com/sheriifMahadi/guides/blob/main/seismic/README.md) 
