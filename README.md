# EventNFTDemo
purchase event NFTs

Once running we should be able to Mint tickets, respond to changes from the wallet like switching of accounts, chain, or updated balance. Finally once the user has minted ticket(s) the minting page will also display those SVG tickets that are stored on the Ethereum blockchain on the minting page so that a user connected with a wallet that has previously purchased tickets can see all NFT tickets that they own.


1. Clone the project and switch to the proper branch:

	git clone https://github.com/MetaMask/react-sdk-linea-workshop && \ 
	cd react-sdk-linea-workshop

2. Open in your Editor of choice and install dependencies from root of project:

	npm install

3. Create an Infura account and setup an Infura account and create an API Key

	Create Environment Variable file inside the apps/web root:
	Copy the file at apps/web/.env.example to .env

	Use hexadecimal network id 
	Linea: '0xe704'

	VITE_PUBLIC_NETWORK_ID=[LINEA-HEX-CHAIN-ID-GOES-HERE]
	VITE_PUBLIC_INFURA_PROJECT_ID=[INFURA-API-KEY-GOES-HERE]

	Create Environment Variable file inside the apps/blockchain root:
	Copy the file at apps/blockchain/.env.example to .env

	Obtain from your dashboard, also known as API key
	INFURA_PROJECT_ID=[INFURA-API-KEY-GOES-HERE]
	PRIVATE_KEY=[MM-PRIVATE-KEY-GOES]

4. Get Linea at: infura.io/faucet/linea

5. Build project and compile contracts to generate apps/web/contract-abis:
	npm run build

6. Deploy contract on Linea testnet
	npm run deploy:linea --workspace blockchain

7. Copy the contract address to the apps/web/lib/config.ts:
	contractAddress: '[CONTRACT-ADDRESS]'

8. Run frontend against deployed contract:
	npm run dev:testnet

9. Test application functionality on MetaMask Browser Extension and Mobile
