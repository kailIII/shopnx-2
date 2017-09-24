
# ShopNx - [MEAN] Angular4 + Node + Mongo

## Bitnami Password
Setting Bitnami application password to '5Ni8a5xnkcGj' 

ci-info: ++++++++Authorized keys from /home/bitnami/.ssh/authorized_keys for user bitnami+++++++++
ci-info: +---------+-------------------------------------------------+---------+-----------------+
ci-info: | Keytype |                Fingerprint (md5)                | Options |     Comment     |
ci-info: +---------+-------------------------------------------------+---------+-----------------+
ci-info: | ssh-rsa | 8d:8a:63:ca:6f:15:41:bb:35:df:2f:2d:cc:4e:a6:9e |    -    | MyFirstInstance |
ci-info: +---------+-------------------------------------------------+---------+-----------------+

ec2: 
ec2: #############################################################
ec2: -----BEGIN SSH HOST KEY FINGERPRINTS-----
ec2: 1024 65:d8:d8:bd:09:25:00:e8:74:86:5d:2c:47:b7:9c:97  root@ip-172-31-70-225 (DSA)
ec2: 256 98:c4:86:02:4e:f3:47:b4:04:d6:46:86:31:6b:5c:1c  root@ip-172-31-70-225 (ECDSA)
ec2: 256 8a:99:81:cd:62:44:57:af:66:1d:81:e9:ac:3a:73:db  root@ip-172-31-70-225 (ED25519)
ec2: 2048 45:4d:55:26:e7:d7:bf:30:4e:cf:05:b2:36:10:2b:ef  root@ip-172-31-70-225 (RSA)
ec2: -----END SSH HOST KEY FINGERPRINTS-----
ec2: #############################################################
-----BEGIN SSH HOST KEY KEYS-----
ecdsa-sha2-nistp256 AAAAE2VjZHNhLXNoYTItbmlzdHAyNTYAAAAIbmlzdHAyNTYAAABBBIV1BN6iz4UMTHXZYPA++8G/0euylqlKZ881PEm0UEeKo+bOF28+Vh2o9ofm1bPEFUPZsC1koPNxg+PwThc4QRs= root@ip-172-31-70-225
ssh-ed25519 AAAAC3NzaC1lZDI1NTE5AAAAIIIUmfB8vZcHDd0MHRmcFsfhERr2F+tv/V+k8fmXZlgE root@ip-172-31-70-225
ssh-rsa AAAAB3NzaC1yc2EAAAADAQABAAABAQD+75rbWLAgtEyTc1ANIB/9t1yE/gZ/zqkNCnL0fOEEvCmZff8ip1EJMYkmnv3ruujQ0bqjvpKOCouSfG8PAM+lz3lXDf/UyfWMCztTca828AwYcADamqi3LYjB9Tpbn5k9Rmp6QrVOwa81MVNgDS07EhCJxAImdDF2bapfJCuDM1me3JSWxV2X8Pw+Q/cpVASVXRsGmgRYBGpqQL7c62fzM87b5F3X2K5AsVbqMDK2J532Ic4khJfqjdsJhnd+Y3IPDxXEJHtyjgOx6rZ3dWxo6bL3NCe/9EXEHAvxIdZlM82ye7bhHe8qCkUHpxIY/MKjcbNs/D6FzPxA72wYrueh root@ip-172-31-70-225
-----END SSH HOST KEY KEYS-----

## Single page ecommerce using Angular4.

## Quick start
> Make sure you have **Node** version >= 8.0, **NPM** >= 5 and **MongoDB**

> Download and unzip the file from codecanyon

> Start mongodb in a separate shell

In Windows operating system we can start it by opening the following file

```bash
C:/Program Files/MongoDB/Server/3.2/bin/mongod.exe
```

```bash
# navigate inside the directory
cd shopnx

# install the dependencies with npm
npm i

# Start the server and client
npm start
```
go to [http://0.0.0.0:4200](http://0.0.0.0:4200) or [http://localhost:4200](http://localhost:4200) in your browser

## Build for production
```bash
npm run prod
```
The production version files will be available inside dist directory

## Deploy to Heroku

1. From command prompt navigate inside the dist directory

2. Copy .env, package.json to dist directory

3. Create a new File named Procfile

4. Add `web: node server/app` into Procfile

5. Install mLab heroku addon
```
heroku addons:create mongolab
```

6. Get MongoDB URI
```
heroku config:get MONGODB_URI
```
*MONGODB_URI => mongodb://heroku_12345678:random_password@ds029017.mLab.com:29017/heroku_12345678*


7. Open `.env` file and change the MONGODB_URI to the above generated URI