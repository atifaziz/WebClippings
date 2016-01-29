# Web Clippings

Clip&middot;ping: _noun_ Something cut off or out, especially an item clipped from a newspaper or magazine.

Following is personal collection of mostly software-related articles and downloads that I have found useful and bookmarked for future reference:

## [Why write Python in Visual Studio?](http://blogs.msdn.com/b/visualstudio/archive/2015/08/03/why-write-python-in-visual-studio.aspx)

Recently, [Visual Studio 2015](http://www.microsoft.com/click/services/Redirect2.ashx?CR_CC=200661214) was released with support for Python. [Python Tools for Visual Studio](https://github.com/Microsoft/PTVS) (PTVS) are available to help throughout Visual Studio in all the places you’d expect, from editing and IntelliSense, to debugging, profiling, and publishing to Azure. You can find all the details and some [video walkthroughs, documentation, and other resources](https://aka.ms/ptvs) on visualstudio.com, and the post announcing [Python Tools 2.1](http://blogs.msdn.com/b/visualstudio/archive/2014/10/15/python-tools-2-1-for-visual-studio.aspx) and [Python Tools 2.2 beta](http://blogs.msdn.com/b/visualstudio/archive/2015/03/16/python-tools-for-visual-studio-2-2-beta-released.aspx). In this post I want to talk about some of the reasons to consider using Visual Studio next time you are working in Python.

Fri Jan 29 13:32:21 2016 +0100

Tags: `vs`, `python`

## [The .NET Framework 4.5 includes new garbage collector enhancements for client and server apps](http://blogs.msdn.com/b/dotnet/archive/2012/07/20/the-net-framework-4-5-includes-new-garbage-collector-enhancements-for-client-and-server-apps.aspx)

> In this post, we will look at how the CLR garbage collector (GC) has been changed in the .NET Framework 4.5 to meet the needs of large client and server apps. These improvements are in response to requests from developers who use the .NET Framework to build large-scale commercial apps. Some of these customers have already reported significant wins after deploying the .NET Framework 4.5 (currently available as an RC release) into production.

Tags: `dotnet`, `gc`

Fri Jan 29 13:29:19 2016 +0100

## [The Tipping Point Query Answers](http://www.sqlskills.com/blogs/kimberly/the-tipping-point-query-answers/)

> **What is the tipping point?** It's the point where the number of rows returned is "no longer selective enough". SQL Server chooses NOT to use the nonclustered index to look up the corresponding data rows and instead performs a table scan.

Tags: `mssql`, `db`, `unread`

Fri Jan 29 13:26:34 2016 +0100

## [R Programming Language - Introduction to R for C# Programmers](https://msdn.microsoft.com/en-us/magazine/Mt238409.aspx)

> The R language is used by data scientists and programmers for statistical computing. In part because of the increasing amounts of data collected by software systems, and the need to analyze that data, R is one of the fastest-growing technologies among my colleagues who use C#. A familiarity with R can be a valuable addition to your technical skill set.

Tags: `r`, `unread`

Fri Jan 29 13:22:06 2016 +0100

## [Recommendations and guidelines for the "max degree of parallelism" configuration option in SQL Server](https://support.microsoft.com/en-us/kb/2806535)

> The Microsoft SQL Server **max degree of parallelism** (`MAXDOP`) configuration option controls the number of processors that are used for the execution of a query in a parallel plan. This option determines the computing and thread resources that are used for the query plan operators that perform the work in parallel. Depending on whether SQL Server is set up on a symmetric multiprocessing (SMP) computer, a non-uniform memory access (NUMA) computer, or hyperthreading-enabled processors, you have to configure the **max degree of parallelism** option appropriately. This article discusses the general guidelines that you can use to configure the **max degree of parallelism** option for SQL Server when you use the `sp_configure` system stored procedure. 

Tags: `mssql`, `mskb`, `admin`

Fri Jan 29 13:16:34 2016 +0100
