# EONIA
EONIA is a decentralized real estate platform running on the Internet Computer Blockchain that allows users to tokenize, buy and sell their real estate properties. Introducing 3d scanning with mobile to upload 3d models of the real estate property.

# Issues

1. We are yet to integrate the working front-end with 3D scanning functionalities to the main EONIA website (where it talks with the IC Blockchain through smart contracts written in MOTOKO)

2. For the time being, we are not deploying the 3D image data (Sizes are big and we need to work on the image processing part and figure a way out !!! ) on the IC Blockchain. Only, the 2D image representing the real estate, the NFD ID of the property, and the Principal ID of the owner are recorded on-chain. We are trying to automate the process of generating a 2D image corresponding to the 3D scanned image of the property and deploying that specific information on IC Blockchain

3. We are making PUT and GET requests to spectre3d API and using photogrammetry and machine learning with Spectre3d to convert it into a 3D mesh. For the time being, we are storing the 3D image data on IPFS and later rendering it back from IPFS to the Discover section of the EONIA webpage.


# To Install and Run the EonD MARKETPLACE Project

1. start local dfx

```
    dfx start
```

2. Run Webpack Server

```
    npx webpack
``` 

3. Run NPM server

```
    npm start
```

4. Deploy canisters

The following example mints a hard coded image of a property on the IC Blockchain from the cli

```
    dfx deploy --argument='("MafuzProperty #123", principal "gbdev-tyqsv-hnvqv-7mgz4-4kcfl-wbv6x-6khez-y56gq-uohqs-quomc-uqe", (vec {137; 80; 78; 71; 13; 10; 26; 10; 0; 0; 0; 13; 73; 72; 68; 82; 0; 0; 0; 10; 0; 0; 0; 10; 8; 6; 0; 0; 0; 141; 50; 207; 189; 0; 0; 0; 1; 115; 82; 71; 66; 0; 174; 206; 28; 233; 0; 0; 0; 68; 101; 88; 73; 102; 77; 77; 0; 42; 0; 0; 0; 8; 0; 1; 135; 105; 0; 4; 0; 0; 0; 1; 0; 0; 0; 26; 0; 0; 0; 0; 0; 3; 160; 1; 0; 3; 0; 0; 0; 1; 0; 1; 0; 0; 160; 2; 0; 4; 0; 0; 0; 1; 0; 0; 0; 10; 160; 3; 0; 4; 0; 0; 0; 1; 0; 0; 0; 10; 0; 0; 0; 0; 59; 120; 184; 245; 0; 0; 0; 113; 73; 68; 65; 84; 24; 25; 133; 143; 203; 13; 128; 48; 12; 67; 147; 94; 97; 30; 24; 0; 198; 134; 1; 96; 30; 56; 151; 56; 212; 85; 68; 17; 88; 106; 243; 241; 235; 39; 42; 183; 114; 137; 12; 106; 73; 236; 105; 98; 227; 152; 6; 193; 42; 114; 40; 214; 126; 50; 52; 8; 74; 183; 108; 158; 159; 243; 40; 253; 186; 75; 122; 131; 64; 0; 160; 192; 168; 109; 241; 47; 244; 154; 152; 112; 237; 159; 252; 105; 64; 95; 48; 61; 12; 3; 61; 167; 244; 38; 33; 43; 148; 96; 3; 71; 8; 102; 4; 43; 140; 164; 168; 250; 23; 219; 242; 38; 84; 91; 18; 112; 63; 0; 0; 0; 0; 73; 69; 78; 68; 174; 66; 96; 130;}))'
```

# To Install and Run the EON NFT Token Project

1. Head to localhost
  
    http://localhost:8080/

2. Creating NFT for Testing

3. Mint an NFT on the command line to get NFT into mapOfNFTs:

The following example mints a hard coded image of a property on the IC Blockchain from the CLI.

```
    dfx canister call opend mint '(vec {137; 80; 78; 71; 13; 10; 26; 10; 0; 0; 0; 13; 73; 72; 68; 82; 0; 0; 0; 10; 0; 0; 0; 10; 8; 6; 0; 0; 0; 141; 50; 207; 189; 0; 0; 0; 1; 115; 82; 71; 66; 0; 174; 206; 28; 233; 0; 0; 0; 68; 101; 88; 73; 102; 77; 77; 0; 42; 0; 0; 0; 8; 0; 1; 135; 105; 0; 4; 0; 0; 0; 1; 0; 0; 0; 26; 0; 0; 0; 0; 0; 3; 160; 1; 0; 3; 0; 0; 0; 1; 0; 1; 0; 0; 160; 2; 0; 4; 0; 0; 0; 1; 0; 0; 0; 10; 160; 3; 0; 4; 0; 0; 0; 1; 0; 0; 0; 10; 0; 0; 0; 0; 59; 120; 184; 245; 0; 0; 0; 113; 73; 68; 65; 84; 24; 25; 133; 143; 203; 13; 128; 48; 12; 67; 147; 94; 97; 30; 24; 0; 198; 134; 1; 96; 30; 56; 151; 56; 212; 85; 68; 17; 88; 106; 243; 241; 235; 39; 42; 183; 114; 137; 12; 106; 73; 236; 105; 98; 227; 152; 6; 193; 42; 114; 40; 214; 126; 50; 52; 8; 74; 183; 108; 158; 159; 243; 40; 253; 186; 75; 122; 131; 64; 0; 160; 192; 168; 109; 241; 47; 244; 154; 152; 112; 237; 159; 252; 105; 64; 95; 48; 61; 12; 3; 61; 167; 244; 38; 33; 43; 148; 96; 3; 71; 8; 102; 4; 43; 140; 164; 168; 250; 23; 219; 242; 38; 84; 91; 18; 112; 63; 0; 0; 0; 0; 73; 69; 78; 68; 174; 66; 96; 130;}, "Mafuzproperty #123")'
```

3. List the item into mapOfListings:

```
    dfx canister call opend listItem '(principal "<REPLACE WITH NFT CANISTER ID>", 2)'
```

4. Get OpenD canister ID:

```
    dfx canister id opend

```

5. Transfer NFT to OpenD:

```
    dfx canister call <REPLACE WITH NFT CANISTER ID> transferOwnership '(principal "ryjl3-tyaaa-aaaaa-aaaba-cai", true)'

```

# Videogrammetry : To Install and Run the 3D Scanning & Web3 Storage Project

## Conneting to the Token Canister

1. Copy over the token declarations folder

2. Set the token canister id into the <REPLACE WITH TOKEN CANISTER ID>

```
    const dangPrincipal = Principal.fromText("<REPLACE WITH TOKEN CANISTER ID>");

```

## This repository contains scripts to convert a video of 3d real life objects or places in 3d model using videogrammetry.

The main python script has the following algorithm:

1. User input the required data
2. Make a post request to the spectre3D api with the input video file.
3. Make a get request to spectre3D api to get the status of the processing.
4. If successfully processed, run the javascript program to upload the 3D model generated to the ipfs.
5. After sucessfull upload, we get a confirmation message. 

## To run the script:

```
    python run_api.py

```
## To upload a custom file to the IPFS:

```
    node web3-client.js --token=<api-token> <file>

```    
