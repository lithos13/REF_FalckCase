# REF_FalckCase
This case involves obtaining the list of the top 250 best-rated movies and, from that list, extracting the movies rated above 8.1 filmed after 2000. 
> [!NOTE]
> This is an addition made to the original case.

# Technical Requirements

- Google Chrome Versión 120.0.6099.111 (Build oficial) (64 bits)
- Microsoft® Excel® 2019 MSO (versión 2311 compilación 16.0.17029.20028) de 64 bits
- Uipath Studio 2023.12.0

# Automation
According to the requirements, this automation was developed as follows:
`This additional solution will use additional movie details, which are accessed by opening the movie URL`

![image](https://github.com/lithos13/REF_FalckCase/assets/68198144/350837ab-4fb9-4353-a791-97dd8b38274b)
 +  ![image](https://github.com/lithos13/REF_FalckCase/assets/68198144/328f2396-4303-467e-9643-74a859300e95)

> [!IMPORTANT]
>In this case, we use the ReFramework template, keeping in mind that the additional data is obtained by opening the movie URL, and the automation needs to iterate through all movies to obtain this additional data.
> The ReFramework was modified to work with DataTables and DataRow. This change was made because originally, it was designed to work with Queues and Queue Items.

## Initialization
In this section, we prepare the data, which will be the list of movies filmed after the year 2000 and rated above 8.1. After obtaining this data, let's add three more columns to the movies' data table.
![image](https://github.com/lithos13/REF_FalckCase/assets/68198144/dcbb3813-ed09-4084-bca5-7da6986d75e4)

> [!NOTE]
> The sequence to obtain this data is the same as in the [original case](https://github.com/lithos13/FalckCase/blob/main/README.md).


## Get Transaction Data
Each transaction corresponds to a movie along with its respective URL.
![image](https://github.com/lithos13/REF_FalckCase/assets/68198144/4688ffe6-e08f-4bca-815b-40e3dc0ba6ff)

## Process Transaction
"In this section, the automation opens the URL to obtain data for `Description`, `Director`, and `Stars`.
![image](https://github.com/lithos13/REF_FalckCase/assets/68198144/5bc9e2e0-dc92-467e-81f8-23a618f6eaea)

and adds each one of them to their respective columns in the DataTable..
![image](https://github.com/lithos13/REF_FalckCase/assets/68198144/ad8afe23-1166-41c7-b709-45d35327a296)



## End Process
Finally, with the complete data, let's save it in an Excel file: Project's folder 'Data\Temp\dt_top250MoviesResult.xlsx.
![image](https://github.com/lithos13/REF_FalckCase/assets/68198144/97a0d8ae-3c22-4799-8e9b-a895f452cf79)

