<h2 align=center> Nillion Verifier Node Guide </h2>

<p align="center">
<img src='photo_2024-08-29_14-57-45.jpg' style="width:1000px;height:600px;">
</p>


- You can use either VPS or Ubuntu on Windows
- Make sure that you have a nillion address, if u have not, you can install [Keplr](https://chromewebstore.google.com/detail/keplr/dmkamcknogkgcdfhhbddcghachkejeap) and create a nillion address
- Now visit this [website](https://chains.keplr.app) and search `nillion` and add nillion testnet to your keplr wallet
- Open your Keplr wallet, search for `nillion` , u will get your nillion address
- Now request nillion faucet from [here](https://faucet.testnet.nillion.com/)

## 1/ Copy and Past Command Your Terminal (WSL/VPS)

```
wget -q -O nillion.sh https://raw.githubusercontent.com/BidyutRoy2/Nillion-Node/main/nillion.sh && sudo chmod +x nillion.sh && ./nillion.sh
```

## Get Wallet Details Past Command & Import Private In Keplr Wallet

```bash
cat ~/nillion/accuser/credentials.json
```
- Copy Save Your Private key , AccountId , PublicKey & Save NotePad

## Claim Faucet: https://faucet.testnet.nillion.com
- Submit Your Nillion Address & Claim

## Verify Node Go To: https://verifier.nillion.com/verifier

- Connect Keplr Wallet Import From Node Private Key
- Click `Verifier` & `Linux` `5 Initialsing the Accuser`
- Submit your `accound_id` and `public_key`

# Running the accuser: YOU MUST WAIT 30-60 MINUTES TO CONTINUE WITH THE STEPS BELOW. The secret verification is designed wait for a period of time before fully registering the accuser


## Once you have the details required to register the accuser, you can run the accuser in the same directory. Ensure that your accusor has some funds, by going to the Nillion faucet

```
sudo docker run -d --name nillion -v $HOME/nillion/accuser:/var/tmp nillion/retailtoken-accuser:v1.0.0 accuse --rpc-endpoint "https://testnet-nillion-rpc.lavenderfive.com" --block-start 5112621
```

## Check the node logs
```
sudo docker logs -f nillion --tail=50
```

## Check registration status:
```
sudo docker logs --tail=1000000 nillion | grep -A 2 Registered | tail -3
```

## Restart the node:
```
sudo docker restart nillion
```

## Stop the node:
```
sudo docker stop nillion
```

# Done 

## Detele/Remove the node:
```
docker ps - Copy Your Nillion CONTAINER_ID
docker stop DOCKER_CONTAINER_ID
docker rm DOCKER_CONTAINER_ID
rm -rf nillion
```

```
sudo docker rm -f nillion
```



# ▄︻デ𝙂𝙚𝙩 𝙇𝙖𝙩𝙚𝙨𝙩 𝘼𝙞𝙧𝙙𝙧𝙤𝙥𝙨 & 𝙐𝙥𝙙𝙖𝙩𝙚𝙨═━一

### ▄︻デ𝙅𝙤𝙞𝙣 𝙏𝙚𝙡𝙚𝙜𝙧𝙖𝙢═━一 [🎀  𝐻𝒾𝒹𝒹𝑒𝓃 𝒢𝑒𝓂  🎀](https://t.me/hiddengemnews) 

### ░▒▓█►─═  𝓗𝓲𝒹ᗪ𝓔η Ǥέ𝕄 ═─◄█▓▒░
