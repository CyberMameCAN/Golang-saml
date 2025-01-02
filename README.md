# GolangでSAML

GolangでSAMLをハンズオンした記録になります。

## 参照

- [GolangでローカルでSAML認証を実装してみる](https://zenn.dev/akira_kuriyama/articles/79baaa90c56a39)
- [ローカル環境でテストに用に起動できるSAML-IdPサーバ](https://qiita.com/murasuke/items/f7cb7fd68cd1bf8ec74e)
- [SAML](https://github.com/crewjam/saml)


## 前準備

### インストール等

#### idP

npmでsaml-idpをインストールする。(参照URLを参考に)  

起動

    npm run saml-idp

#### SP

公開鍵と秘密鍵を生成(openssl)  


Golang

    go mod init smp16-saml
    go mod tidy


## 動作

以下、ブラウザでの操作

### 設定

idPにSPを初期設定する。

    http://localhost:7000/settings

### 

    http://localhost:8000/hello

URLにアクセス後、**Sign in**をクリックする。  
SPにリダイレクトされて、**Hello, saml jackson!**と表示されると成功。

