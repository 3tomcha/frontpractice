# Frontend Practice

## Contributors

- [株式会社 D-Chain](https://d-chain.co.jp)

## 目次

- [環境構築](#環境構築)

  - [nvm ( Node Version Manager ) のインストール](#nvm-node-version-manager-のインストール)
    - [Mac](#mac)
    - [Windows](#windows)
  - [Node.js のインストール](#nodejs-のインストール)

- [このレポジトリについて](#このレポジトリについて)
  - [仕様](#仕様)

---

# 環境構築

## 1. nvm ( Node Version Manager ) のインストール

- ### Mac

  1. `command` + `space` で Spotlight Search を開き、 `terminal` と入力

  2. 以下のコマンドの **どちらか** を入力し `return`

     ```zsh
     curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.7/install.sh | bash
     ```

     ```zsh
     wget -qO- https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.7/install.sh | bash
     ```

  3. 以下のコマンドを実行し、正常にインストールされているか確認 ( `nvm` と表示されたら OK )

     ```zsh
     command -v nvm
     ```

     - `nvm: command not found` が出る場合、以下のコマンド実行してみてください

       - bash の場合

         ```bash
         source ~/.bash_profile
         ```

       - zsh の場合

         ```zsh
         source ~/.zshrc
         ```

---

- #### 上記通りにやってもうまくいかない場合

  - [ここ](https://github.com/nvm-sh/nvm?tab=readme-ov-file#troubleshooting-on-macos)を参照しトラブルシューティングを行ってください

- ### Windows

  - #### インストーラーを使用する場合

    1. [ここ](https://github.com/coreybutler/nvm-windows/releases/download/1.1.12/nvm-setup.zip)からインストーラーをダウンロード ( zip ファイル )

    2. zip を展開し、インストーラーに従ってください ( 全て `Next` で進んで構いません、設定を変えたい人はご自由にどうぞ )

  - #### WSL2 ( Windows Subsystem for Linux 2 ) にインストールする場合

    - ディストリビューション `Ubuntu:22.04`

    1. 以下のコマンドを実行し、ディストリビューションを更新する ( 推奨 )

       ```ubuntu
       sudo apt update && sudo apt upgrade
       ```

    2. 以下のコマンドを実行し、cURL をインストール

       ```ubuntu
       sudo apt-get install curl
       ```

    3. 以下のコマンドを実行し、nvm をインストール

       ```ubuntu
       curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/master/install.sh | bash
       ```

    4. 以下のコマンドを実行し、正常にインストールされているか確認

       ```ubuntu
       nvm -v
       ```

       - `0.39.7`等，バージョン情報が出てくれば OK です
       - `Command 'nvm' not found ...` が出る場合、現在のターミナルを閉じてから再度開き、もう一度やり直してください
       - もしくは
         ```ubuntu
         source ~/.bashrc
         ```
         と実行したあとに再度「nvm -v」を打ってみてください．

---

- #### 上記通りにやってもうまくいかない場合

  - [ここ](https://github.com/nvm-sh/nvm?tab=readme-ov-file#troubleshooting-on-linux)を参照しトラブルシューティングを行ってください

## 2. Node.js のインストール

- Mac はターミナル、Windows はコマンドプロンプト ( または WSL ) を開いておいてください

1. 以下のコマンドを実行し、`Node.js: 20.14.0` をインストール

   ```cmd
   nvm install 20.14.0
   ```

2. 以下のコマンドを実行し、`Node.js: 20.14.0` を使用しているか確認 ( `v20.14.0` と表示されたら OK )

   ```cmd
   node --version
   ```

   - 違うバージョンが表示される場合、以下のコマンドを実行してください

     ```cmd
     nvm use 20.14.0
     ```

- また以下のコマンドを実行し、`npm` があることも確認してください

  ```cmd
  npm --version
  ```

# このレポジトリについて

## 仕様

- 対応ブラウザ： Chrome ( JavaScript を許可してください )
- 対応デバイス： PC
- 対応ウォレット： MetaMask ( Chrome 拡張機能 )
- local Storage を使用

- Indexer 無し
- DB 無し
- Backend ( Server, Server Action ) 無し

## 使用パッケージ

- `wagmi` : latest ( 10.7.0 )
- `tailwindcss` : ^3.4.3
- `typescript` : ^5.2.2
- `shadcn-ui` : 0.8.0
- `react-hook-form`: ^7.51.5

## 始め方

1. レポジトリをクローンする

   - SSH を設定してある場合

     ```cmd
     git clone git@github.com:blockchaininnovation/frontpractice.git
     ```

   - HTTPS を使用する場合

     ```cmd
     git clone https://github.com/blockchaininnovation/frontpractice.git
     ```

2. クローンしたディレクトリに移動し、以下のコマンドを実行

   ```cmd
   cd wagmi-project
   ```

   ```cmd
   npm install
   ```

   ```cmd
   npm build
   ```

   ```cmd
   npm start
   ```

3. ブラウザで以下にアクセス

   http://localhost:3000 または http://127.0.0.1:3000
