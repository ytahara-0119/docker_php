# ローカルPHP環境作成
ローカルにPHP環境をさくっと作ります。
nginx mysql5.7 php7.4

## 1. 事前にDOCKERとDOCKER-COMPOSEを使えるようにしておく
terminalでコマンドを打って確認する。
![image1](img/1.png)

## 2. git cloneする
git clone https://github.com/ytahara-0119/docker_php.git


## 3. ファルダ構成
```bash
docker_php
├── README.md
├── docker-compose.yml
├── mysql
│   └── data
├── nginx
│   └── nginx.conf
├── php
│   ├── Dockerfile
│   └── php.ini
└── www
    └── html
          └── index.php このファイルを書き換えたり、このフォルダに新しいプログラムを追加したり  
```
## 4. dockerフォルダでdocker-compose up -d ビルドと起動
`docker-compose up -d`

## 5. dokcer ps でコンテナが起動してるか確認
![image2](img/2.png)
## 6. localhost:8080でアクセス
![image3](img/3.png)

## 7. localhost:8888でphpmyadminにアクセスできる
![image4](img/4.png)
passwordはデフォルトでroot

## 8. 終了するときはdocker-compose stop
`docker-compose stop`
一度ビルドした後の起動は
`docker-compose up`
