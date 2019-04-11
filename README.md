## running environment

* macOS 10.14 (mojave)
* Windows 10

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

#### note

cypress not have CI friendry output option.
https://github.com/cypress-io/cypress/issues/3079