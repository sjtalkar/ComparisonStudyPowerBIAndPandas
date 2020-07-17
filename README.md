# Comparison Study of working with PDF data from the web using PowerBI And Pandas

I am following Gil Raviv blog posts on reading, cleaning and interpreting COVID data from WHO site for countries of the world. I am performig the same transformations that need to be applied to the data in Pandas as well and then verifying my results between the two.


There are two options to read the tabular data from https://www.who.int/docs/default-source/coronaviruse/situation-reports/20200715-covid-19-sitrep-177.pdf

* Read the relevant pages using Tabula_Py's read_pdf
* Download the PDF and convert it into a CSV file and then read the CSV file into a dataframe using pandas (note the encoding required here is Latin)

I chose the download option and converted the file into a CSV and then created a dataframe which requires further cleansing


Cleaning:
* Remove columsn with null values - Here we have continent rows with no data. We can use dropna with the All option and in PowerBI we can filter out rows
* The second challenge is that space characters are used as the thousands separator. There are several ways to solve it.
  Here is one:df['Total confirmed cases'] = df['Total confirmed cases'].apply(lambda x: x.replace(' ',''))
* Now you can convert the numerical columns. Click the left icon in each of the numerical column headers and select Whole Number.
* The addtional cleanups include removing bottom rows, repeated header rows

