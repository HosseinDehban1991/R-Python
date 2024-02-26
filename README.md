
 title: "Use R and Python Together"
 #!title: "Use R and Python Together"
# author: "Hossein Dehban_Feb 2024"

# Step1: Install Python
  # Install python on your system: (https://www.python.org/)
  # Step2: Install R and Rstudio
  # Install R on your system: (https://www.r-project.org/)
  # Install Rstudio on your system: (https://posit.co/download/rstudio-desktop/)
  #! Installing essential libraries in R ( from CRAN Repository or other methods)
# Step3: Setting the Python path in Rstudio
   #! Open Rstudio —> Tools —> Global Options —> click python(left menu bar) —>
# Set python interpreter :
# -----Install python module (library)------------------------
# A: python environment (open cmd and type : pip install module)

# Example: pip install pandas
# B: R environment (install and load reticulate library in R)
install.packages('reticulate')
library(reticulate)
#! install pandas by py_install( )
# Example: 
py_install("pandas")
#---------------------------------------------------
# Step4: Writing Python and R code together
# reticulate is a library for writing Python code in R
#Open Rstudio
#install.packages('reticulate')
# load reticulate
library(reticulate)
#--------------------------------------------------------------
# Load python library (for exmple : pandas as pd)
# in python environment ~ import pandas as pd
# in R environment:
pd <- import('pandas')
# Using pandas function (Example: read .xlsx file using pandas library in R)
pd <- import('pandas')
myxlsfile <- pd$read_excel('test.xlsx')

# read .xlsx file using R Library(such as openxlsx)
library(openxlsx)
myxlsfile2 <- read.xlsx(xlsxFile = 'test.xlsx')
#--------------------------------------
# Email: Dehbanh@gmail.com
