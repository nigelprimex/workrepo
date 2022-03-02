# workrepo
Example of how to setup a 2nd ssh credential file, to work with a 2nd github account from one machine.

For example if you have one account for your job, and another personal one.

## First generate a new ssh key

## In your repository settings add 'sshCommmand'
```
#> git config core.sshCommand "ssh -i ~/.ssh/yournewkeyfile -o IdentitiesOnly=yes"
```

## If you originally cloned the repo via https, change to ssh.
Edit your .git/config [remote "origin"] from 
```
url = https://github.com/nigelprimex/workrepo.git
```

to:

```
url = git@github.com:nigelprimex/workrepo.git
```

## Otherwise set up an "origin" remote.
```
#> git remote add origin git@github.com:nigelprimex/workrepo.git
```
