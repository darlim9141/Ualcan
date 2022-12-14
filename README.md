## Ualcan scraping program


This program is for get expression value and P value from [ualcan](http://ualcan.path.uab.edu) web page
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
ex)
```c
  from webdriver_manager.chrome import ChromeDriverManager
```
```c
  driver = webdriver.Chrome(execuatable_path=ChromeDriverManager().install())
```

After download Web driver, __change the code line 5 and 12__ accoring to [this](https://github.com/SergeyPirogov/webdriver_manager). Don't forget to install webdriver_manager to before change the code
```c
  pip install webdriver-manager
```

Make excel file at same directory of this program, the first row of the excel file have gene name


Symbol|Expression value|Survival P value|TPM<1|unwanting gene
---|---|---|---|---|
HN1|||||
ZNF580|||||
...



# File
These files are need to be in same directory, before running the program


* driver.py

* store.xlsx -> for saving the values from the web page

* webdriver.exe -> need to run the program(don't necesssary need to be this directory)

* webdriver.log -> automatically generated files when running a program, deleting it doesn't matter



# Usage
You have to set up several variable at line 15~19


* __path = "C:\\. . ."__  
assign your directory of program file (line 15)
  
  ex)
  ```c
    path = "C:\\Users\\harim\\sele\\"
  ```


* __download_path = "C:\\. . ."__  
assign your download directory (use for download and upload PDF file) (line 16)

  ex)
  ```c
    download_path = "C:\\Users\\harim\\Downloads\\"
  ```


* __file = ". . .xlsx"__ 
assign excel file name (line 17)
  
  ex)
  ```c
    file = "store.xlsx"
  ```


* __row_number = ". . ."__  
assign row number of excel file that program will start reading, don't use quotation mark for this variable (line 18)

  ex)
  ```c
    row_number = 5604
  ```
  
  
* __last_row = ". . ."__
assing the row number of last gene name (line 19)

  ex)
  ```c
    last_row = 9554
  ```


If you want to change the standard for classifying unnecessary genes, check line 84 to 104
