# Comparison Study of working with PDF data from the web using PowerBI And Pandas

I am following Gil Raviv blog posts on reading, cleaning and interpreting COVID data from WHO site for countries of the world. I am performig the same transformations that need to be applied to the data in Pandas as well and then verifying my results between the two.


There are two options to read the tabular data from https://www.who.int/docs/default-source/coronaviruse/situation-reports/20200715-covid-19-sitrep-177.pdf

* Read the relevant pages using Tabula_Py's read_pdf
* Download the PDF and convert it into a CSV file and then read the CSV file into a dataframe using pandas (note the encoding required here is Latin)

I chose the download option and converted the file into a CSV and then created a dataframe which requires further cleansing
