## Ualcan scraping program

This program is for get expression value and P value from [ualcan](http://ualcan.path.edu) web page
automatically and markdown the characters of the certain gene that user wants


# Prerequisite

Before start a program, you need to install [selenium library](https://www.selenium.dev/documentation/webdriver/getting_started/install_library/)
```c
  pip install selenium
```
```c
  conda intall selenium
```

Also download the [Web driver](https://www.selenium.dev/documentation/webdriver/getting_started/install_drivers/) that you want to use for program
Make sure download the same version of the Webdriver of your currently using browser



After download Web driver, change the code line 5 and 14 accoring to [this](https://github.com/SergeyPirogov/webdriver_manager). Don't forget to install webdriver_manager to before change the code
```c
  pip install webdriver-manager
```

Make excel file at same directory of this program, the first row of the excel file need have gene name, and other row have to be empthy

Symbol|Expression value|Survival P value|TPM<1|unwanting gene
---|---|---|---|---|
HN1|||||
ZNF580|||||
...



# File
These files are need to be in same directory, before running the program

* driver.py -> 
* store.xlsx -> for saving the values from the web page
* webdriver.exe -> need to run the program(don't necesssary need to be this directory)



# Usage
You have to set up several variable at line 17 ~ 20 and line 147

* path = "C:/..." assign your directory of program file
  
  ex)```
      path = "C:/Users/harim/sele/"
      ```

* download_path = "C:/..." assign your download directory (use for download and upload PDF file)

  ex)```
      download_path = "C:/Users/harim/Downloads/"
      ```

* file = "...xlsx" assign excel file name
  
  ex)```
      file = "store.xlsx"
      ```

* row_number = "...." assign row number of excel file that program will start reading, for this variable don't use quotation mark

  ex)```
      row_number = 5604
      ```
