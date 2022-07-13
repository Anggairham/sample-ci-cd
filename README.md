# sample-ci-cd

### Referensi
* https://dev.to/knowbee/how-to-setup-continuous-deployment-of-a-website-on-a-vps-using-github-actions-54im
* https://dev.to/miangame/how-to-automate-a-deploy-in-a-vps-with-github-actions-via-ssh-101e
* https://stackoverflow.com/questions/63480433/how-to-run-a-github-action-from-a-branch-other-than-master
* https://github.com/actions/checkout/discussions/277

### Copy Via SSH for VUE,React,Angular
* https://sivabalanb.medium.com/deploy-react-app-to-vps-digitalocean-vultr-using-git-actions-5766be8d2961
* https://github.com/marketplace/actions/copy-via-ssh

### Workflow
* After a better reading of https://docs.github.com/en/actions/reference/events-that-trigger-workflows specially the last part, seems that the ./github/workflows/* must be present in all the involved branches in order to make things work as I expected
* Workflow harus ada di branch terkait
* For example, if the event occurred on a particular repository branch, then the workflow files must be present in the repository on that branch.
### Skip based on commit message
* https://github.com/marketplace/actions/skip-based-on-commit-message

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

* Oh iya, sebelum menjalankan workflows ini, pastikan di server teman — teman sudah pernah melakukan clone projek ini. sebagai contoh projek saya tadi ada di lokasi ~/app/example-ci-cd-auto-deploy-vps . maka saya harus mengclone dulu di server untuk pertama kali.
