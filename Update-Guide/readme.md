<h2 align=center>Nillion Verifier Node Guide Update</h2>

# If You Already Installed But Show Fasle Delete Old Images and Container Then Run Node Again

## How to Delete Docker Node Installed File

Check List > `docker ps -a`

Stop Containers > `docker stop <Nillion_container_id>`

Remove Containers > `docker rm <Nillion_container_id>`

List All Images > `docker images -a`

Remove Images > `docker rmi <Nillion_image_id>`

<details>
  <summary><b>Example</b></summary>
  <ul>
    <code>docker stop 88f734545bc8</code>
    <br>
    <code>docker rm 88f734545bc8</code>
    <br>
    <code>docker rmi d1cc47dd3dec</code>
  </ul>
</details>


- You can use either VPS or Ubuntu on Windows
- Ubuntu troubleshooting related video is [here](https://x.com/ZunXBT/status/1827779868630876651)
- Make sure that you have a nillion address, if u have not, you can install [Keplr](https://chromewebstore.google.com/detail/keplr/dmkamcknogkgcdfhhbddcghachkejeap) and create a nillion address
- Open your Keplr wallet, search for `nillion`, click on manage chain and the add nillion testnet to your Keplr wallet
- Copy this nillion address from Keplr
- Now request nillion faucet from [here](https://faucet.testnet.nillion.com/)
- Use this command to install docker on your system
```bash
sudo apt update && sudo apt install curl && curl -fsSL https://get.docker.com -o get-docker.sh && sudo sh get-docker.sh
```
- Use this command to pull nillion accuser image
```bash
sudo docker pull nillion/retailtoken-accuser:latest
```
- Use the below command to create a directory and to initialise the accuser
```bash
mkdir -p nillion/accuser && sudo docker run -v ./nillion/accuser:/var/tmp nillion/retailtoken-accuser:latest initialise
```
- After executing the above command, you will see `accound_id` and `public_key` in your terminal, copy the value
- Now visit [this site](https://verifier.nillion.com/verifier), submit your `accound_id` and `public_key` in the appropriate field
- Visit [faucet site](https://faucet.testnet.nillion.com/) to request faucet in your `account_id` you copied earlier
- Now run this command to get your accuser wallet private key
```bash
cat ~/nillion/accuser/credentials.json
```
- Copy the private key and save it, if you lose, you will not regain access to your accuser wallet
---
<h2 align=center>NOW TAKE A BREAK FOR 60 MINS</h2>

---
- After 60 mins, run these 2 final commands
- Install `jq` now
```bash
sudo apt update && sudo apt install jq
```
```bash
sudo docker run -v ./nillion/accuser:/var/tmp nillion/retailtoken-accuser:latest accuse --rpc-endpoint "https://testnet-nillion-rpc.lavenderfive.com/" --block-start "$(curl -s https://testnet-nillion-rpc.lavenderfive.com/abci_info | jq -r '.result.response.last_block_height')"
```


# ▄︻デ𝙂𝙚𝙩 𝙇𝙖𝙩𝙚𝙨𝙩 𝘼𝙞𝙧𝙙𝙧𝙤𝙥𝙨 & 𝙐𝙥𝙙𝙖𝙩𝙚𝙨═━一

### ▄︻デ𝙅𝙤𝙞𝙣 𝙏𝙚𝙡𝙚𝙜𝙧𝙖𝙢═━一 [🎀  𝐻𝒾𝒹𝒹𝑒𝓃 𝒢𝑒𝓂  🎀](https://t.me/hiddengemnews) 

### ░▒▓█►─═  𝓗𝓲𝒹ᗪ𝓔η Ǥέ𝕄 ═─◄█▓▒░
