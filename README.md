[![Awesome](images/awesome.svg)](https://github.com/sindresorhus/awesome)

# 🦄 Awesome Solana NFTs

A curated list of resources for builders / artists hacking NFTs on Solana.

- ✅ Includes: open standards, protocols, OSS repos, community-built tools
- ✋ Excludes: individual drops, future promises (without actual code / working product)
- 🔀 Ordering: OSS before closed-source, ordered by github stars

If you see something missing - please submit a PR 🙏

## 📜 NFT Open Standards

- [Metaplex Token Metadata Standard](https://github.com/metaplex-foundation/metaplex-program-library/tree/master/token-metadata)
  ![](https://img.shields.io/github/stars/metaplex-foundation/metaplex.svg?style=social)
  ([docs](https://docs.metaplex.com/token-metadata/specification#token-standards)) - defines NFT metadata (its structure, how it's stored on-chain / off-chain) and different types of NFTs (master editions, normal editions, one-offs, participation NFTs)
- [Burnt Finance "Collections"](https://github.com/BurntFinance/Collections)
  ![](https://img.shields.io/github/stars/BurntFinance/Collections.svg?style=social) - a standard that proposes to start recording NFTs as part of "collections". A collection adds an NFT to an array stored in a PDA to verify it as original, and the NFT in turn signs the collection's PK to verify the addition is valid (otherwise any collection could claim the NFT is part of it).

## 🚀 NFT Issuance

- Metaplex - a set of 4 progams that together enable NFT creators to mint and auction off their creations. Highly customizable (eg can set max mint, add attributes, decide what kind of edition you want to sell).
  - [Token Metadata](https://github.com/metaplex-foundation/metaplex-program-library/tree/master/token-metadata)
    ![](https://img.shields.io/github/stars/metaplex-foundation/metaplex.svg?style=social)
    ([docs](https://docs.metaplex.com/architecture/deep_dive/overview)) - described above
  - [Token Vault](https://github.com/metaplex-foundation/metaplex-program-library/tree/master/token-vault)
    ![](https://img.shields.io/github/stars/metaplex-foundation/metaplex.svg?style=social)
    ([docs](https://docs.metaplex.com/architecture/deep_dive/token_vault)) - escrow & fractionalization of NFTs
  - [Auction](https://github.com/metaplex-foundation/metaplex-program-library/tree/master/auction/program)
    ![](https://img.shields.io/github/stars/metaplex-foundation/metaplex.svg?style=social)
    ([docs](https://docs.metaplex.com/architecture/deep_dive/auction)) - different types of auctions for NFTs
  - [Metaplex](https://github.com/metaplex-foundation/metaplex-program-library/tree/master/metaplex)
    ![](https://img.shields.io/github/stars/metaplex-foundation/metaplex.svg?style=social)
    ([docs](https://docs.metaplex.com/architecture/deep_dive/metaplex)) - the only program aware of the other 3, brings everything together
- [Metaplex Store](https://github.com/metaplex-foundation/metaplex/tree/master/js)
  ![](https://img.shields.io/github/stars/metaplex-foundation/metaplex.svg?style=social)
  ([docs](https://docs.metaplex.com/storefront/introduction)) - self-serve front-end for Metaplex
- [Holaplex](https://www.holaplex.com/) - managed storefront for Metaplex, setup in 5 minutes
- [Candy Shop](https://candy.liqnft.com) - Javascript library that allows projects to host their own escrowless, on-chain marketplace with few lines of code. Built on Metaplex auction house program
- [Metaplex Candy Machine](https://github.com/metaplex-foundation/metaplex-program-library/tree/master/candy-machine/program)
  ![](https://img.shields.io/github/stars/metaplex-foundation/metaplex.svg?style=social)
  ([docs](https://docs.metaplex.com/candy-machine-v2/introduction)) - simple program (to use, not to build!) that issues a fixed number of NFTs at a fixed price, first come first serve. If Metaplex itself has too many knobs for you to think about, consider the Candy Machine instead.
- Managed launchpad services - we've not tried and are not promoting either:)
  - [Coinfra](https://www.coinfra.io/)
  - [Nova Launch](https://novalaunch.art/)
  - [CrayonCreed](https://crayoncreed.com/)
  - [MonkeLabs](https://monkelabs.io/)
  - [launchlabs](https://launchlabs.app/)
  - [MOONGATE](https://moongate.space/)

## 🏦 Vaults

- [Token Vault](https://github.com/metaplex-foundation/metaplex-program-library/tree/master/token-vault)
  ![](https://img.shields.io/github/stars/metaplex-foundation/metaplex.svg?style=social)
  ([docs](https://docs.metaplex.com/architecture/deep_dive/token_vault)) - Metaplex vaults. Support fractionalization, although without built-in auctionn mechanic (you'd need to collect all the pieces manually).
- [Gem Bank](https://github.com/gemworks/gem-farm)
  ![](https://img.shields.io/github/stars/gemworks/gem-farm.svg?style=social) ([docs](https://docs.gemworks.gg/)) - Gemworks vaults. Users deposit/withdraw, bank manager locks/unlocks. Can control what NFTs are / aren't allowed in using a whitelist of mints / creators.

## 📝 Whitelisting

- [Gumdrop](https://github.com/metaplex-foundation/metaplex-program-library/tree/master/gumdrop)
  ![](https://img.shields.io/github/stars/metaplex-foundation/metaplex.svg?style=social)
  ([docs](https://docs.metaplex.com/airdrops/create-gumdrop)) ([guide](https://hackmd.io/@MarkSackerberg/gumdrop)) - can be used to create a whitelisted candy machine sale.
- [SPL-Airdrop](https://github.com/Lost-Cat-FC/spl-airdrop)
  ![](https://img.shields.io/github/stars/Lost-Cat-FC/spl-airdrop.svg?style=social) - can be used to airdrop whitelist tokens to a list of addresses.

## 🥩 Staking

- Can deposit multiple token mints (actually useful for NFTs):
  - [Gem Farm](https://github.com/gemworks/gem-farm)
    ![](https://img.shields.io/github/stars/gemworks/gem-farm.svg?style=social) ([docs](https://docs.gemworks.gg/)) - fully OSS staking program designed for NFT projects to offer yield to their communities. Choose between fixed and variable rate, configure params like min staking time & min cooldown and much more.
- Can deposit only a single token mint at a time:
  - [Serum's Staking Program](https://github.com/project-serum/stake) ![](https://img.shields.io/github/stars/project-serum/stake.svg?style=social) (and the [UI for it](https://github.com/project-serum/stake-ui)) - Serum's staking program. Most complex out of the bunch, but most fully-featured (supports time-locked rewards, doesn't comingle users' funds). Users need to actively "claim" the stake by periodically clicking a button.
  - [Step Finance Rewards Pool](https://github.com/step-finance/reward-pool) ![](https://img.shields.io/github/stars/step-finance/reward-pool.svg?style=social) - Step Finance rewards program. "AMM-style", meaning users' funds are pooled and rewards distributed proportionally. Supports rewards in up to 2 different mints.
  - [Step Finance Staking Program](https://github.com/step-finance/step-staking) ![](https://img.shields.io/github/stars/step-finance/step-staking.svg?style=social) - Step Finance staking program. A simpler program vs the one above, only pays out in one type of token.

## 🪂 Airdrops to NFT holders

- [Gumdrop](https://github.com/metaplex-foundation/metaplex-program-library/tree/master/gumdrop)
  ![](https://img.shields.io/github/stars/metaplex-foundation/metaplex.svg?style=social)
  ([docs](https://docs.metaplex.com/airdrops/create-gumdrop)) ([guide](https://hackmd.io/@MarkSackerberg/gumdrop)) - can be used to airdrop NFTs & tokens to whitelisted accounts. Users can be notified via email, SMS, or discord.
- [Air Support](https://github.com/theskeletoncrew/air-support)
  ![](https://img.shields.io/github/stars/theskeletoncrew/air-support.svg?style=social) - set of scripts to airdrop NFTs to your following in 5 easy steps.
- [Ghetto SolAir](https://github.com/h4rkl/Ghetto-SolAir)
  ![](https://img.shields.io/github/stars/h4rkl/Ghetto-SolAir.svg?style=social) - a guerilla tactix command lined based airdrop tool for Solana with no polish and max functionality.
- [Xin Dragons Airdroppper](https://github.com/Xin-Dragons/solana-toolkit)
  ![](https://img.shields.io/github/stars/Xin-Dragons/solana-toolkit.svg?style=social) - Utility lib for taking Solana NFT snapshots and running token airdrops, checking token holders etc

## 🤝 NFT Escrows / Swaps

- [Metaplex Auction House](https://github.com/metaplex-foundation/metaplex-program-library/tree/master/auction-house)
  ![](https://img.shields.io/github/stars/metaplex-foundation/metaplex.svg?style=social) - sell your NFT for a fixed price in a decentralized manner.
- [Metaplex Token Entangler](https://github.com/metaplex-foundation/metaplex-program-library/tree/master/token-entangler)
  ![](https://img.shields.io/github/stars/metaplex-foundation/metaplex.svg?style=social) - an escrow service that enables 2 parties to swap their NFTs.
- [Cofre](https://cofre.so/) - online tool for p2p NFT swaps.
- [YAWWW](https://trade.yawww.io/app/trade) - another p2p escrow tool by a member of the MonkeDAO.
- [FoxySwap](https://famousfoxes.com/swap) - P2P NFT swap service by the Famous Fox Federation team.

## 💸 NFT Marketplaces

- [Tensor](https://tensor.trade/) - AMM/Aggregator
- [HadeSwap](https://hadeswap.com/) - AMM
- [Elixir](https://elixirnft.io) - AMM
- [GoatSwap](https://goatswap.xyz/) - AMM
- [MagicEden](https://magiceden.io/) - Normal marketplace
- [OpenSea](https://opensea.io/solana-collections) - Normal marketplace
- [SolanArt](https://solanart.io/) - Normal marketplace
- [Exchange.Art](https://exchange.art/) - 1/1 art marketplace
- [FormFunction](https://formfunction.xyz/) - 1/1 art marketplace

## 🖼 NFT Galleries

- [NftEyez](https://nfteyez.global/) - online NFT gallery.
- [solwal.io](https://solwal.io/) - Search and explore wallet.
- [Nftbucket](https://nftbucket.com/) - Create your own NFT gallery.
- [civic.me](https://civic.me/) - NFT gallery with support for multiple wallets and customization.
- [Gallie](https://gallie.io/) - Curate your NFT collection to share with the world.

## 📅 Upcoming NFT Drops

- [How Rare Drops](https://howrare.is/drops) - SOL specific drops. In my experience this has the widest coverage. No pics tho:(
- [Moonly - Upcoming NFT Drops](https://moon.ly/solana) - Up to date Solana upcoming drops, tools, and much more
- [Solanalysis Upcoming Drops](https://solanalysis.com/upcoming) - SOL specific drops.
- [Next Drop](https://nextdrop.is/upcoming?chain=solana) - multi-chain drop info, includes Solana (filterable)
- [Non Fungi](https://www.non-fungi.com/solana-nft-drops/) - multi-chain drop info, includes Solana (filterable)
- [NFT Calendar](https://nftcalendar.io/b/solana/) - multi-chain drop info, includes Solana (filterable)
- [Ape O'Clock](https://www.apeoclock.com/all-sol-launches/) - multi-chain drop info, includes Solana (filterable)
- [NearingNFT](https://www.nearingnft.net/) - multi-chain drop info, includes Solana (filterable)
- [Rarity Tools](https://rarity.tools/upcoming/) - multi-chain drop info, includes Solana
- [NFT Evening](https://nftevening.com/calendar/) - multi-chain drop info, includes Solana
- [CoinMarketCap](https://coinmarketcap.com/nft/upcoming/) - multi-chain drop info, includes Solana
- [NFT Drop Scanner](https://nftdropscanner.com) - multi-chain drop info, includes Solana
- [NFT Sailing](https://nftsailing.net) - multi-chain drop info, includes Solana (filterable)

## 📊 NFT Data

### General

- [NFT🍌APE](https://nftape.me/)([github code](https://github.com/ilmoi/nftape.me) ![](https://img.shields.io/github/stars/ilmoi/nftape.me.svg?style=social)) - 1-click tool to calculate your P&L / paperhands / diamondhands amounts
- [Moonly - Market Data,Real-time NFT Events](https://moon.ly/monitor) - Solana Market Stats, FP, Trends, Marketcap
- [Solanafloor](https://solanafloor.com/) - floor insights for NFTs on Solana.
- [Solanalysis](https://solanalysis.com/) - track market cap and trading activity for Solana-based NFTs.
- [NFT FloorPrice](https://nftfloorprice.vercel.app/) - another app to track floor prices (shows by Marketplace).
- [Solana Seer](https://solseer.app/) - see floor prices for each NFT in your wallet (includes those currently selling on marketplaces).
- [CryptoSlam](https://cryptoslam.io/) - useful multi-chain analytics, has all the top collections on Solana
- [Nasus](https://nasus.io/) - portfolio management focused NFT viewer
- [MoveMints by BridgeSplit](https://movemints.bridgesplit.com/) - tracks the latest Solana NFT drops and analyzes their community growth.
- [Solens](https://solens.io/) - All-in-one analytics platform to follow Solana NFT trends, smart money activity and historical data (by marketplace).
- [SolsWatch](https://sols.watch/) - Data Insights and charts on Solana NFT collections from the secondary marketplaces. Discover new collections as soon as they are added to the marketplaces.
- [NFT Collection's Mint Addresses](https://github.com/BL0CK-X/solana-nft-collection-mint-addresses) - an open source GitHub repository that maps a collection name to a list of mint addresses on Solana.
- [Blockchain API](https://docs.blockchainapi.com/) - Mint NFTs, read NFTs, read/write candy machines, buy/list/delist on NFT marketplaces, and much more with the Blockchain API
- [MrBot](https://mrbot.tech/) - Real time data for all collections (floor price, last sold, volume, listed), mintbot, sniper, famousfoxes tokens metrics.

### Rarity

- [How Rare Is](https://howrare.is/) - rarity tools for NFTs on solana.
- [Moonrank](https://moonrank.app/) - absolute statistical rarity for solana NFTs.
- [SolTracker](https://soltracker.io/rarity) - has a smaller selection of projects, but works.

## 💧 NFT Fractionalization / Liquidity

- [Token Vault](https://github.com/metaplex-foundation/metaplex-program-library/tree/master/token-vault)
  ![](https://img.shields.io/github/stars/metaplex-foundation/metaplex.svg?style=social)
  ([docs](https://docs.metaplex.com/architecture/deep_dive/token_vault)) - allows fractionalization of NFTs, although only has a naive buyout mechanism
- [Fraktion](https://www.fraktion.art/)
- [Bridgesplit](https://www.bridgesplit.com/)
- [MIMO](https://linktr.ee/millionmonke)
- [LIQNFT](https://liqnft.com)

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
- [Solana NFT Sales Monitor](https://github.com/t4top/solana-nft-sales-monitor)
  ![](https://img.shields.io/github/stars/t4top/solana-nft-sales-monitor.svg?style=social) - monitors NFT collections sales and posts them to Discord.

## 🙏 Community-built Tools

### for Metaplex (CLIs)

- [Metaboss](https://github.com/samuelvanderwaal/metaboss)
  ![](https://img.shields.io/github/stars/samuelvanderwaal/metaboss.svg?style=social) - rust CLI that acts as a "swiss army knife" for Metaplex (decode metadata, mint new NFTs, update metadata, and more).
- [Metaplex JS CLI](https://github.com/metaplex/js)
  ![](https://img.shields.io/github/stars/metaplex/js.svg?style=social) - js bindings for Metaplex.
- [Metaplex Python CLI](https://github.com/metaplex-foundation/python-api)
  ![](https://img.shields.io/github/stars/metaplex-foundation/python-api.svg?style=social) - python bindings for Metaplex.
- [Metaplex Rust CLI](https://github.com/CalebEverett/metaplex-cli)
  ![](https://img.shields.io/github/stars/CalebEverett/metaplex-cli.svg?style=social) - another rust CLI for metaplex, similar ot Metaboss.

### for Metaplex (other)

- [Sonar NFT Creator](https://nft-creator.sonar.watch/#/) ([github code](https://github.com/sonar-watch/nft-creator-ui))
  ![](https://img.shields.io/github/stars/sonar-watch/nft-creator-ui.svg?style=social) - upload a file, name it, add a description and mint your NFT. Super simple tool for experimenting!
- [Script to update Solana NFT Token Metadata](https://github.com/thuglabs/solana-nft-token-metadata-update) ![](https://img.shields.io/github/stars/thuglabs/solana-nft-token-metadata-update.svg?style=social)
- [NFT Armory](http://nftarmory.me/) ([github code](https://github.com/ilmoi/nft-armory))
  ![](https://img.shields.io/github/stars/ilmoi/nft-armory.svg?style=social) - UI tool to view / mint / update Metaplex NFTs, aimed at developers/artists for quick and efficient experimentation.
- [MetaplexMetadata-js](https://github.com/vicyyn/MetaplexMetadata-js)
  ![](https://img.shields.io/github/stars/vicyyn/MetaplexMetadata-js.svg?style=social) - scrape metadata for the provided mint.
- [Solana mint List](https://github.com/statikdev/sol-mint-list)
  ![](https://img.shields.io/github/stars/statikdev/sol-mint-list.svg?style=social) - provide mint wallet address > scrape metadata & arweave data for each NFT in a given collection.
- [Abstractica](https://tools.abstratica.art/) - provide mint wallet address > get addresses of current holders of a given collection.
- [getHolderSnapshot](https://github.com/halaprix/getHolderSnapshot)
  ![](https://img.shields.io/github/stars/halaprix/getHolderSnapshot.svg?style=social) - provide list of NFT mints > get holders for each.
- [Metaplex Store Installer](https://github.com/blackranger07/Metaplex-Store-Installer)
  ![](https://img.shields.io/github/stars/blackranger07/Metaplex-Store-Installer.svg?style=social) - community script to install metaplex store on a linux box.
- [Metaplex Launch Cost Calculator](https://feecalc.live/) - enter your collection size to calculate the total fees you will incur to launch.
- [Solana Address Generator](https://github.com/thislooksrare/solana-wallet-generator) - generate fancy looking solana addresses.

### for Candy Machine

- [Candy Machine Mint](https://github.com/exiled-apes/candy-machine-mint)
  ![](https://img.shields.io/github/stars/exiled-apes/candy-machine-mint.svg?style=social) - off the shelf front-ends for Candy Machine.
- [MintUI](https://github.com/InnerMindDAO/MintUI)
  ![](https://img.shields.io/github/stars/InnerMindDAO/MintUI.svg?style=social) - extensible UI for creating Metaplex Candy Machines.
- [Willy Wonka](https://github.com/crispheaney/willy-wonka)
  ![](https://img.shields.io/github/stars/crispheaney/willy-wonka.svg?style=social) - Mint candy machine NFTs from your CLI. Use your preferred rpc provider. Avoid rage quitting because the candy machine GUI fails.
- [CSV-to-JSON for Candy Machine](https://github.com/thuglabs/csv-to-json-for-candy-machine)
  ![](https://img.shields.io/github/stars/thuglabs/csv-to-json-for-candy-machine.svg?style=social) - quickly turn a CSV file into a bunch of JSONs that the Candy Machine expects.
- [Candy Machine V2 Responsive UI](https://github.com/Fulgurus/candy-machine-v2-responsive-ui) ![](https://img.shields.io/github/stars/Fulgurus/candy-machine-v2-responsive-ui.svg?style=social) - responsive, customizable prod-ready UI for Candy Machine V2.
- [Candy Machine V2 + NFT Marketplace](github.com/LIQNFT/candy-machine-v2-with-marketplace) - Candy Machine V2 for primary sale + NFT marketplace powered by Candy Shop for secondary trading
- [Next.js Tailwind CSS Candy Machine V2](https://github.com/updatesettings/nextjs-candy-machine-v2) ![](https://img.shields.io/github/stars/updatesettings/nextjs-candy-machine-v2?style=social) - Next.js, Whitelist signup to Notion, Tailwind CSS, NFT Collection Viewer, and more.
- [List all Candy Machines in existence](https://gist.github.com/levicook/aadb079bf9daa1eeda3ff603c73b1b79)
- [Complete Video Tutorial](https://www.youtube.com/watch?v=9dAnpo0OiAg) - Full Candy Machine V2 Video (Sugar update) tutorial detailing all steps of the project (Assets generation, Pre-sale, Mint, REVEAL, ...).
- [Config generator](https://github.com/vdusart/candymachinev2-config-generator) - Easy tool to automatically generate the configuration of a candymachineV2 by answering some questions.
- [Crossmint](https://docs.crossmint.io) - Enables minting NFTs with a credit card, an NFT minting API, and paying for Solana NFTs using ETH+MetaMask.

### for Arweave

- [Arweave NFT Uploader](https://github.com/0xEnrico/arweave-nft-uploader) ![](https://img.shields.io/github/stars/0xEnrico/arweave-nft-uploader.svg?style=social)
- [Arweave Image Uploader](https://github.com/thuglabs/arweave-image-uploader) ![](https://img.shields.io/github/stars/thuglabs/arweave-image-uploader.svg?style=social)
- [Permaweb Dropper](https://github.com/textury/permaweb-dropper) ![](https://img.shields.io/github/stars/textury/permaweb-dropper.svg?style=social)
- [Harbor](https://github.com/kevinrodriguez-io/harbor) ![](https://img.shields.io/github/stars/kevinrodriguez-io/harbor.svg?style=social)
- [Sol NFT Tools](https://sol-nft.tools/) - has an uploder section.

### Multi-function

- [Solana Tools](https://www.solana-tools.com/) - find PDAs, ATAs, and read NFT/token metadata from a mint address.
- [Sol NFT Tools](https://sol-nft.tools/) - get mints created by a creator, get metadata from a mint, get holders of a bunch of mints, upload files to arweave.
- [Skunka Tools](https://www.skunka-tools.xyz/) - SPL Token generator and manager, delete token accounts, burn tokens and more features to come.

### Dapp Boilerplates

- [Create Solana Dapp](https://github.com/thuglabs/create-dapp-solana-nextjs) - Scaffolding for a Solana dapp using TS, Next.JS, Tailwinds CSS, and Daisy UI.
- [Dapp Scaffold](https://github.com/solana-labs/dapp-scaffold) - Scaffolding for a dapp using TS, React & Antd.
- [sol-rayz](https://github.com/NftEyez/sol-rayz) - set of tools to quickly build NFT Galleries

## 🦾 Generative Art Tools

- [Hashlips Art Engine](https://github.com/HashLips/hashlips_art_engine)
  ![](https://img.shields.io/github/stars/HashLips/hashlips_art_engine.svg?style=social) - JS gen art generator.
- [NFT Image generator](https://github.com/benyaminahmed/nft-image-generator)
  ![](https://img.shields.io/github/stars/benyaminahmed/nft-image-generator.svg?style=social) - python code in jupyter notebooks for generative art.
- [Treat Toolbox](https://github.com/theskeletoncrew/treat-toolbox)
  ![](https://img.shields.io/github/stars/theskeletoncrew/treat-toolbox.svg?style=social) - drag and drop tool with a friendly UI to randomly combine layers into generative art.
- [NFT Maker](https://github.com/hempworks/nft-maker-js)
  ![](https://img.shields.io/github/stars/hempworks/nft-maker-js.svg?style=social) - NodeJS package to generate NFT images and JSON compatible with Metaplex's Candy Machine.
- [Solseum NFT generator](https://github.com/Solseum/solseum-nft-generator)
  ![](https://img.shields.io/github/stars/Solseum/solseum-nft-generator.svg?style=social) - python cli for genrative art with sophisticated tooling/charts around the rarity system.
- [Lifecycle NFT generator](https://github.com/lightcycleresearch/lightcycle-nft-generator)
  ![](https://img.shields.io/github/stars/lightcycleresearch/lightcycle-nft-generator.svg?style=social) - python cli for generative art.
- [Candy Maker](https://github.com/kevinrodriguez-io/candy-maker/)
  ![](https://img.shields.io/github/stars/kevinrodriguez-io/candy-maker.svg?style=social) - ts cli for generative art.
- [TIEXO](https://github.com/TiexoHQ/toolbox)
  ![](https://img.shields.io/github/stars/TiexoHQ/toolbox.svg?style=social) - generative NFT art toolbox from the creators of Moonlet.

## ⚙️ RPC Providers

- [GenesysGo](https://genesysgo.com/)
- [GetBlock](https://getblock.io/)
- [QuickNode](https://quicknode.com/)
- [RunNode](https://runnode.com/)
- [Triton One | RPC Pool](https://triton.one/#/)
- [Figment](https://figment.io/datahub/solana/)
- [Blockdaemon](https://blockdaemon.com/marketplace/solana/)
- [Syndica](https://syndica.io/)
- [NOWNodes](https://nownodes.io)
- [Node Monkey](https://marketplace.nodemonkey.io/)

## 🔗 Related Awesome Lists

- [Awsome Solana](https://github.com/paul-schaaf/awesome-solana) ![](https://img.shields.io/github/stars/paul-schaaf/awesome-solana.svg?style=social)
- [Awesome Serum](https://github.com/project-serum/awesome-serum) ![](https://img.shields.io/github/stars/project-serum/awesome-serum.svg?style=social)
- [Awesome Solana Gaming](https://github.com/murlokito/awesome-solana-gaming) ![](https://img.shields.io/github/stars/murlokito/awesome-solana-gaming.svg?style=social)
