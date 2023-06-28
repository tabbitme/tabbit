![Group 15](https://github.com/tabbitme/tabbit/assets/8872443/0b9a83e6-0c9a-4cab-bbcd-dc3be7273073)

# TABBIT - NFTで革新する観光のカタチ -

## 課題

**“現在の集客を維持したいが広告費が高い”**

顧客獲得とコスト削減は、企業収益の安定化と増加を目指す上で欠かせない要素です。しかし、集客活動に伴う広告費や予約プラットフォーム手数料は避けられず、これらが利益率の低下を招きます。特に旅行プラットフォーム(OTA)の手数料は平均で 10~15%にも上り、事業者にとって重い負担となっています。

## 解決策

**“ガス代,ウォレット不要！NFT チケットで、新しい集客エコシステムをつくる”**

TABBIT の NFT チケットサービスは、"新規顧客の獲得"と"コスト削減"、これらを一石二鳥に達成する新たな解決策を提供します。

- **『ユーザー主導のバイラルマーケティング』**：リピーター（ファン）を活用し、顧客自身が事業者の広告となることで、広告費を削減します。顧客は SNS を通じて自然な口コミを拡散し、新たな集客チャンネルとなります。
- 『**顧客の直接取引化』**：一度獲得した顧客を、Web2 プラットフォームを介さないダイレクトなコミュニケーションで確実にリピーターへと育成します。予約プラットフォーム手数料を追加コストとせずに、持続的な関係を築くことが可能です。

### ◎TechStack

| Title                          |                                                                                                                                                                                                                 詳細 |
| :----------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------: |
| Token Bound Account (ERC6551)  |                                      ERC6551 は NFT(ERC721)を従来の Wallet のような役割として活用できる新しい企画です。今回はエンドユーザーが Wallet を持っていなくても、Wallet 機能を活用できるように実装しました。 |
| Smart Contract Wallet(ERC4337) |                                           ERC6551 をエンドユーザーがガス代負担なし、かつ web3 のリテラシーがなくてもセキュアな Wallet 管理を実現するために ERC4337 を活用した Smart Contract Wallet を実装しました。 |
| PatchWallet/LitProtocol        | エンドユーザーが Wallet を持つ前に、事業者がメールアドレスに紐づいた Wallet アドレスを特定すること、そしてエンドユーザーがメール認証だけで Wallet を持てるようにするために、PatchWallet/LitProtocol を活用しました。 |

### ◎ ユーザーフロー

1. 顧客がその旅行関連商品を決済する ※今回実装しない
2. **事業者がサイト上で商品となるチケット NFT を発行 (ERC1155 規格)**
3. TABBIT が顧客の Pass NFT(ERC721+ERC6551)を発行しチケット NFT(ERC1155)を自動で格納
4. **事業者が顧客のスマートコントラクトウォレットに Pass NFT を送付**
5. 送付したことをメールで通知 ※今回実装しない
6. **顧客がサイトにアクセスする**
7. **メール認証（Wallet が不要） ※ LitProtocol 使用**
8. **チケットを受け取ったことを確認する**

### ◎ 各実装内容

**実装状況**

| Title          |                                                              URL |
| :------------- | ---------------------------------------------------------------: |
| ピッチ動画     |                                     https://youtu.be/XpNz4fmwth4 |
| デモ動画       |                                    https://youtu.be/zmENJzrxZRw |
| デモサイト     |                                 https://tabbit-front.vercel.app/ |
| コントラクト   | [tabbit-contracts](https://github.com/tabbitme/tabbit-contracts) |
| フロントエンド |         [tabbit-front](https://github.com/tabbitme/tabbit-front) |

**Astar コントラクト**

| contract                   |                                                                                                                   contract address |
| :------------------------- | ---------------------------------------------------------------------------------------------------------------------------------: |
| ERC721 - TabbitPass        | [0xFe055AeD04B5b1aBbD5ea7b4DF329a2B4E24A21A](https://blockscout.com/astar/address/0xFe055AeD04B5b1aBbD5ea7b4DF329a2B4E24A21A#code) |
| ERC1155 - TabbitTicket     | [0xC74399208F6Ea056d69Ad09a33eB25eAf8493a2b](https://blockscout.com/astar/address/0xC74399208F6Ea056d69Ad09a33eB25eAf8493a2b#code) |
| TokenBoundAccount(ERC6551) | [0xB3a856A657A57735b2C264A0a203eAF77e2ca57F](https://blockscout.com/astar/address/0xB3a856A657A57735b2C264A0a203eAF77e2ca57F#code) |
| ERC6511registry            | [0xdB803f3DB844DB02D14ffF738662A646A1D2C96d](https://blockscout.com/astar/address/0xdB803f3DB844DB02D14ffF738662A646A1D2C96d#code) |

**Mumbai コントラクト**

| Contract                   |                                                                                                                contract address |
| :------------------------- | ------------------------------------------------------------------------------------------------------------------------------: |
| ERC721 - TabbitPass        | [0x8C3cCd438A39ec57Df12841031D47d516C6a6c81](https://mumbai.polygonscan.com/address/0x8C3cCd438A39ec57Df12841031D47d516C6a6c81) |
| ERC1155 - TabbitTicket     | [0x1464D892F270D5746C3c12C6ED48f8DCdF3e673d](https://mumbai.polygonscan.com/address/0x1464D892F270D5746C3c12C6ED48f8DCdF3e673d) |
| TokenBoundAccount(ERC6551) | [0x261146F1A96021ab11C0541441016c731296b017](https://mumbai.polygonscan.com/address/0x261146F1A96021ab11C0541441016c731296b017) |
| ERC6511registry            | [0x02101dfB77FDE026414827Fdc604ddAF224F0921](https://mumbai.polygonscan.com/address/0x02101dfB77FDE026414827Fdc604ddAF224F0921) |
