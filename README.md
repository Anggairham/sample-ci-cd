# sample-ci-cd

### Tutorial
* Generetae SSH key
```
ssh-keygen -t rsa -b 4096 -C "test@gmail.com"
```
* The email is the one you use on your GitHub account
* Add a public key to authorized keys
```
cat ~/.ssh/id_rsa.pub >> ~/.ssh/authorized_keys
```