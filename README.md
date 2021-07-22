## running environment

* Linux (Debian 10)
* Windows 10
* macOS 10.14

## how to run

### first time only

* npm install
* edit cypress.env.json (username and password)

### after setup 

```
./node_modules/bin/cypress run
```


## appendix

### jenkins(on windows) automation

batch script is below

```
cd /d [your_cloned_dir]

call npm install
call node_modules\.bin\cypress install
call node_modules\.bin\cypress run --reporter markdown

exit %ERRORLEVEL%
```

### linux automation

```
#!/bin/bash -eu

cd /work/scripts/cypress-dl-autologin

# don't want colors on cypress output
# https://github.com/cypress-io/cypress/issues/3079
export NO_COLOR=1

./node_modules/.bin/cypress install
./node_modules/.bin/cypress run --reporter markdown
```
