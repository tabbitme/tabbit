
![Group 15](https://github.com/tabbitme/tabbit/assets/8872443/0b9a83e6-0c9a-4cab-bbcd-dc3be7273073)


# TABBIT - 観光産業向けERC6551を活用したNFTチケット発行プロトコル

## 課題

**“現在の集客を維持したいが広告費が高い”**

顧客獲得とコスト削減は、企業収益の安定化と増加を目指す上で欠かせない要素です。しかし、集客活動に伴う広告費や予約プラットフォーム手数料は避けられず、これらが利益率の低下を招きます。特に旅行プラットフォーム(OTA)の手数料は平均で10~15%にも上り、事業者にとって重い負担となっています。


## 解決策

**“ガス代,ウォレット不要！NFTチケットで、新しい集客エコシステムをつくる”**

TABBITのNFTチケットサービスは、"新規顧客の獲得"と"コスト削減"、これらを一石二鳥に達成する新たな解決策を提供します。

- **『ユーザー主導のバイラルマーケティング』**：リピーター（ファン）を活用し、顧客自身が事業者の広告となることで、広告費を削減します。顧客はSNSを通じて自然な口コミを拡散し、新たな集客チャンネルとなります。
- 『**顧客の直接取引化』**：一度獲得した顧客を、Web2プラットフォームを介さないダイレクトなコミュニケーションで確実にリピーターへと育成します。予約プラットフォーム手数料を追加コストとせずに、持続的な関係を築くことが可能です。
- 

### ◎TechStack

| Title |                           詳細 |
| :------- | -----------------------------------------: |
| Token Bound Account (ERC6551)   | ERC6551はNFT(ERC721)を従来のWalletのような役割として活用できる新しい企画です。今回はエンドユーザーがWalletを持っていなくても、Wallet機能を活用できるように実装しました。 |
| Smart Contract Wallet(ERC4337)   | ERC6551をエンドユーザーがガス代負担なし、かつweb3のリテラシーがなくてもセキュアなWallet管理を実現するためにERC4337を活用したSmart Contract Walletを実装しました。 |
| PatchWallet/LitProtocol   | エンドユーザーがWalletを持つ前に、事業者がメールアドレスに紐づいたWalletアドレスを特定すること、そしてエンドユーザーがメール認証だけでWalletを持てるようにするために、PatchWallet/LitProtocolを活用しました。 |


### ◎ユーザーフロー

1. 顧客がその旅行関連商品を決済する ※今回実装しない
2. **事業者がサイト上で商品となるチケットNFTを発行 (ERC1155規格)**
3. TABBITが顧客のPass NFT(ERC721+ERC6551)を発行しチケットNFT(ERC1155)を自動で格納
4. **事業者が顧客のスマートコントラクトウォレットにPass NFTを送付**
5. 送付したことをメールで通知 ※今回実装しない
6. **顧客がサイトにアクセスする**
7. **メール認証（Walletが不要） ※ LitProtocol使用**
8. **チケットを受け取ったことを確認する**

### ◎各実装内容

**実装状況**

| Title |                           URL |
| :------- | -----------------------------------------: |
| デモ動画   | TBD |
| デモサイト   | https://tabbit-front.vercel.app/  |
| コントラクト   | [tabbit-contracts](https://github.com/tabbitme/tabbit-contracts) |
| フロントエンド   | [tabbit-front](https://github.com/tabbitme/tabbit-front) |

**Astarコントラクト**

| contract |                           contract address |
| :------- | -----------------------------------------: |
| ERC6511   | [TBD](https://blockscout.com/astar/address/0x010f494348f7fAdA7960369CFb51e08546665c9C#code) |
| ERC721   | [TBD](https://blockscout.com/astar/address/0x010f494348f7fAdA7960369CFb51e08546665c9C#code) |
| ERC1155   | [TBD](https://blockscout.com/astar/address/0x010f494348f7fAdA7960369CFb51e08546665c9C#code) |
| ERC6511registry   | [TBD](https://blockscout.com/astar/address/0x010f494348f7fAdA7960369CFb51e08546665c9C#code) |

**Mumbaiコントラクト**

| Contract |                           contract address |
| :------- | -----------------------------------------: |
| ERC6511   | [TBD](https://mumbai.polygonscan.com/address/0xf6d5ce08f45c8090f9da582b951f9EBA1B0336Fb#code) |
| ERC721   | [0x9FF927E3d79E34144fD831e67e389692B8AE82AC](https://mumbai.polygonscan.com/address/0x9FF927E3d79E34144fD831e67e389692B8AE82AC#readContract) |
| ERC1155   | [0x3E7E22f04b86e265BC181B4FB69f193bF3259A14](https://mumbai.polygonscan.com/address/0x3E7E22f04b86e265BC181B4FB69f193bF3259A14#readContract) |
| ERC6511registry   | [TBD](https://mumbai.polygonscan.com/address/0xf6d5ce08f45c8090f9da582b951f9EBA1B0336Fb#code) |






