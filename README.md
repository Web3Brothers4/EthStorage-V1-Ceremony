# ⚡ EthStorage V1 Trusted Setup Ceremony – Quick Guide

* Detailed guide to contribute to the ceremony which is conducted for our Groth16 zk-SNARK circuits
* ETHstorage is L2 that lets you store data and use it for games, socials, AI. It makes sure no one can fake data or pretend to store
* This ceremony is about making sure ETHstorage stays secure and decentralized

### Ceremony will last from August 13 to 22

---

## Requirements :
- Local PC Ubuntu 22.04
- or VPS : 2 vCPU, 4GB RAM, 30GB+ SSD recommended

  * GitHub account : for authentication
  * Github account age: ≥ 1 month  
  * At least 1 public repository  
  * Followings ≥ 5 accounts and atleast 1 or more followers

**Purchase a vps from [Xorek](https://xorek.cloud/en)**
  **Direct link to buy same specfication as mentioned [link](https://my.xorek.cloud/billmgr?startform=v2.vds.order.param)**
  * this will save you from keeping your pc on continuously

## Follow The Guide :

### Update & Install Dependencies
```
sudo apt update && sudo apt upgrade -y
sudo apt install -y curl git build-essential
```

### Install Node.js
```
curl -fsSL https://deb.nodesource.com/setup_18.x | sudo -E bash -
sudo apt install -y nodejs
sudo npm install -g npm@9.2
```

### Check Versions


```
node -v
npm -v
```

### Create Temporary Directory

```
mkdir ~/trusted-setup-tmp && cd ~/trusted-setup-tmp

```
### Install Phase2 CLI

```
sudo npm install -g @p0tion/phase2cli
```

### Verify CLI Installation


```
phase2cli --version
```

### Authenticate with GitHub

```
phase2cli auth
```

* Visit **[https://github.com/login/device](https://github.com/login/device)**
* Enter the code from your terminal
* Click **Authorize ethstorage**
* Allow **Read & Write access to GitHub Gists** in permissions

### 7) Start a `screen` session

```bash
screen -S ceremony
```

### 8) Join the ceremony

```bash
phase2cli contribute -c ethstorage-v1-trusted-setup-ceremony
```

* Press **Enter** for random input, or type your own characters.

---

## 🧹 Cleanup & Logout

When done, it’s recommended to clean up for security:

```bash
phase2cli clean
phase2cli logout
rm -rf ~/ceremonyeth
```

---

🖥 Screen Commands

| Action         | Command                       |
| -------------- | ------------------------------|
| Detach         | `Ctrl + A + D`                |
| Resume         | `screen -r ceremony`          |
| Delete screen  | `screen -XS ceremony quit`    |
| List sessions  | `screen -ls`                  |

---

## 🛠 Troubleshooting

**npm update error (`EBADENGINE`)**
You’re on Node 18 — stick to `npm@10`:

```bash
npm install -g npm@10
```

**Lost connection?**
Just re-run:

```bash
phase2cli contribute -c ethstorage-v1-trusted-setup-ceremony
```

It will resume from where you left off.


---

🎉 **You’ve successfully contributed to EthStorage’s decentralization!**

---

Follow : https://x.com/Web3Brothers for more tech contents.
