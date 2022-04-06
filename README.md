
# RAILGUN Trusted Setup Ceremony: How to Contribute Guide

First of all, reach us in the [RAILGUN Phase-2 Ceremony Telegram group](https://t.me/+moI-BUoCLMM0MmZl) to participate in the ceremony.

The important part of the ceremony is that the toxic value is not leaked and it's deleted after the completion of the ceremony. Thus we recommend you to restart your machine after completing your contribution.

You can check the [Phase1 Perpetual Powers of Tau Ceremony](https://github.com/weijiekoh/perpetualpowersoftau) to verifiy Phase-1 contributions.

## 1. Requirements
A machine with 4 cores and 16Gb would do the work, but we recommend a bigger machine to process the ceremony faster.


For attestation, please ensure that you have a public identity at [Keybase](https://keybase.io/), or Twitter account.


## 2. Preparation of the Machine

You will need to nodejs [NodeJS v14+](https://linuxize.com/post/how-to-install-node-js-on-ubuntu-20-04/#installing-nodejs-and-npm-from-nodesource) and [Wormhole](https://magic-wormhole.readthedocs.io/en/latest/welcome.html#installation)(**or other means of sharing files with the coordinator such as using DropBox**).

Ensure that you have `node` and `wormhole` in your PATH environment variable by running the following commands successfully:
```
node -v
command -v wormhole
```
Make sure that the NodeJS version is 14 or higher.

## 3. Contributing to the ceremony
1. Prepare the contribution code in advance
```
git clone https://github.com/Railgun-Privacy/phase2-v2.git
cd phase2-v2
npm i
mkdir -p ceremony/old
mkdir -p ceremony/new
```
2. Once you receive a code from the coordinator (e.g., **7-certify-framework**), use wormhole to download the last contribution
```
code=7-certify-framework
wormhole receive $code -o ./ceremony/old --accept-files
```
Alternatively, you can receive the last contribution and extract it to `./ceremony/old`

3. Contribute to the ceremony, write your name without curly brackets and spaces.
```
npm start {yourname}
```
4. Once the contribution finishes successfully, you can send the files in ```./ceremony/new``` to the coordinator
If you use wormhole, then share the code with the coordinator so that he can receive them.
```
wormhole send ./ceremony/new
```

## 4. Attesting to your contribution
After you finish the contribution successfully, the code will output the **transcript path** to a file that contains the hash values of your contributions. It is paramount to bind the transcript to your identity by one of the following ways:
1. If you have [Keybase](https://keybase.io/) identity, then sign the **transcript** file and share the signature with the coordination
2. If you have a twitter account, then tweet the SHA256 of the **transcript** file

### Thank you very much for contributing!