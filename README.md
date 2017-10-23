# Web Clippings

Clip&middot;ping: _noun_ Something cut off or out, especially an item clipped from a newspaper or magazine.

Following is personal collection of mostly software-related articles and downloads that I have found useful and bookmarked for future reference:

## [How JavaScript works: inside the V8 engine + 5 tips on how to write optimized code](https://blog.sessionstack.com/how-javascript-works-inside-the-v8-engine-5-tips-on-how-to-write-optimized-code-ac089e62b12e)

> [The first post of the series](https://blog.sessionstack.com/how-does-javascript-actually-work-part-1-b0bacc073cf) focused on providing an overview of the engine, the runtime and the call stack. This second post will be diving into the internal parts of Google’s V8 JavaScript engine. 

Tags: `javascript`, `optimization`, `performance`, `v8`

Mon Oct 23 22:26:30 2017 +0200

## [How to Write a Git Commit Message](https://chris.beams.io/posts/git-commit/)

> 1. Separate subject from body with a blank line
> 2. Limit the subject line to 50 characters
> 3. Capitalize the subject line
> 4. Do not end the subject line with a period
> 5. Use the imperative mood in the subject line
> 6. Wrap the body at 72 characters
> 7. Use the body to explain what and why vs. how

Tags: `git`

## [Yours, Mine and Ours](http://ericsink.com/articles/Yours_Mine_Ours.html)

> I claim here that there are three categories of software:
>
> - MeWare:  The developer creates software.  The developer uses it.  Nobody else does.
> - ThemWare:  The developer creates software.  Other people use it.  The developer does not.
> - UsWare:  The developer creates software.  Other people use it.  The developer uses it too.
>
> For completeness, I suppose I should probably mention the obvious fourth category:
>
> - NobodyWare:  The developer creates software.  Nobody uses it.

Tags: `software`

Mon Oct 16 13:46:27 2017 +0200

## [Better bitmap performance with Roaring bitmaps](https://arxiv.org/pdf/1402.6407.pdf)

> Bitmap indexes are commonly used in databases and search engines. By exploiting bit-level parallelism, they can significantly accelerate queries. However, they can use much memory, and thus we might prefer compressed bitmap indexes. Following Oracle's lead, bitmaps are often compressed using run-length encoding (RLE). Building on prior work, we introduce the Roaring compressed bitmap format: it uses packed arrays for compression instead of RLE. We compare it to two high-performance RLE-based bitmap encoding techniques: WAH (Word Aligned Hybrid compression scheme) and Concise (Compressed _n_ Composable Integer Set). On synthetic and real data, we find that Roaring bitmaps (1) often compress significantly better (e.g., 2x) and (2) are faster than the compressed alternatives (up to 900x faster for intersections). Our results challenge the view that RLE-based bitmap compression is best.

Tags: `performance`, `pdf`

Wed Oct 04 10:11:01 2017 +0200

## [Why are there so many implementations of Object Pooling in Roslyn?](https://stackoverflow.com/a/30736257/6682)

> I'm the lead for the Roslyn performance v-team. All object pools are designed to reduce the allocation rate and, therefore, the frequency of garbage collections. This comes at the expense of adding long-lived (gen 2) objects. This helps compiler throughput slightly but the major effect is on Visual Studio responsiveness when using the VB or C# IntelliSense.

Tags: `c#`, `roslyn`, `memory`

Wed Sep 27 23:09:00 2017 +0200

## [Functional C# (5) Local Function and Closure](https://weblogs.asp.net/dixin/functional-csharp-local-function-and-closure)

Tags: `c#`

Tue Sep 26 17:04:33 2017 +0200

## [RFC 7806: Problem Details for HTTP APIs](https://tools.ietf.org/html/rfc7807)

> This document defines a "problem detail" as a way to carry machine-readable details of errors in a HTTP response to avoid the need to define new error response formats for HTTP APIs.

Tags: `http`, `http-api`, `json`, `diagnostics`, `rfc`

Thu Sep 21 13:09:22 2017 +0200

## [Zero Garbage Collector for .NET Core](http://tooslowexception.com/zero-garbage-collector-for-net-core/)

> Starting from .NET Core 2.0 coupling between Garbage Collector and the Execution Engine itself have been loosened. Prior to this version, the Garbage Collector code was pretty much tangled with the rest of the CoreCLR code. However, [Local GC initiative](https://github.com/dotnet/coreclr/projects/3) in version 2.0 is already mature enough to start using it. The purpose of the exercise we are going to do is to **prepare Zero Garbage Collector that replaces the default one**.

Tags: `gc`, `.net`

Tue Sep 19 10:09:17 2017 +0200

## [How to retrieve indexed source files of a portable executable binary file](https://support.microsoft.com/en-us/help/3195907/how-to-retrieve-indexed-source-files-of-a-portable-executable-binary-file)

> This article describes how to retrieve the indexed source files of a portable executable (PE) binary file from source control by using information that's stored in the PE binary file's pairing program database (PDB) file. Because the indexed source files have their hash values embedded in the PDB file, these hash values can be used to verify the authenticity of the source files during their retrieval. 

Tags: `mskb`, `debugging`

Wed Mar 29 23:26:41 2017 +0200

## [Dissecting the `new()` constraint in C#: a perfect example of a leaky abstraction](https://blogs.msdn.microsoft.com/seteplia/2017/02/01/dissecting-the-new-constraint-in-c-a-perfect-example-of-a-leaky-abstraction/)

> This is a fairly long post, but we managed to cover many interesting details.
>
> - The `new()` constraint in the C# language is extremely leaky: in order to use it correctly and efficiently the developer should understand the implementation details of the compiler and the BCL.
> - We've figured out that the C# compiler calls `Activator.CreateInstance<T>` for creating an instance of a generic argument with a `new()` constraint (but remember, this is true only for C# 6+ compilers and the older versions emit the call only for reference types).
> - We've discovered the implications of the `Activator.CreateInstance` from a developer's point of view in terms of correctness and performance.
> - We've come up with a few alternatives, starting with a very simple one that _unwraps_ `TargetInvocationException`, to a fairly sophisticated solution based on code generation.
> - We've discussed a few interesting aspects of the generics implementation in the CLR and their impact on the performance (very minor, and likely negligible in the vast majority of cases).
> - And finally, we've come up with a solution that can solve aforementioned issues with the `new()` constrained by using the custom `System.Activator.CreateInstance<T>` implementation.

Tags: `dotnet`, `c#`, `performance`

Tue Mar 28 17:05:58 2017 +0200

## [Locks and exceptions do not mix](https://blogs.msdn.microsoft.com/ericlippert/2009/03/06/locks-and-exceptions-do-not-mix/)

> A couple years ago I wrote a bit about how our codegen for the lock statement could sometimes lead to situations in which an unoptimized build had [different potential deadlocks](http://blogs.msdn.com/ericlippert/archive/2007/08/17/subtleties-of-c-il-codegen.aspx) than an optimized build of the same source code. This is unfortunate, so we’ve fixed that for C# 4.0. However, all is still not [rainbows, unicorns and Obama](http://iamchriscollins.com/badpaintingsofbarackobama/images/4.jpg), as we’ll see.

Tags: `c#`, `threading`

Tue Mar 07 15:06:54 2017 +0100

## [Anonymous Recursion in C#](https://blogs.msdn.microsoft.com/wesdyer/2007/02/02/anonymous-recursion-in-c/)

> [Recursion](http://en.wikipedia.org/wiki/Recursion) is beautiful and [lambdas](http://en.wikipedia.org/wiki/Lambda_calculus) are the ultimate abstraction.  But how can they be used together?  Lambdas are anonymous functions and recursion requires names

Tags: `c#`, `fp`

Tue Mar 07 09:44:19 2017 +0100

## [Making Money Using Math](http://queue.acm.org/detail.cfm?id=3055303)

> Modern applications are increasingly using probabilistic machine-learned models

> Machine learning, or ML, is all the rage today, and there are good reasons for that. Models created by machine-learning algorithms for problems such as spam filtering, speech and image recognition, language translation, and text understanding have many advantages over code written by human developers. Machine learning, however, is not as magical as it sounds at first. In fact, it is rather analogous to how human developers create code using test-driven development.

Tags: `math`, `ml`, `ai`, `fp`, `cs`

Fri Feb 24 16:44:58 2017 +0100

## [getline.cs update: Partying like it is 1992](http://tirania.org/blog/archive/2016/Jan-14.html)

> Back in 2008, I wrote about `getline.cs`, a single-file command line editor for shell application. It included Emacs key bindings, history, customizable completion and incremental search. It is equivalent to GNU's readline library, except it is implemented in a [single C# file](https://github.com/mono/mono/blob/master/mcs/tools/csharp/getline.cs).

> I recently updated getline.cs to add a popup-based completion and C# heuristics for when to automatically trigger code completion.

Mon Feb 20 18:33:39 2017 +0100

## [The TTY demystified](http://www.linusakesson.net/programming/tty/)

> The TTY subsystem is central to the design of Linux, and UNIX in general. Unfortunately, its importance is often overlooked, and it is difficult to find good introductory articles about it. I believe that a basic understanding of TTYs in Linux is essential for the developer and the advanced user.

Tags: `unix`, `linux`, `tty`

Sun Feb 05 15:56:39 2017 +0100

## [Ad-hoc Polymorphism in F# (how to survive without Type Classes)](http://withouttheloop.com/articles/2014-10-21-fsharp-adhoc-polymorphism/)

> A recurring source of confusion for me when reading about and writing F# has been ad-hoc polymorphism, and it seems that I am not the only one:
>> &ldquo;F# does not have support for type-classes, or for multi-methods, or anything in between and while you can do certain tricks to achieve such an effect, like passing around a global virtual table, truth is F#&rsquo;s ad-hoc polymorphic capabilities really suck.&rdquo;

Tags: `f#`, `polymorphism`

Thu Feb 02 08:00:49 2017 +0100

## [Amazon Web Services in Plain English](https://www.expeditedssl.com/aws-in-plain-english)
 
> Hey, have you heard of the new AWS services: ContainerCache, ElastiCast and QR72? Of course not, I just made those up.

> But with 50 plus opaquely named services, we decided that enough was enough and that some plain english descriptions were needed.

Tags: `aws`

Mon Jan 30 11:16:38 2017 +0100

## [Low latency, large working set, and GHC’s garbage collector: pick two of three](https://blog.pusher.com/latency-working-set-ghc-gc-pick-two/)

> Pusher makes it easy for developers to reliably deliver data at scale. A few features we are working on required a rewrite of our internal message bus, but we knew anything we build has to perform as reliably as the existing platform. Our chosen language for this job was Haskell, compiled with GHC. Haskell, unusually obsessed with correctness, was a good choice for our focus on reliability. GHC was a good choice as a compiler with a reputation for good performance. But our performance tests showed that our new implementation had performance problems. It suffered from high worst-case latency: the time between sending and receiving a message could be in the hundreds of milliseconds.

> This blog post documents our investigation of these latency problems. Our findings have some implications for designing similar systems using GHC.

Tags: `gc`, `haskell`

Wed Jan 18 10:11:51 2017 +0100

## [How do I see what the JIT compiled, anyway?](http://mikedimmick.blogspot.ch/2008/03/how-do-i-see-what-jit-compiled-anyway.html)

> You use the SOS debugger extension's `!U` command.

Tags: `jit`, `asm`, `debugging`

Wed Jan 11 17:02:17 2017 +0100

## [Samples for Parallel Programming with the .NET Framework](https://code.msdn.microsoft.com/Samples-for-Parallel-b4b76364)

> This project provides samples and extensions for the parallel programming support in the .NET Framework.

See also [Parallel Extensions Extras NuGet package](https://www.nuget.org/packages/MSFT.ParallelExtensionsExtras/).

Tags: `tpl`, `parallel`, `concurrency`, `plinq`, `sample`

Thu Dec 15 18:43:13 2016 +0100

## [The Myth of the Full-stack Developer](http://andyshora.com/full-stack-developers.html)

> - &ldquo;Full-stack.&rdquo;
> - Full-stack used to mean less layers.
> - Identifying mastery
> - How skilled are you in each discipline?
> - The skill of acquiring new skills
> - Why I'm not a full-stack developer
> - Some people are willing to have a go at everything
> - The employability of a true full-stack developer: HIGH.
> - Please harass me in the comments

Tags: `opinion`

Thu Dec 15 09:56:02 2016 +0100

## [Portable PDB](https://github.com/dotnet/core/blob/v1.1.0-preview1/Documentation/diagnostics/portable_pdb.md)

> .NET Core introduces a new symbol file (PDB) format - portable PDBs. Unlike traditional PDBs which are Windows-only, portable PDBs can be created and read on all platforms.

Tags: `debugging`, `pdb`

Thu Dec 15 09:53:42 2016 +0100

## [Advanced Bash-Scripting Guide](http://www.tldp.org/LDP/abs/html/index.html)

> This tutorial assumes no previous knowledge of scripting or programming, yet progresses rapidly toward an intermediate/advanced level of instruction…all the while sneaking in little nuggets of UNIX&reg; wisdom and lore. It serves as a textbook, a manual for self-study, and as a reference and source of knowledge on shell scripting techniques. The exercises and heavily-commented examples invite active reader participation, under the premise that the only way to really learn scripting is to write scripts.

Tags: `bash`, `book`

Thu Dec 15 08:24:55 2016 +0100

## [How do I determine the location of my script? I want to read some config files from the same place.](http://mywiki.wooledge.org/BashFAQ/028)

> There are two prime reasons why this issue comes up: either you want to externalize data or configuration of your script and need a way to find these external resources, or your script is intended to act upon a bundle of some sort (eg. a build script), and needs to find the resources to act upon. 

> It is important to realize that in the general case, this problem has no solution. Any approach you might have heard of, and any approach that will be detailed below, has flaws and will only work in specific cases. First and foremost, try to avoid the problem entirely by not depending on the location of your script! 

Tags: `bash`

Thu Dec 15 08:22:20 2016 +0100

## [Implementing, and Understanding Type Classes](http://okmij.org/ftp/Computation/typeclass.html)

> Computational abstractions&mdash;higher-order functions, continuations, modules, processes, automatic memory management&mdash;have made programs much faster to write, easier to show correct and to reuse. And yet there is, often subconscious, resistance to abstractions: they appear ritualistic, formal&mdash;too abstract. One gets the feeling of getting lost. To overcome the mistrust for an abstraction it may help to look at its realization, to see what is being abstracted away. The awareness of low-level implementation details brings the appreciation of an abstraction and the intuitive explanation for it.

Tags: `haskell`, `ocaml`

Mon Dec 12 08:40:08 2016 +0100

## [Asynchronous Programming with the Reactive Framework and the Task Parallel Library&mdash;Part 3](http://bvanderveen.com/a/async-with-rx-and-the-tpl-part-3)

> Both the Reactive Framework and the Task Parallel Library define their own concept of a scheduler. A scheduler is like a gatekeeper to the CPU. Schedulers expose a method which allows outside code to provide a piece of work which should be performed. In many scheduler implementations, the piece of work is put into a queue, and the scheduler performs the work at some point in the future. The thread on which the work is performed and when is decided by the scheduler, and is important to consider if you're writing a program with a user interface, or if you're writing a server which manages special worker threads.

Tags: `tpl`, `rx`, `threading`

Fri Dec 02 11:47:03 2016 +0100

## [UTF-8 Everywhere (Manifesto)](http://utf8everywhere.org/)

> Our goal is to promote usage and support of the UTF-8 encoding and to convince that it should be the default choice of encoding for storing text strings in memory or on disk, for communication and all other uses. We believe that our approach improves performance, reduces complexity of software and helps prevent many Unicode-related bugs. We suggest that other encodings of Unicode (or text, in general) belong to rare edge-cases of optimization and should be avoided by mainstream users.

Tags: `text`, `unicode`

Mon Nov 07 09:43:08 2016 +0100

## [You're Using HttpClient Wrong and it is Destabilizing Your Software](http://aspnetmonsters.com/2016/08/2016-08-27-httpclientwrong/) ##

> I've been using `HttpClient` wrong for years and it finally came back to bite me. My site was unstable and my clients furious, with a simple fix performance improved greatly and the instability disapeared.

Tags: `http`, `.net`

Wed Oct 26 12:07:08 2016 +0200

## [Lesser known Git commands](https://hackernoon.com/lesser-known-git-commands-151a1918a60#.y5flrkwnw)

> Git has a strong commitment to backwards compatibility: many powerful features are hidden behind options rather than exposed as default behaviour. Fortunately Git also supports _aliases_, so you can create your own commands that do all manner of Git magic. Here’s a selection of the more useful (or at least entertaining) aliases defined in my `.gitconfig`.

Tags: `git`

Fri Oct 07 23:54:02 2016 +0200

## [Understanding LINQ to Objects (7) Interactive Extensions (Ix)](https://weblogs.asp.net/dixin/understanding-linq-to-objects-7-interactive-extensions-ix)

> Besides those built-in query methods (aka standard query operators) provided by `System.Linq.Enumerable`, Microsoft also offer another set of query methods through a library called [Interactive Extensions (Ix)](https://github.com/Reactive-Extensions/Rx.NET). The library can be [installed from nuget](https://www.nuget.org/packages/Ix-Main/)…There is no document for this library provided from Microsoft, except the library’s XML comments. These query methods will be explained by either examples and/or their implementation, whichever can be more intuitive.

Tags: `linq`

Wed Oct 05 08:28:43 2016 +0200

## [Classes for the Masses (Extended Abstract)](http://www.mlworkshop.org/2016-7.pdf)

> Type classes are an immensely popular and productive feature of Haskell. They have since been adopted in, and adapted to, numerous other languages, including theorem provers. We show that type classes have a natural and efficient representation in .NET that paves the way for the extension of F#, C# and other .NET languages with type classes. Our encoding is type preserving and promises easy and safe cross-language inter-operation. We have extended the open source C# compiler and language service, Roslyn, with pervasive support for type classes and have prototyped a more minimalist design for F#.

Tags: `c#`, `f#`, `haskell`

Sun Sep 25 10:51:02 2016 +0200

## [Singleton HttpClient? Beware of this serious behaviour and how to fix it](http://byterot.blogspot.co.uk/2016/07/singleton-httpclient-dns.html)

> Using singleton `HttpClient` results in your instance not to honour DNS changes which can have serious implications. The solution is to set the `ConnectionLeaseTimeout` of the `ServicePoint` object for the endpoint.

Tags: `.net`, `http`

Tue Aug 16 13:37:23 2016 +0200

## [Google’s QUIC protocol: moving the web from TCP to UDP](https://ma.ttias.be/googles-quic-protocol-moving-web-tcp-udp/)

> The QUIC protocol (Quick UDP Internet Connections) is an entirely new protocol for the web developed on top of UDP instead of TCP.

> Some are even (jokingly) calling it [TCP/2](https://daniel.haxx.se/blog/2016/07/27/workshop-day-two/).

Tags: `www`, `network`, `tcp`, `udp`, `unread`

Tue Aug 16 13:33:41 2016 +0200

## [Return Any (Task-Like) Type From An Async Method](http://blog.i3arnon.com/2016/07/25/arbitrary-async-returns/)

> Since async-await was added to C# 5.0 you could `await` any custom awaitable type as long as it follows a specific pattern: has a `GetAwaiter` method that returns an awaiter that in turn has `IsCompleted`, `OnCompleted` and `GetResult` (more on it [here](http://stackoverflow.com/a/28236920/885318)). But the language is stricter when it comes to the return type of an async method. You can only return 3 types from an async method: `void`, `Task` and `Task<T>`.

> These compiler rules[ were recently expanded](https://github.com/dotnet/roslyn/pull/12518) to also allow returning any custom type from an async method as long as it follows a specific pattern.

Tags: `c#`, `tpl`, `async`

Mon Aug 08 13:52:52 2016 +0200

## [The RAppArmor Package: Enforcing Security Policies in R Using Dynamic Sandboxing on Linux](https://www.jstatsoft.org/article/view/v055i07)

> 	The increasing availability of cloud computing and scientific super computers brings great potential for making R accessible through public or shared resources. This allows us to efficiently run code requiring lots of cycles and memory, or embed R functionality into, e.g., systems and web services. However some important security concerns need to be addressed before this can be put in production. The prime use case in the design of R has always been a single statistician running R on the local machine through the interactive console. Therefore the execution environment of R is entirely unrestricted, which could result in malicious behavior or excessive use of hardware resources in a shared environment. Properly securing an R process turns out to be a complex problem. We describe various approaches and illustrate potential issues using some of our personal experiences in hosting public web services. Finally we introduce the RAppArmor package: a Linux based reference implementation for dynamic sandboxing in R on the level of the operating system.

Tags: `r`, `security`

Wed Jul 06 11:32:21 2016 +0200

## [ConvertFrom-String: Example-based text parsing](https://blogs.msdn.microsoft.com/powershell/2014/10/31/convertfrom-string-example-based-text-parsing/)

> `ConvertFrom-String` lets you parse a file by providing a template that contains examples of the desired output data rather than by writing a (potentially complex) script.

Tags: `powershell`

Wed Jul 06 11:23:13 2016 +0200

## [How the dotnet CLI tooling runs your code](http://mattwarren.org/2016/07/04/How-the-dotnet-CLI-tooling-runs-your-code/)

> …It’s the `dotnet` CLI (Command Line Interface) tooling that is the focus of this post and more specifically how it actually runs your code

Tags: `dotnet`, `.net`

Tue Jul 05 22:49:46 2016 +0200

## [Date & Time Formats on the Web](https://www.hackcraft.net/web/datetime/)

> There are several different formats used in different places in the technologies of the World Wide Web to represent dates, times and date/time combinations (hereafter collectively referred to as “datetimes” unless a distinction has to be made). This document presents a survey of the most significant, details which formats are mandated by the key technologies of the web, and offers advice for deciding what formats you should use in your own web applications.

Tags: `www`

Sat Jun 25 11:37:42 2016 +0200

## [`LogonUser` + `LOGON32_LOGON_NEW_CREDENTIALS`, What is this flag used for?](https://blogs.msdn.microsoft.com/winsdk/2015/08/25/logonuser-logon32_logon_new_credentials-what-is-this-flag-used-for/)

> Impersonation becomes really important in a scenario where you are attempting to access a server which has no trust with your system since you can’t modify the permissions for the remote secured resource to allow your user access. In the past, this was done by providing alternate credentials to the `IPC$` share with `WNetAddConnection2()`. Using `IPC$` kind of stopped working in Windows VISTA for certain scenarios but a lot of developers today are still unaware of the changes. Due to the limitations and scenarios where it doesn’t work, a new flag was introduced in Windows VISTA for `LogonUser()`, `LOGON32_LOGON_NEW_CREDENTIALS` to address the weaknesses for this common scenario. 

Tags: `windows`, `admin`, `security`

Fri Jun 24 16:24:50 2016 +0200

## [Disabling User Account Control (UAC) on Windows Server](https://support.microsoft.com/en-gb/kb/2526083)

> Under certain constrained circumstances, disabling User Account Control (UAC) on Windows Server can be an acceptable and recommended practice. These circumstances occur only when all the following conditions are true:
>
> - Only administrators are allowed to log on to the Windows-based server interactively at the console or by using Remote Desktop Services.
> - Administrators log on to the Windows-based server only to perform legitimate system administrative functions on the server.
>
> If either of these conditions is not true, UAC should remain enabled.

Tags: `windows`, `admin`, `security`, `mskb`

Fri Jun 24 14:25:57 2016 +0200

## [TA-Lib : Technical Analysis Library](http://www.ta-lib.org/)

> Multi-Platform Tools for Market Analysis&hellip;
> - TA-Lib is widely used by trading software developers requiring to perform technical analysis of financial market data.
> - Includes 200 indicators such as ADX, MACD, RSI, Stochastic, Bollinger Bands etc&hellip; ([more info](http://www.ta-lib.org/function.html))
> - Candlestick pattern recognition
>
> Open-source API for C/C++, Java, Perl, Python and 100% Managed .NET

Tags: `ta`, `trading`, `library`

Thu Jun 23 11:38:16 2016 +0200

## [Regular Expression Matching Can Be Simple And Fast](https://swtch.com/~rsc/regexp/regexp1.html)

> This is a tale of two approaches to regular expression matching. One of them is in widespread use in the standard interpreters for many languages, including Perl. The other is used only in a few places, notably most implementations of awk and grep. The two approaches have wildly different performance characteristics

Tags: `regex`, `performance`, `unread`

Wed Jun 22 18:03:18 2016 +0200

## [.NET Framework 4.6 list of changes](https://dotnet2015.blob.core.windows.net/changes/dotnet46-changes.txt)

> .NET Framework 4.6 contains hundreds of bug fixes and improvements.
> This list details those changes, grouped by feature area.
> Each change includes our TFS bug numbers at the end of the line.
>
> See also: [diff_net452_net46.html](https://dotnet2015.blob.core.windows.net/changes/diff_net452_net46.html)

Tags: `.net`

Wed Jun 22 13:57:15 2016 +0200

## [What's New in the .NET Framework](https://msdn.microsoft.com/library/ms171868.aspx)

> This article summarizes key new features and improvements in the following versions of the .NET Framework:
>
> - .NET Framework 4.6.2 Preview
> - .NET Framework 4.6.1
> - .NET 2015 and .NET Framework 4.6
> - .NET Framework 4.5.2
> - .NET Framework 4.5.1
> - .NET Framework 4.5
> 
> This article does not provide comprehensive information about each new feature and is subject to change. 

Tags: `.net`

Wed Jun 22 13:49:07 2016 +0200

## [Console Virtual Terminal Sequences](https://msdn.microsoft.com/en-us/library/windows/desktop/mt638032(v=vs.85).aspx)

>  Virtual terminal sequences are control character sequences that can control cursor movement, color/font mode, and other operations.
>
> More information about terminal sequences can be found at [http://vt100.net](http://vt100.net).

Tags: `windows`

Wed Jun 22 09:18:53 2016 +0200

## [Handling AggregateExceptions](https://colinmackay.scot/2011/05/17/handling-aggregateexceptions/)

> AggregateException has a `Handle` method that takes a delegate of `Func<Exception, bool>` i.e. It takes an Exception as a parameter and returns a `bool`. The return value indicates whether the function handled the exception or not.

Tags: `.net`, `tpl`

Mon Jun 20 09:11:42 2016 +0200

## [Installing R packages without admin rights on MS Windows](http://www.magesblog.com/2012/04/installing-r-packages-without-admin.html)

> The other day I ended up in front of a Windows PC with R installed, but a locked down `"C:\Programme Files"` folder. That ment that R couldn't install any packages into the default directory `"C:\Programme Files\R\R-X.Y.Z\library"` (replace `R-X.Y.Z` with the version number of R installed). 
>
> Never-mind, there is an option for that, the libs argument in the install.packages function.

Tags: `windows`, `r`, `admin`

Fri Jun 17 10:50:26 2016 +0200

## [Running C# scripts and snippets in Visual Studio Code with scriptcs](http://www.strathweb.com/2015/11/running-c-scripts-and-snippets-in-visual-studio-code-with-scriptcs/)

> Visual Studio Code can also now be extended via plugins – and when that was announced, I thought why not make something for scriptcs? There already is a scriptcs plugin for Sublime Text and for Atom, so it only makes sense to have one for Visual Studio Code.

Tags: `c#`, `csx`, `vscode`

Fri Jun 17 10:48:58 2016 +0200

## [PowerShell One-Liners: Collections, Hashtables, Arrays and Strings](https://www.simple-talk.com/sysadmin/powershell/powershell-one-liners--collections,-hashtables,-arrays-and-strings/)

> The way to learn PowerShell is to browse and nibble, rather than to sit down to a formal five-course meal. In his continuing series on Powershell one-liners, Michael Sorens provides Fast Food for busy professionals who want results quickly and aren't too faddy. Part 3 has as its tasty confections  Collections, Hashtables, arrays and strings.

Tags: `powershell`

Thu Jun 16 11:33:53 2016 +0200

## [Publishing and Running ASP.NET Core Applications with IIS](https://weblog.west-wind.com/posts/2016/Jun/06/Publishing-and-Running-ASPNET-Core-Applications-with-IIS)

> When you build ASP.NET Core applications and you plan on running your applications on IIS you'll find that the way that Core applications work in IIS is radically different than in previous versions of ASP.NET.

> In this post I'll explain how ASP.NET Core runs in the context of IIS and how you can deploy your ASP.NET Core application to IIS.

Tags: `aspnet`, `aspnet-core-1.0`, `iis`

Fri Jun 10 13:05:28 2016 +0200

## [Writing Safe Shell Scripts](https://sipb.mit.edu/doc/safe-shell/  )

> Writing shell scripts leaves a lot of room to make mistakes, in ways that will cause your scripts to break on certain input, or (if some input is untrusted) open up security vulnerabilities. Here are some tips on how to make your shell scripts safer.

Tags: `posix`, `bash`, `shell`

Fri Mar 11 23:10:22 2016 +0100

## [FastRWeb: Fast Interactive Web Framework for Data Mining Using R](http://urbanek.info/research/pub/urbanek-iasc08.pdf)

> Our basic goal is to fully leverage R and yet to allow users to interact with the system without the need to resort to the R language. &hellip; In this talk we will describe the various parts of the system ranging from the fast-response infrastructre, AJAX tools for on-demand data loading to R facilities for intuitive creation of web objects, plots and interactive graphics. We will illustrate the use of the framework on several examples, including our implementation of a real-world mining tool used in practice for exploratory data analysis and data mining in very large databases.

Tags: `r`, `pdf`

Fri Mar 04 17:50:07 2016 +0100

## [Cleaning Up After Migrating From Hg to Git](http://christoph.ruegg.name/blog/cleaning-up-after-migrating-from-hg-to-git.html)

> There is a lot of guidance out there on how to migrate from Mercurial to Git, but they often leave you with a repository in a bad state. Even more so if it originally was a subversion repository, then migrated to Mercurial and now finally to Git.

Tags: `git`, `hg`

Tue Mar 01 18:42:10 2016 +0100

## [Further Down the Rabbit Hole: PowerShell Modules and Encapsulation](https://www.simple-talk.com/dotnet/.net-tools/further-down-the-rabbit-hole-powershell-modules-and-encapsulation/)

> Modules allow you to use standard libraries that extend PowerShell&rsquo;s functionality. They are easier to use than to create, but if you get the hang of creating them, your code will be more easily-maintained and re-usable. Let Michael Sorens once more be your guide through PowerShell&rsquo;s &lsquo;Alice in Wonderland&rsquo; world.

Tags: `psh`

Tue Feb 02 18:34:12 2016 +0100

## [SQL Server and Node.js, BFFs For Life](http://nerdventure.io/sql-server-and-node-js/)

> Recently, with the help of other reference implementations and documents, I was able to add NTLM authentication support to what I consider the best SQL lib for Node.js.

Tags: `node`, `mssql`, `ntlm`

Mon Feb 01 11:59:01 2016 +0100

## [ServiceWorker: Revolution of the Web Platform](https://ponyfoo.com/articles/serviceworker-revolution)

> While not the most amusingly named feature of the web platform, everything seems to point at ServiceWorker being the **most significant addition** to the web platform since the introduction of *AJAX* – over 10 years ago. Not to be confused with WebWorker (*used to offload intense compute operations onto another execution thread*), ServiceWorker allows you to intercept (*and hijack*) network requests originating from your site before they’re even dispatched. This article explores how it works, what it means and what it enables, and how you can implement it by following a case study.

Tags: `web`

Sun Jan 31 21:26:43 2016 +0100

## [Goodbye Child Actions, Hello View Components](http://www.davepaquette.com/archive/2016/01/02/goodbye-child-actions-hello-view-components.aspx)

> In previous versions of MVC, we used [Child Actions](http://haacked.com/archive/2009/11/18/aspnetmvc2-render-action.aspx/) to build reusable components / widgets that consisted of both Razor markup and some backend logic. The backend logic was implemented as a controller action and typically marked with a `[ChildActionOnly]` attribute. Child actions are extremely useful but as some have pointed out, it is easy to [shoot yourself in the foot](http://www.khalidabuhakmeh.com/obscure-bugs-asp-net-mvc-child-actions).

> **Child Actions do not exist in MVC 6.** Instead, we are encouraged to use the new View Component feature to support this use case. Conceptually, view components are a lot like child actions but they are a lighter weight and no longer involve the lifecycle and pipeline related to a controller. Before we get into the differences, let’s take a look at a simple example.

Tags: `aspnet`, `mvc` 

Fri Jan 29 13:40:23 2016 +0100

## [How to Take an Asp.Net MVC Web Site Down for Maintenance](https://www.simple-talk.com/dotnet/asp.net/how-to-take-an-asp.net-mvc-web-site-down-for-maintenance/)

> Keeping a customer facing web site up and performing well is a challenge, especially when you are still adding new features. While providing an &ldquo;always on&rdquo; experience for users is preferred there are times when it is easier to take the site &ldquo;down for maintenance&rdquo; and fix those things that are just too difficult and costly to do with the site up. Jon Smith describes his solution to a controlled &ldquo;down for maintenance&rdquo; approach for ASP.NET MVC sites.

Tags: `aspnet`, `mvc` 

Fri Jan 29 13:38:51 2016 +0100

## [Announcing NuGet 3.1 with Support for Universal Windows Platform](http://blog.nuget.org/20150729/Introducing-nuget-uwp.html)

> Today the NuGet team in collaboration with several other teams at Microsoft is happy to announce the release of a new version of the NuGet clients supporting the Universal Windows Platform and the new Portable class libraries. The NuGet tools are available through Tools&rarr;Extensions and Updates&rarr;Update tab in Visual Studio 2015 as well as from our [GitHub repository](https://github.com/nuget/home/releases). Additionally, we have released a new version of the NuGet command-line tool that you can download from [NuGet.org](http://dist.nuget.org/win-x86-commandline/v3.1.0-beta/nuget.exe).

> In this post, we will review the new capabilities that package authors can use and the process that windows programmers need to follow in order to use NuGet with their projects.

Tags: `nuget`, `uwp`

Fri Jan 29 13:36:01 2016 +0100

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

## [Recommendations and guidelines for the &ldquo;max degree of parallelism&rdquo; configuration option in SQL Server](https://support.microsoft.com/en-us/kb/2806535)

> The Microsoft SQL Server **max degree of parallelism** (`MAXDOP`) configuration option controls the number of processors that are used for the execution of a query in a parallel plan. This option determines the computing and thread resources that are used for the query plan operators that perform the work in parallel. Depending on whether SQL Server is set up on a symmetric multiprocessing (SMP) computer, a non-uniform memory access (NUMA) computer, or hyperthreading-enabled processors, you have to configure the **max degree of parallelism** option appropriately. This article discusses the general guidelines that you can use to configure the **max degree of parallelism** option for SQL Server when you use the `sp_configure` system stored procedure. 

Tags: `mssql`, `mskb`, `admin`

Fri Jan 29 13:16:34 2016 +0100
