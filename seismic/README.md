# Seismic Interaction 

Gmic, in this guide we are going to deploy a contract on seismic devnet. This works on Mac, Linux, and Windows via wsl  
Also, check out the official docs at https://docs.seismic.systems/appendix/devnet

**NOTE - This is not incentivized and should be done for fun and learning.**  
## Deploy and encrypted contract

### 1. Install rust  
Install rust by running this command:

    curl https://sh.rustup.rs -sSf | sh  
    
Select option 1 to choose the default installation. After installation run: ```. "$HOME/.cargo/env"```

<hr/>  

### 2. Install jq
For mac 

    brew install jq  

For linux 

    sudo apt-get install jq
    
<hr/>  

### 3. Install sfoundryup
    curl -L \
     -H "Accept: application/vnd.github.v3.raw" \
     "https://api.github.com/repos/SeismicSystems/seismic-foundry/contents/sfoundryup/install?ref=seismic" | bash
     
After installation run the code below
    
    source ~/.bashrc

<hr/>  


### 4. Run sfoundryup
This step requires patience as it could take anywhere from 5-60mins. Stalling at 98% is normal

    sfoundryup

<hr/>  

### 5. Clone repository
first let's clone the repo onto our machine 

    git clone --recurse-submodules https://github.com/SeismicSystems/try-devnet.git

Then we change into the directory  

    cd try-devnet/packages/contract/
<hr/>  

![Screenshot 2025-04-22 071553](https://github.com/user-attachments/assets/878bd63c-ac1b-4751-a81f-2757ab16adec)
### If you come across this error when running the command above, refer to this guide [solve-error](https://github.com/sheriifMahadi/guides/blob/main/seismic/solve-error.md)


### 6. Deploy contract
Then deploy 

    bash script/deploy.sh

## Interact with an encrypted contract

### 1. Install bun

    curl -fsSL https://bun.sh/install | bash

<hr/>  


### 2. Install node dependencies
Change directories 

    cd ~/try-devnet/packages/cli/

Then run 

    bun install

<hr/>  


### 3. Send transaction
    bash script/transact.sh
