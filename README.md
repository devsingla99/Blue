# LOG ANALYZER
### OBJECTIVE
This is a Log analyzer which takes a file as Input, extracts, parses and stores data in a format that can be used
to easily filter out activities based on different parameters and the final result should contains atleast following
information
1. IP Address
2. Frequency of ip address
3. User Agent
4. Status Code (200/401/500 etc).
5. Request Type (GET/POST/PUT etc)
6. API
### EXECUTION PART
To run the log analyser open the LOG_ANALYSER.ipynb and enter the path where log file is stored. The path will be stored in a variable file_location. The output file will be stored at location where jupyter notebook is installed.
### DEPENDENCY
* PYTHON3
* CSV (for installation   ----->>  pip install csv)
* RE (for installation   ----->>  pip install re)
### DESCRIPTION 
In this work sample provided to us we have taken a apache log file  which contains info regarding ip adress,user agent,status code,api,request type etc.
So we have decided to use regular expression for matching th pattern in the entire log file .
We first read the log file to see how different patterns can be uniquely identified.
Beginning with extracting ip adress . We have used regex tester and succesfully extracted ip adresses after write its regular expression.
We have stored all ip adresses in a list. We have also calculate frequency of each ip adress .Then we have extracted status code. Its identification in the given log file was that it is a 3 digit number and there was a space at before starting and at ending of status code.
After extracting it we have put it in a list. Then moving ahead we formed the regular expression for request type . We explored and found common request type like put,get,head,delete,connectetc.
And stored the result obtained in a list. Then we worked on extracting api and wrote regular expression for the same and stored all the api's in a list.
At last we created and empty data frame and embedded all the columns like ipadress,freq_ofipadress,user_agent,statuscode,api and request type.
After that we converted the data frame to csv file. So this we we extracted 6 things from the log file and saved it in a csv file.
