# Wazuh
This repository contains the Installation guide of Wazuh

# Preparing the Server/System has the supported Operating System (e.g., Ubuntu, CentOS, etc.)
- Update the Server/System
  . For Ubuntu/Debian
  ```bash
     sudo apt update && sudo apt upgrade -y
  ```
  . For CentOS/RHEL
  ```bash
     sudo yum update -y
  ```
# Install the Wazuh Manager
- Add the Wazuh repository
  ```bash
     curl -s https://packages.wazuh.com/key/GPG-KEY-WAZUH | sudo gpg --dearmor -o /usr/share/keyrings/wazuh-archive-keyring.gpg
   echo "deb [signed-by=/usr/share/keyrings/wazuh-archive-keyring.gpg] https://packages.wazuh.com/4.x/apt/ stable main" | sudo tee /etc/apt/sources.list.d/wazuh.list
  ```
- Update the packages
  ``bash
    sudo apt update
  ```
- Install the Wazuh Manager
  ```bash
     sudo apt install wazuh-manager
  ```
- Start and Enable the wazuh-manager service
  ```bash
     sudo systemctl daemon-reload
     sudo systemctl enable wazuh-manager
     sudo systemctl start wazuh-manager
  ```
# Install Wazuh Indexer ( For Log Storage)
- If you need to store and analyze logs, install the Wazuh Indexer
  ```bash
     sudo apt install wazuh-indexer
  ```
- After the installation of wazuh-indexer configure it according to your needs

# Install Wazuh Dashboard
- Install the Wazuh Dashboard for visualization
  ```bash
     sudo apt install wazuh-dashboard
  ```
- Start and Enable the wazuh-dashboard
  ```bash
     sudo systemctl daemon-reload
     sudo systemctl enable wazuh-dashboard
     sudo systemctl start wazuh-dashboard
  ```
- Access the wazuh dashboard
  
  . Open a browser and go to httpS://<IP_ADDRESS>
  
  . Login with the credentials given during the installation process

