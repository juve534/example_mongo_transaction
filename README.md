# example_mongo_transaction
MongoDBのトランザクションを試してみる

## MongoDB4.0のインストール

[公式の手順](https://docs.mongodb.com/master/tutorial/install-mongodb-on-red-hat/)に従ってインストールしていきます。

### repo用意

```:/etc/yum.repos.d/mongodb-org-3.2.repo
[mongodb-org-4.0]
name=MongoDB Repository
baseurl=https://repo.mongodb.org/yum/redhat/$releasever/mongodb-org/4.0/x86_64/
gpgcheck=1
enabled=1
gpgkey=https://www.mongodb.org/static/pgp/server-4.0.asc
```

### インストール実施

```
yum install -y mongodb-org-4.0.0 mongodb-org-server-4.0.0 mongodb-org-shell-4.0.0 mongodb-org-mongos-4.0.0 mongodb-org-tools-4.0.0
```

### 立ち上げ

```
service mongod start
```

### 起動確認

```
$ mongo
MongoDB shell version v4.0.0
connecting to: mongodb://127.0.0.1:27017
MongoDB server version: 4.0.0
```

## 参考資料
* [Install MongoDB Community Edition on Red Hat Enterprise or CentOS Linux — MongoDB Manual](https://docs.mongodb.com/master/tutorial/install-mongodb-on-red-hat/)