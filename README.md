## Ualcan scraping program

This program is for get expression value and P value from [ualcan](http://ualcan.path.edu) web page
automatically and markdown the characters of the certain gene that user wants


#Prerequisite

Before start a program, you need to install [selenium library](https://www.selenium.dev/documentation/webdriver/getting_started/install_library/)
```c
  pip install selenium
```
```c
  conda intall selenium
```

Also download the [Web driver](https://www.selenium.dev/documentation/webdriver/getting_started/install_drivers/) that you want to use for program
Make sure download the same version of the Webdriver that you currently using Web browser



After download Web driver, change the code line 5 and 14 accoring to [this](https://github.com/SergeyPirogov/webdriver_manager), please make sure to install webdriver-manager and after add code following to your using browser
```c
  pip install webdriver-manager
```

Make excel file at same directory of this program, the first row of the excel file need have gene name, and other row have to be empthy

Symbol|Expression value|Survival P value|TPM<1|unwanting gene
---|---|---|---|---|
HN1|||||
ZNF580|||||
.
.
.
