# Web Clippings

Clip&middot;ping: _noun_ Something cut off or out, especially an item clipped from a newspaper or magazine.

Following is personal collection of mostly software-related articles and downloads that I have found useful and bookmarked for future reference:

## [Recommendations and guidelines for the "max degree of parallelism" configuration option in SQL Server](https://support.microsoft.com/en-us/kb/2806535)

> The Microsoft SQL Server **max degree of parallelism** (`MAXDOP`) configuration option controls the number of processors that are used for the execution of a query in a parallel plan. This option determines the computing and thread resources that are used for the query plan operators that perform the work in parallel. Depending on whether SQL Server is set up on a symmetric multiprocessing (SMP) computer, a non-uniform memory access (NUMA) computer, or hyperthreading-enabled processors, you have to configure the **max degree of parallelism** option appropriately. This article discusses the general guidelines that you can use to configure the **max degree of parallelism** option for SQL Server when you use the `sp_configure` system stored procedure. 

Tags: `mssql`, `mskb`, `admin`

Fri Jan 29 13:16:34 2016 +0100
