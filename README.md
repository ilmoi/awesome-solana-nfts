[![Awesome](images/awesome.svg)](https://github.com/sindresorhus/awesome)

# 🦄 Awesome Solana NFTs 

A curated list of resources for builders / artists hacking NFTs on Solana.

- ✅ Includes: open standards, protocols, OSS repos, community-built tools
- ✋ Excludes: individual drops, future promises (without actual code / working product)

If you see something missing - please submit a PR 🙏

## 📜 NFT Open Standards
- [Metaplex Token Metadata Standard](https://github.com/metaplex-foundation/metaplex/tree/master/rust/token-metadata)
  ![](https://img.shields.io/github/stars/metaplex-foundation/metaplex.svg?style=social) 
  ([docs](https://docs.metaplex.com/nft-standard)) - defines NFT metadata (its structure, how it's stored on-chain / off-chain) and different types of NFTs (master editions, normal editions, one-offs, participation NFTs)

## 🚀 NFT Issuance
- Metaplex - a set of 4 progams that together enable NFT creators to mint and auction off their creations. Highly customizable (eg can set max mint, add attributes, decide what kind of edition you want to sell).
    - [Token Metadata](https://github.com/metaplex-foundation/metaplex/tree/master/rust/token-metadata)
      ![](https://img.shields.io/github/stars/metaplex-foundation/metaplex.svg?style=social) 
      ([docs](https://docs.metaplex.com/architecture/deep_dive/overview)) - described above
    - [Token Vault](https://github.com/metaplex-foundation/metaplex/tree/master/rust/token-vault) 
      ![](https://img.shields.io/github/stars/metaplex-foundation/metaplex.svg?style=social)
      ([docs](https://docs.metaplex.com/architecture/deep_dive/token_vault)) - escrow & fractionalization of NFTs
    - [Auction](https://github.com/metaplex-foundation/metaplex/tree/master/rust/auction/program) 
      ![](https://img.shields.io/github/stars/metaplex-foundation/metaplex.svg?style=social)
      ([docs](https://docs.metaplex.com/architecture/deep_dive/auction)) - different types of auctions for NFTs
    - [Metaplex](https://github.com/metaplex-foundation/metaplex/tree/master/rust/metaplex) 
      ![](https://img.shields.io/github/stars/metaplex-foundation/metaplex.svg?style=social)
      ([docs](https://docs.metaplex.com/architecture/deep_dive/metaplex)) - the only program aware of the other 3, brings everything together
- [Metaplex Store](https://github.com/metaplex-foundation/metaplex/tree/master/js) 
  ![](https://img.shields.io/github/stars/metaplex-foundation/metaplex.svg?style=social) 
  ([docs](https://docs.metaplex.com/create-store/introduction)) - self-serve front-end for Metaplex
- [Holaplex](https://www.holaplex.com/) - managed storefront for Metaplex, setup in 5 minutes
- [Metaplex Candy Machine](https://github.com/metaplex-foundation/metaplex/tree/master/rust/nft-candy-machine)
  ![](https://img.shields.io/github/stars/metaplex-foundation/metaplex.svg?style=social)
  ([docs](https://docs.metaplex.com/create-candy/introduction)) - simple program (to use, not to build!) that issues a fixed number of NFTs at a fixed price, first come first serve. If Metaplex itself has too many knobs for you to think about, consider the Candy Machine instead.
- [Fair Launch](https://github.com/metaplex-foundation/metaplex/tree/master/rust/fair-launch) 
  ![](https://img.shields.io/github/stars/metaplex-foundation/metaplex.svg?style=social)
  ([docs](https://hackmd.io/FxCiD20ETZeMbfA8on9WMg?view#Fair-Launch-Protocol)) ([intro video](https://www.youtube.com/watch?v=Ucfl_vbdYQI)) - a way to do "fair" launches in 3 phases: 1)users bid, 2)users adjust their bids, 3)a lottery determines winners who get to mint the NFTs.
- A number of "managed" launch services exist: [Nova Launch](https://novalaunch.art/), [CrayonCreed](https://crayoncreed.com/). We've not tried and are not promoting either:)

## 🪂 Airdrops to NFT holders
- [Air Support](https://github.com/theskeletoncrew/air-support)
  ![](https://img.shields.io/github/stars/theskeletoncrew/air-support.svg?style=social) - set of scripts to airdrop NFTs to your following in 5 easy steps. 
- [Ghetto SolAir](https://github.com/h4rkl/Ghetto-SolAir)
  ![](https://img.shields.io/github/stars/h4rkl/Ghetto-SolAir.svg?style=social) - a guerilla tactix command lined based airdrop tool for Solana with no polish and max functionality.

## 🤝 NFT Escrows / Swaps
- [Metaplex Auction House](https://github.com/metaplex-foundation/metaplex/tree/master/rust/auction-house) 
  ![](https://img.shields.io/github/stars/metaplex-foundation/metaplex.svg?style=social) - sell your NFT for a fixed price in a decentralized manner.
- [Metaplex Token Entangler](https://github.com/metaplex-foundation/metaplex/tree/master/rust/token-entangler)
  ![](https://img.shields.io/github/stars/metaplex-foundation/metaplex.svg?style=social) - an escrow service that enables 2 parties to swap their NFTs.
- [Cofre](https://cofre.so/) - online tool for p2p NFT swaps.
- [YAWWW](https://trade.yawww.io/app/trade) - another p2p escrow tool by a member of the MonkeDAO.

## 💸 NFT Marketplaces
- [Solanart](https://solanart.io/)
- [Digitaleyez](https://digitaleyes.market/)
- [MagicEden](https://magiceden.io/)
- [Solsea](https://solsea.io/)
- [Alpha Art](https://alpha.art/)
- [FTX NFT Marketplace](https://ftx.com/en/nfts)

## 💧 Upcoming NFT Drops
- [How Rare Drops](https://howrare.is/drops) - in my experience this has the widest coverage. No pics tho:(
- [Solanalysis Upcoming Drops](https://solanalysis.com/upcoming)
- [Non Fungi Solana drops](https://www.non-fungi.com/solana-nft-drops/)
- [NFT Evening](https://nftevening.com/calendar/) - multi-chain drop info, includes Solana
- [Upcoming NFT](https://upcomingnft.art/) - multi-chain drop info, includes Solana

## 📊 NFT Data
### General
- [Solanafloor](https://solanafloor.com/) - floor insights for NFTs on Solana.
- [Solanalysis](https://solanalysis.com/) - track market cap and trading activity for Solana-based NFTs.
- [NFT FloorPrice](https://nftfloorprice.vercel.app/) - another app to track floor prices (shows by Marketplace).  
- [Solana Seer](https://solseer.app/) - see floor prices for each NFT in your wallet (includes those currently selling on marketplaces).
- [CryptoSlam](https://cryptoslam.io/) - useful multi-chain analytics, has all the top collections on Solana 
- [NASUS](https://nasus.io/) - portfolio management focused NFT viewer

### Rarity
- [How Rare Is](https://howrare.is/) - rarity tools for NFTs on solana.
- [Moonrank](https://moonrank.app/) - absolute statistical rarity for solana NFTs.
- [SolTracker](https://soltracker.io/rarity) - has a smaller selection of projects, but works.

## 🛡️ NFT Verification / Security
- [Solguard](https://www.solguard.io/) - enter the NFT mint to find out if it's part of a real collection or fake.

## 🤖 NFT Marketplace Bots
- [MonkeDAO Twitter Bot](https://github.com/MonkeDAO/observer) 
  ![](https://img.shields.io/github/stars/MonkeDAO/observer.svg?style=social) - observes marketplace sales and tweets them.
- [Discord Bot](https://github.com/milktoastlab/SolanaNFTBot) 
  ![](https://img.shields.io/github/stars/milktoastlab/SolanaNFTBot.svg?style=social) - tracks sales and posts them to discord.
- [Sales Tracker Bot](https://github.com/flutternft/solana-nft-sales-tracker) 
  ![](https://img.shields.io/github/stars/flutternft/solana-nft-sales-tracker.svg?style=social) - tracks marketplace sales by observing payments flowing back to creators. Marketplace agnostic.
- [SMB Marketplace History](https://github.com/boxwooddev/smb-marketplace-history) 
  ![](https://img.shields.io/github/stars/boxwooddev/smb-marketplace-history.svg?style=social) - sales bot for SMBs in particular, built by the legend @statikdev.

## 🙏 Community-built Tools
### for Metaplex (CLIs)
- [Metaboss](https://github.com/samuelvanderwaal/metaboss) 
  ![](https://img.shields.io/github/stars/samuelvanderwaal/metaboss.svg?style=social) - rust CLI that acts as a "swiss army knife" for Metaplex (decode metadata, mint new NFTs, update metadata, and more).
- [Metaplex Rust CLI](https://github.com/CalebEverett/metaplex-cli)
  ![](https://img.shields.io/github/stars/CalebEverett/metaplex-cli.svg?style=social) - another rust CLI for metaplex, similar ot Metaboss.
- [Metaplex Python CLI](https://github.com/metaplex-foundation/python-api) 
  ![](https://img.shields.io/github/stars/metaplex-foundation/python-api.svg?style=social) - python bindings for Metaplex.
- [Metaplex JS CLI](https://github.com/metaplex/js)
  ![](https://img.shields.io/github/stars/metaplex/js.svg?style=social) - js bindings for Metaplex.

### for Metaplex (other)
- [NFT Armory](http://nftarmory.me/) ([github code](https://github.com/ilmoi/nft-armory))
  ![](https://img.shields.io/github/stars/ilmoi/nft-armory.svg?style=social) - UI tool to view / mint / update Metaplex NFTs, aimed at developers/artists for quick and efficient experimentation.
- [Sonar NFT Creator](https://nft-creator.sonar.watch/#/) ([github code](https://github.com/sonar-watch/nft-creator-ui)) 
  ![](https://img.shields.io/github/stars/sonar-watch/nft-creator-ui.svg?style=social) - upload a file, name it, add a description and mint your NFT. Super simple tool for experimenting!
- [MetaplexMetadata-js](https://github.com/vicyyn/MetaplexMetadata-js) 
  ![](https://img.shields.io/github/stars/vicyyn/MetaplexMetadata-js.svg?style=social) - scrape metadata for the provided mint.
- [Solana mint List](https://github.com/statikdev/sol-mint-list) 
  ![](https://img.shields.io/github/stars/statikdev/sol-mint-list.svg?style=social) - provide mint wallet address > scrape metadata & arweave data for each NFT in a given collection.
- [Abstractica](https://tools.abstratica.art/) - provide mint wallet address > get addresses of current holders of a given collection.
- [getHolderSnapshot](https://github.com/halaprix/getHolderSnapshot) 
  ![](https://img.shields.io/github/stars/halaprix/getHolderSnapshot.svg?style=social) - provide list of NFT mints > get holders for each.
- [Script to update Solana NFT Token Metadata](https://github.com/thuglabs/solana-nft-token-metadata-update) ![](https://img.shields.io/github/stars/thuglabs/solana-nft-token-metadata-update.svg?style=social)
- [Metaplex Launch Cost Calculator](https://feecalc.live/) - enter your collection size to calculate the total fees you will incur to launch.
- [Metaplex Store Installer](https://github.com/blackranger07/Metaplex-Store-Installer) 
  ![](https://img.shields.io/github/stars/blackranger07/Metaplex-Store-Installer.svg?style=social) - community script to install metaplex store on a linux box.

### for Candy Machine
- [Candy Machine Mint](https://github.com/exiled-apes/candy-machine-mint) 
  ![](https://img.shields.io/github/stars/exiled-apes/candy-machine-mint.svg?style=social) - off the shelf front-ends for Candy Machine.
- [Solana Candy Factory](https://github.com/kevinfaveri/solana-candy-factory) 
  ![](https://img.shields.io/github/stars/kevinfaveri/solana-candy-factory.svg?style=social) - fork, customize, and deploy your own candy machine mint app to a custom domain, ultra fast.
- [MintUI](https://github.com/InnerMindDAO/MintUI) 
  ![](https://img.shields.io/github/stars/InnerMindDAO/MintUI.svg?style=social) - extensible UI for creating Metaplex Candy Machines.
- [Willy Wonka](https://github.com/crispheaney/willy-wonka)
  ![](https://img.shields.io/github/stars/crispheaney/willy-wonka.svg?style=social) - Mint candy machine NFTs from your CLI. Use your preferred rpc provider. Avoid rage quitting because the candy machine GUI fails.
- [CSV-to-JSON for Candy Machine](https://github.com/thuglabs/csv-to-json-for-candy-machine) 
  ![](https://img.shields.io/github/stars/thuglabs/csv-to-json-for-candy-machine.svg?style=social) - quickly turn a CSV file into a bunch of JSONs that the Candy Machine expects.
- [List all Candy Machines in existence](https://gist.github.com/levicook/aadb079bf9daa1eeda3ff603c73b1b79)

### for Arweave
- [Permaweb Dropper](https://github.com/textury/permaweb-dropper) ![](https://img.shields.io/github/stars/textury/permaweb-dropper.svg?style=social)
- [Arweave NFT Uploader](https://github.com/0xEnrico/arweave-nft-uploader) ![](https://img.shields.io/github/stars/0xEnrico/arweave-nft-uploader.svg?style=social)
- [Arweave Image Uploader](https://github.com/thuglabs/arweave-image-uploader) ![](https://img.shields.io/github/stars/thuglabs/arweave-image-uploader.svg?style=social)
- [Harbor](https://github.com/kevinrodriguez-io/harbor) ![](https://img.shields.io/github/stars/kevinrodriguez-io/harbor.svg?style=social)
- [Sol NFT Tools](https://sol-nft.tools/) - has an uploder section.

### Multi-function
- [Solana Tools](https://www.solana-tools.com/) - find PDAs, ATAs, and read NFT/token metadata from a mint address.
- [Sol NFT Tools](https://sol-nft.tools/) - get mints created by a creator, get metadata from a mint, get holders of a bunch of mints, upload files to arweave.

## 🦾 Generative Art Tools
- [NFT Image generator](https://github.com/benyaminahmed/nft-image-generator) 
  ![](https://img.shields.io/github/stars/benyaminahmed/nft-image-generator.svg?style=social) - python code in jupyter notebooks for generative art.
- [Treat Toolbox](https://github.com/theskeletoncrew/treat-toolbox) 
  ![](https://img.shields.io/github/stars/theskeletoncrew/treat-toolbox.svg?style=social) - drag and drop tool with a friendly UI to randomly combine layers into generative art.
- [Solseum NFT generator](https://github.com/Solseum/solseum-nft-generator) 
  ![](https://img.shields.io/github/stars/Solseum/solseum-nft-generator.svg?style=social) - python cli for genrative art with sophisticated tooling/charts around the rarity system.
- [Lifecycle NFT generator](https://github.com/lightcycleresearch/lightcycle-nft-generator) 
  ![](https://img.shields.io/github/stars/lightcycleresearch/lightcycle-nft-generator.svg?style=social) - python cli for generative art.
- [Candy Maker](https://github.com/kevinrodriguez-io/candy-maker/) 
  ![](https://img.shields.io/github/stars/kevinrodriguez-io/candy-maker.svg?style=social) - ts cli for generative art.
- [TIEXO](https://github.com/TiexoHQ/toolbox) 
  ![](https://img.shields.io/github/stars/TiexoHQ/toolbox.svg?style=social) - generative NFT art toolbox from the creators of Moonlet.
- [NFT Maker](https://github.com/hempworks/nft-maker-js) 
  ![](https://img.shields.io/github/stars/hempworks/nft-maker-js.svg?style=social) - NodeJS package to generate NFT images and JSON compatible with Metaplex's Candy Machine.

## ⚙️ RPC Providers
- [QuickNode](https://quicknode.com/)
- [GenesysGo](https://genesysgo.com/)
- [RunNode](https://runnode.com/)
- [Triton One | RPC Pool](https://triton.one/#/)
- [Figment](https://figment.io/datahub/solana/)
- [Blockdaemon](https://blockdaemon.com/marketplace/solana/)
- [Syndica](https://syndica.io/)

## 🔗 Related Awesome Lists
- [Awsome Solana](https://github.com/paul-schaaf/awesome-solana) ![](https://img.shields.io/github/stars/paul-schaaf/awesome-solana.svg?style=social)
- [Awesome Serum](https://github.com/project-serum/awesome-serum) ![](https://img.shields.io/github/stars/project-serum/awesome-serum.svg?style=social) 
- [Awesome Solana Gaming](https://github.com/murlokito/awesome-solana-gaming) ![](https://img.shields.io/github/stars/murlokito/awesome-solana-gaming.svg?style=social)
