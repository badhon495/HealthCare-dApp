<div align="center">

# HealthCare-dApp

![Solidity](https://img.shields.io/badge/Solidity-0.8+-363636?style=flat-square&logo=solidity)
![Web3.js](https://img.shields.io/badge/Web3.js-1.0+-F16822?style=flat-square&logo=web3.js)
![Truffle](https://img.shields.io/badge/Truffle-5.0+-5E464D?style=flat-square&logo=truffle)
![Ethereum](https://img.shields.io/badge/Ethereum-Blockchain-627EEA?style=flat-square&logo=ethereum)
![MetaMask](https://img.shields.io/badge/MetaMask-Wallet-F6851B?style=flat-square&logo=metamask)
![Ganache](https://img.shields.io/badge/Ganache-Local%20Blockchain-E4A663?style=flat-square)

A decentralized application (dApp) for managing patient records and doctor bookings using Ethereum. Developed as part of the **CSE446: Blockchain and Cryptocurrencies** course project.

</div>

## Features

- **Appointment Management**: Patients can book appointments with doctors.
- **Role-Based Access**: Roles for patients, doctors, and admins can be registered.
- **Data on Blockchain**: All data is securely stored on the Ethereum blockchain using smart contracts.
- **Tech Stack**: Built with React.js and Solidity.
- **Blockchain Interaction**: Uses MetaMask for blockchain interactions.
- **Deployment Tools**: Smart contracts deployed with Truffle; Ganache used for local Ethereum blockchain.



## Environment Setup
Following commands are tested on Linux.

If you want more through instructions, please visit the following [Tutorial](https://github.com/YEASIN49/CSE446-Content/blob/main/Ethereum%20Dapp/README.mdche/) made by Yeasin sir. 

### Prerequisites
1. **Install Node Version Manager (nvm):**
   ```bash
   curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.2/install.sh | bash
   ```

2. **Install Node.js (v18.15.0):**
   ```bash
   nvm install 18.15.0
   nvm alias default 18.15.0
   ```

3. **Install Truffle:**
   ```bash
   npm install -g truffle
   ```

4. **Install Ganache:**
   - Download from [Ganache](https://trufflesuite.com/ganache/)
   - Install additional tools:
     ```bash
     sudo add-apt-repository universe && sudo apt install libfuse2
     ```
   - Make the downloaded file executable and run it.

5. **Install MetaMask:**
   - Go to [MetaMask](https://metamask.io/) and install the extension for your preferred browser.
   - Follow the on-screen instructions to set up MetaMask.

### Connecting MetaMask to Ganache
1. **Add Network Manually in MetaMask:**
   - Network Name: localhost:7545
   - New RPC URL: http://127.0.0.1:7545
   - Chain ID: 1337
   - Currency Symbol: ETH

2. **Import Ganache Account to MetaMask:**
   - Copy the private key from Ganache.
   - Import the account in MetaMask using the private key.



## Installation
1. Clone the repository.
2. Start Ganache and create a new workspace.
3. Compile and deploy the smart contracts using Truffle:
    ```bash
    truffle compile
    truffle migrate
    ```
4. Install the required packages:
    ```bash
    npm install
    ```
5. Start the React app:
    ```bash
    npm run dev
    ```
6. Open the app in your browser at `http://localhost:3000/`.



## Screenshots

### Registration Page (Admin & Doctor)
The landing page of the app where the user can register as an Admin, Doctor, or Patient. Switching the account from MetaMask will change the role of the user. The first account of Ganache is an Admin account. If logged in as the first account, the landing page will directly take you to the Admin dashboard. Change the account to another account from Ganache to see the registration page.
![Registration Page](Screenshot/registration_transaction.png)

### Registration Page (Patient)
Here patients can register by providing their details. Every time you register a new patient, a new transaction is created in the blockchain.
![Registration Page](Screenshot/patient_registration.png)

### Admin Dashboard
Here you will be able to update patient information.
![Admin Dashboard](Screenshot/patient_update.png)

### Patient Dashboard
Here you will be able to book an appointment with a doctor. You can also view if the doctor is booked at a particular time.
![Patient Dashboard](Screenshot/patient_dashboard.png)
Every time a patient books an appointment, the selected admin gets one ether as a fee.
![Doctor Booking](Screenshot/doctor_book.png)

### Doctor Schedule
Here the doctor can view their schedule and appointments with information like how many patients registered and their age.
![Doctor Schedule](Screenshot/schedule_update.png)



## How to Contribute
1. Fork the repository.
2. Push your changes to a new branch.
3. Create a pull request.
4. Wait for the pull request to be reviewed.


---

<div align="center">
  <p>⭐ Star this repo if you found it helpful!</p>
</div>