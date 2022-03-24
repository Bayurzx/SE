<!--- STARTEXCLUDE --->
# Save Earth with CELO

Create entries of newly discovered, rare, or near-extinct life discoveries on earth with the help of `AI` 🤖 for the world to see and get rewards for prioritized discoveries.

<!---Add Image here --->
![image](https://raw.githubusercontent.com/Bayurzx/make-crypto-mobile-hackathon/save-earth/save_earth/codebase/save-earth/screenshots/details11.jpg)
![image](https://raw.githubusercontent.com/Bayurzx/make-crypto-mobile-hackathon/save-earth/save_earth/codebase/save-earth/screenshots/image%20dataset2.jpg)


# Why I Did It (Inspiration) ???
## `For the joy of a new discovery!!!`
*What's a better way to describe the beauty of life on earth than with a simple picture?*
I wanted to create a project that could create awareness on rare, unique, endangered plants and animals. It's vital that people understand the impact we have on the natural world around us with respect to extinction of other species.

# What It Does???
- It allows any one on earth or beyond 👽 `😉` To feature their discovery! And with the help of AI, The app can help detect high priority images, add it to a special collection which the admin can easily utilize.
- It also creates a community for we, the environmental/nature freaks, NGOs, scientists, researchers, explorers, adventurers of the world who care about nature...  etc... To come together and feature, discuss something weird you saw from some where on earth and save it. Hence, Save-Earth get it... 😁😊😓😓
- The app, with the help of the Custom Vision Prediction API was able to detect and then classify images returning a probability percent and give responses based on the probability.
- Reward users with CELO tokens when a prioritized discovery is found


- The app was able to automatically store high priority images that were detected by the Custom Vision AI by creating and saving it into Blob Containers.

![image](https://raw.githubusercontent.com/Bayurzx/Save_Earth_AI/master/screenshots/auto_containers.jpg)

- It also allowed people, given admin access, to tag and send image datasets for training.
![image](https://raw.githubusercontent.com/Bayurzx/make-crypto-mobile-hackathon/save-earth/save_earth/codebase/save-earth/screenshots/image_dataset1.jpg)

---

# What Do You Do???
## Checkout the site here 👉 [Saveearth With Celo](https://save-earth-celo.netlify.app/) 👈
---
- First, signin with google.
- Upload link shows only show after signin
- Give it a name, add a caption, give some description, tell us where you saw it. Take a pic and upload it or send us the link. Upload it to AI 🤖 to see if it's on our radar. Then add a location. Have in mind that the app uses `Google Geocoder API` So use a language Google map will understand. It also uses `Google Javascript Map API` for exact coordinates so don't forget to click the coordinate button!.
- You will need to access to your celo wallet to donate or recieve rewards!
---

# How we built it???
Save_Earth_AI Architecture 👇

![image](https://raw.githubusercontent.com/Bayurzx/make-crypto-mobile-hackathon/save-earth/save_earth/codebase/save-earth/screenshots/architecture.png)
- A user fills the form at the upload page, includes an image but first, sends the image data to Custom Vision AI
- If the image is detected by AI, If it is prioritized, it is sent to a blob container.
  - Prioritized images have at least +99.5% accuracy allowance.
  - The `CELO reward` is then released
- User receives response and can continue with uploading data
- The data is then stored in the database (Blobs go the Blob container; documents go to NoSQL)
---
- Similar step involves creation of Image Datasets.
- Anyone can create dataset (provided they have admin access) but only Root Administrator can train the customvision AI.
- This was put to in place to prevent common mistakes like:
    - Using bad data
    - Overfitting the model
    - Using unbalanced data

# What's Next???
- It was so much fun implementing CELO contracts to this project. 
- The vision ahead is to allow creation of `NFTs` for user discoveries
  - While the world slowly transitions in to `web3` cloud providers cloud providers are relied on for blob storage.
  - In the future images will be added to the IPFS network instead

---

## Stack Highlights 🥪🥪🥪
- [ContractKit](https://docs.celo.org/developer-guide/contractkit) elps you to communicate with your contract.
- The celo contract was built on the [Alfajores Testnet](https://docs.celo.org/getting-started/alfajores-testnet)
- [Remix](https://remix.ethereum.org/) was used mainly for writing the solidity contract
- Azure Cognitive Services' **Custom Vision** : Custom Vision makes it easy for anyone to train and analyze tagged `Image Datasets` without much prior experience with an already provided machine learning algorithm without, the complexity of spinning up VMs or GPU clusters. 
- Azure Container Storage: This enables storing blob files such as images for backups, archiving, retrieval and analysis 
---
### This web app also made use of :
| Languages  | Frameworks | Cloud services | Databases        | APIs        | Platform    |
 | ---------- | ---------- | -------------- | ---------------- | ----------- | ----------- |
| JS, HTML,CSS | Reactjs  | Azure(VM, VNet etc.) | DataStax Astra(Frontend)     | Azure BlobClient API, Azure Custom Vision API, Google Geocoder API, Google JavaScript Map API   |  Netlify   |

---

## Here are examples of trained images the AI will detect
Alpaca, American Crow, American Goldfinch (Male), American Robin (Adult), American Robin (Juvenile), Blue Jay, Common Grackle, `Hedgehog` House Wren, Mourning Dove, Northern Cardinal (Adult Male),  `Parrot`, `Red Panda`, Red-tailed Hawk (Dark morph), `Sunflower`, Tufted Titmouse, `White Tiger`.

### So Feel free to use the any of these and check the AI response (*Surprise, surprise😉*)

---
## Here is the `Admin Login` to test out creation of image Datasets
Admin user: celohack6@gmail.com
Admin password: h@(k(e10o

---
## Setting UP!.

### Setting up CELO
- Install the CeloExtensionWallet from the google chrome store.
  - Or, connect to the celo network on Metamask, Yes it is metamask accessible. For more info: [Metamask on Celo Network](https://medium.com/defi-for-the-people/how-to-set-up-metamask-with-celo-912d698fcafe)
- For new users, create a wallet 
- Go to https://celo.org/developers/faucet and get tokens for the alfajores testnet.
- Switch to the alfajores testnet in the CeloExtensionWallet.


### Setup Azure Custom Vision
- Follow this 👉 [link](https://portal.azure.com/#create/Microsoft.CognitiveServicesCustomVision) 👈 to create a custom vision resource

- Fill in the details as shown below

![image](https://raw.githubusercontent.com/Bayurzx/Save_Earth_AI/master/screenshots/Custom%20Vision%20UI.jpg)

- You will be directed to your Custom Vision UI. Remember to collect and keep your keys and endpoints url safely.

![image](https://raw.githubusercontent.com/Bayurzx/Save_Earth_AI/master/screenshots/customvision.jpg)

- For more info on custom vision click 👉 [link](https://docs.microsoft.com/en-us/learn/modules/classify-images-with-custom-vision-service/) 👈
---

### Setup Azure Storage Account
- Follow this 👉 [link](https://portal.azure.com/#create/Microsoft.StorageAccount) 👈 to create an Azure Storage Account
- Fill in the details as shown below

![image](https://raw.githubusercontent.com/Bayurzx/Save_Earth_AI/master/screenshots/azure_storage.jpg)

For more info click [here](https://docs.microsoft.com/en-us/azure/storage/blobs/storage-quickstart-blobs-nodejs)

*Do not forget to configure CORS from portal*


---
### Setting up DB
- [DataStax Astra](https://github.com/DataStax-Examples/sample-app-template)
- Follow the link for more info on how to setup the DB

### Setting Up Geocoder APIs
- You can easily get the keys for the Google Geocoder API and Google Javascript Map API [here](https://console.cloud.google.com/marketplace)

---
# Final Setup

Clone to your local machine...
`git clone <put copied git link here>`

Install all dependencies in package.json
`npm install`

While that is working, you should sort out your .env file, go to the .env.sample file you will get details on your environment variables

You should run using `npx netlify dev` to enable you utilize netlify-cli functions

Happy coding!


Youtube: https://youtu.be/t8w5vo5yMLc



