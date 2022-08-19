## Ualcan scraping program


This program is for get expression value and P value from [ualcan](http://ualcan.path.edu) web page
automatically and markdown the characters of the certain gene that user wants


# Prerequisite


Before start a program, install [selenium library](https://www.selenium.dev/documentation/webdriver/getting_started/install_library/)
```c
  pip install selenium
```
```c
  conda intall selenium
```
 
 
Also download the [Web driver](https://www.selenium.dev/documentation/webdriver/getting_started/install_drivers/) want to use for program, Download the same version of the web driver as your current browser.


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
You have to set up several variable at line 17 ~ 21


* __path = "C:\\. . ."__  
assign your directory of program file (line 17)
  
  ex)
  ```c
    path = "C:\\Users\\harim\\sele\\"
  ```


* __download_path = "C:\\. . ."__  
assign your download directory (use for download and upload PDF file) (line 18)

  ex)
  ```c
    download_path = "C:\\Users\\harim\\Downloads\\"
  ```


* __file = ". . .xlsx"__ 
assign excel file name (line 19)
  
  ex)
  ```c
    file = "store.xlsx"
  ```


* __row_number = ". . ."__  
assign row number of excel file that program will start reading, don't use quotation mark for this variable (line 20)

  ex)
  ```c
    row_number = 5604
  ```
  
  
* __last_row = ". . ."__
assing the row number of last gene name

  ex)
  ```c
    last_row = 9554
  ```


If you want to change the standard for classifying unnecessary genes, check line 85 to 105
