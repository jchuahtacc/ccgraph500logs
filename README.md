# ccgraph500logs

### Configuration

Requires hostfile and an RSA keypair. Create a keypair with no passphrase...

```
ssh-keygen -t rsa -b 4096 -C "github@emailaddress"
```

Then add the keypair to GitHub. Then...

```
ssh -T git@github.com
```

Make your GitHub project and delete the `.git` directory in this one. Then...

```
git init
git remote add origin git@github.com:/username/repo.git
git add .
git commit -m "Initial commit"
git push origin master
```

Modify the `runme` script to point to the keypair you just created, along with any number of processes and problem scale. You can run it headless with:

```
nohup ./runme &
```

Each complete run will push logs to your GitHub repo
