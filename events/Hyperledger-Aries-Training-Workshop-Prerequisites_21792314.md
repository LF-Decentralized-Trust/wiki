1. [Community Events](index.html)
2. [Community Events Home](Community-Events-Home_21790731.html)
3. [Workshops](Workshops_21790888.html)
4. [Build Your Identity Solution Using Hyperledger Aries](Build-Your-Identity-Solution-Using-Hyperledger-Aries_21790854.html)

# Community Events : Hyperledger Aries Training Workshop Prerequisites

Created by Lynn Gray Bendixsen, last modified by Oumar FALL on Jan 20, 2022

To attend the [Hyperledger Foundation Community Workshop series, Intro to Decentralized Identity](Build-Your-Identity-Solution-Using-Hyperledger-Aries_21790854.html), some preparatory work must be done in order to follow along with the workshops. Please make sure the OS and tools listed below are installed. The command lines are provided because in some cases, the default download will not work with our solution.

## OS

To successfully follow the examples given during the training, you will need Ubuntu 18.04 (The desktop version is required).

## Required tools

If not already installed, you will need to install curl, Node.js, Git, Docker, and Docker-Compose on your Ubuntu system. These must be installed to do the labs during the training session. Use the steps in each section below to properly install each element.

### **curl  (optional: typing "curl -help" will tell you if the following is needed)**

```
sudo apt install -y curl
```

### **Node.js**

**Note:** Do *not* use the default method for installing Node.js in Ubuntu, please enter the two command lines listed here.

```
curl -sL https://deb.nodesource.com/setup_16.x | sudo -E bash -
sudo apt install -y nodejs
```

### **Git**

```
sudo apt install -y git
```

### **Docker**

Only perform Steps 1 and 2 from the following link to install docker: [https://www.digitalocean.com/community/tutorials/how-to-install-and-use-docker-on-ubuntu-18-04](https://www.digitalocean.com/community/tutorials/how-to-install-and-use-docker-on-ubuntu-18-04).

### **Docker-Compose**

Enter these three commands in your terminal:

```
sudo curl -L https://github.com/docker/compose/releases/download/1.25.5/docker-compose-`uname -s`-`uname -m` -o /usr/local/bin/docker-compose
sudo chmod +x /usr/local/bin/docker-compose
docker-compose --version
```

Your output should read as follows: `$ docker-compose version 1.25.5, build 8a1c60f6`

Install a necessary dependency:

```
sudo apt -y install libgconf2-4
```

Ubuntu 21 dependency

If you are using a recent version of Ubuntu (+21.04) you should install the "shared low-level terminfo" library. Otherwise the *indy-cli* installation may fail;

```
sudo apt install -y libtinfo5
```

### **Download Repos**

Enter these six commands into your terminal:

```
cd ~
mkdir git-hltraining
cd git-hltraining
git clone https://github.com/hyperledger/aries-toolbox.git
git clone https://github.com/hyperledger/aries-acapy-plugin-toolbox.git
cd aries-acapy-plugin-toolbox
git fetch
git checkout hl-workshop
cd ~
```

### **Install Indy-CLI**

Enter all of the following steps in to the Ubuntu command line:

```
sudo apt-key adv --keyserver keyserver.ubuntu.com --recv-keys CE7709D068DB5E88
sudo add-apt-repository "deb https://repo.sovrin.org/sdk/deb bionic stable"
sudo add-apt-repository "deb https://repo.sovrin.org/deb bionic stable"
sudo apt-get update -y
sudo apt-get upgrade -y 
sudo apt-get install -y indy-cli
cd ~
```

```

```

Now download the Indicio TestNet Genesis file:

```
curl -O https://raw.githubusercontent.com/Indicio-tech/indicio-network/main/genesis_files/pool_transactions_testnet_genesis
```

Create a cliconfig file (e.g. vi cliconfig) in your home directory and add the following contents:

```
{
  "taaAcceptanceMechanism": "for_session"
}
```

Run indy-cli. A full path for cliconfig is needed if you do not run indy-cli from your home directory.

```
indy-cli --config cliconfig  
```

### **Ubuntu In a VM**

If Ubuntu is installed on Mac or Windows in a Virtualbox VM, do the following:

1. Perform all the steps listed in [this tutorial](https://www.tecmint.com/install-virtualbox-guest-additions-in-ubuntu/) to update your system and enable copy and paste.
2. Make sure to restart your VM and that the Shared Clipboard is set to bidirectional:
3. 1. In your VM machine settings, in Virtual Box &gt; General &gt; Advanced
   2. Set ‘Shared Clipboard’ to ‘Bidirectional’

## **Test starting the agents and toolbox**

From one terminal, run the following:

```
cd ~/git-hltraining/aries-toolbox
npm install
npm run dev
```

After running these commands, you should see a window like the following pop up:

![](attachments/21792314/21792392.png?height=400)

This is the Aries Toolbox. We will now start the agents. From another terminal, run the following:

```
cd ~/git-hltraining/aries-acapy-plugin-toolbox/demo
docker-compose -f docker-compose.alice-bob.yml up --build
```

Permissions

When running docker-compose (or other docker commands), you may need to prefix the command with \`sudo\` if it initially fails due to permissions.

The above command would then look like:

```
sudo docker-compose -f docker-compose.alice-bob.yml up --build
```

After running this command, you should see output similar to the following:

![](attachments/21792314/21792393.png?height=400)

If you've gotten to this point, you should be ready to run the agents and toolbox for the workshop!

## Attachments:

![](images/icons/bullet_blue.gif) [Screenshot from 2022-01-13 19-43-18.png](attachments/21792314/21792392.png) (image/png)  
![](images/icons/bullet_blue.gif) [Screenshot from 2022-01-13 19-52-35.png](attachments/21792314/21792393.png) (image/png)  
![](images/icons/bullet_blue.gif) [Screenshot from 2022-01-19 07-26-24.png](attachments/21792314/21792440.png) (image/png)  
![](images/icons/bullet_blue.gif) [error1.png](attachments/21792314/21792441.png) (image/png)  
![](images/icons/bullet_blue.gif) [Screenshot from 2022-01-19 07-24-49.png](attachments/21792314/21792442.png) (image/png)  
![](images/icons/bullet_blue.gif) [image2022-5-30\_3-50-24.png](attachments/21792314/21793418.png) (image/png)  
![](images/icons/bullet_blue.gif) [image2022-5-30\_3-52-33.png](attachments/21792314/21793419.png) (image/png)  
![](images/icons/bullet_blue.gif) [image2022-5-30\_3-57-28.png](attachments/21792314/21793420.png) (image/png)  
![](images/icons/bullet_blue.gif) [image-2023-3-6\_1-40-2.png](attachments/21792314/21793806.png) (image/png)

Document generated by Confluence on Nov 26, 2024 16:14

[Atlassian](http://www.atlassian.com/)
