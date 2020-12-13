# Twitter-streaming
A REST API which streams Twitter data and stores them in a database.

Twitter Streaming API was used to stream real time twitter data based on some keywords. Also the number of tweets that you want to extract can be passed as a parameter to the function which implements streaming.

The streamed data was stored in a database on which some built-in queries can be applied.

Also, the stored tweets in the database can be exported to a csv file for further analysis.

Some functionalities of the API are:
1. store_tweets - This class streams twitter data based on some keywords and stores them in a database.

                  It takes two parameters : 
                  i) query word   
                  ii)number of tweets to stream
                  e.g. - <ip_address>/store_tweets/cricket/10
                 
2. show_data  - This class shows all the twitter data stored in the database.

                e.g. - <ip_address>/show_data

3. table_size - This class shows the size of the table (SQL) or size of the collection (NoSQL).

                e.g. - <ip_address>/table_size

4. table_name - This class shows the name of the table or collection.

                e.g. - <ip_address>/table_name

5. delete_table - This class deletes the twitter table or collection.

                  e.g. - <ip_address>/delete_table
                  
6. column_names - This class shows the columns of the twitter data.

7. filter_int - This class filters the integer columns based on some user input.

                It takes three parameters:
                i)  Column Name - The column which is to be filtered.
                ii) Operator  (e.g. - < , > , = )
                iii) Number - The number by which to filter. 
                e.g. - <ip_address>/filter_int/FollowerCount/</10
                
8. filter_string - This class filters the string columns based on some user input.

                   It takes three parameters:
                    i)  Column Name - The column which is to be filtered.
                    ii) Operator  (e.g. - starts , ends , = , contains )
                    iii) Text - The text by which to filter. 
                    e.g. - <ip_address>/filter_string/ScreenName/starts/ani
                    
9. sort - This class sorts the collection or table according to a particular column.

          It takes two parameters : 
          i) Column - The name of the column to be sorted.
          ii) Operator - Specifies whether to sort in ascending or descending order (e.g. - asc , desc)
          e.g. - <ip_address>/sort/RetweetCount/asc
          
10. date_range - This class shows the data in a specified range of dates.

                 It takes two parameters :
                 i) from_date - The start of the date range
                 ii) to_date - The end of the date range
                 e.g. - <ip_address>/date_range/2018-03-21/2018-03-27
                 
11. export_csv - This class exports the twitter data stored in the database to a csv file on the local machine.

                 It takes one parameter : 
                 i) File path - The location of the csv file on the local machine.
                 e.g. - <ip_address>/export_csv/F-files-tweet.csv
                 
12. custom - This class queries the data based on some user specified query. (only for SQL)

                   It takes one parameter:
                   i) query - The custom SQL query. 
                   e.g. - <ip_address>/custom/SELECT * FROM Twitter_data WHERE Language != 'en'
