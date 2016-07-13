作者：Tavish Armstrong

It's commonplace to say that computer hardware is now so fast that most developers don't have to worry about performance.Infact,Douglas Crockford declined to write achapter for this book for that reason:
> If I ware to write a chapter,it would be about anti-performance:most effort spent in pursuit of performance is wasted.I don't think that is what you are looking for.

Donald Knuth made the same point thirty years age:
> We should forget about small efficiencies,say about 97% of the time: premature optimization is the root is all evil.

对于开发者而言不必担心计算机硬件的性能，因为它非常迅速。实际上Douglas Crockford谢绝了写这一章，原因如下：
> 如果我写了这章，这将是低效的，一些精力花费在追求性能上是浪费的。我不认为那是你们想要的。

Donald Knuth 在三年前持有类似的观点：
> 我们应当忽略一些小的性能，say about 97% of the time:过早地优化是所有罪恶的根源。

But betwwen mobile devices with limited power and memory,and data analysis projects that need to process terbytes,a growing number of developers do need to make their code faster,their data structures smaller, and their response times shorter.However,while hundreds of textbooks explain the basics of operating systems,networks,computer graphics,and databases,few(if any) explain how to find and fix things in real applications that are simply too damn slow.

移动设备的内存和电量是有限的，数据分析项目需要处理百万兆字节。越来越多的开发者需要他们的代码更快，数据结构更小，响应时间更短。虽然数百万的教科书解释操作系统，网络，计算机图形学以及数据库的基本基本知识，但很少有解释如何查找和修复实际应用中太慢的问题。

This collection of case studies is our attempt to fill that gap.Each chapter is written by real developers who hava had to make an existing system faster or who had to design something to be fast in the first place.They cover many different kinds of software and performance goals; what they have in common is a detailed understanding of what cctually happens when, and how the different parts of large applications fit together.Our hope is that book will-like its predecessor _The Architecture of Open Source Applications_ ——help you become a better developer by letting you look over these experts' shoulders.
—— Tavish Armstrong

这里收集的案例试图修复这些缺陷，每一章都是由真正的开发人员编写，他们必须使一个现存的系统更快，或者在设计中将速度放在首位。他们的共同点是详细的了解到究竟发生了什么。并且如何将一个较大的应用的不同部分组装到一起。我们希望这本书能够像之前的《The Architecture of Open Source Applications》一样，通过查看这些专家的肩膀帮助你成为更好的开发者。
—— Tavish Armstrong

## Contributors
* Tavish Armstrong (editorial): Tavish studies software engineering at Concordia University and hopes to graduate in the spring of 2014. His online home is http://tavisharmstrong.com.

* Michael Snoyman (Warp): Michael is the lead software engineer at FP Complete. He is the founder and lead developer of the Yesod Web Framework, which provides a means of creating robust, high-performance web applications. His formal studies include actuarial science, and he has previously worked in the US auto and homeowner insurance industry analyzing large data sets.

* Kazu Yamamoto (Warp): Kazu is a senior researcher of IIJ Innovation Institute. He has been working for open source software around 20 years. His products include Mew, KAME, Firemacs and mighty.

* Andreas Voellmy (Warp): Andreas is a PhD candidate in Computer Science at Yale University. Andreas uses Haskell in his research on software-defined networks and has published open source Haskell packages, such as nettle-openflow, for controlling routers using Haskell programs. Andreas also contributes to the GHC project and is a maintainer of GHC’s IO manager.

* Ilya Grigorik (Chrome): Ilya is a web performance engineer and developer advocate on the Make The Web Fast team at Google, where he spends his days and nights on making the web fast and driving adoption of performance best practices. You can find Ilya online on his blog at igvita.com and under @igrigorik on Twitter.

* Evan Martin (Ninja): Evan has been a programmer at Google for nine years. His background before that includes degrees in computer science and linguistics. He has hacked on many minor free software projects and a few major ones, including LiveJournal. His website is http://neugierig.org .

* Bryce Howard (Mobile Performance): Bryce is a software architect who obsesses about making things go fast. He has 15+ years in the industry, and has worked for a number of startups you’ve never heard of. He is currently taking a stab at this whole “writing” thing and authoring an introductory Amazon Web Services book for O’Reilly Associates.

* Kyle Huey (Memshrink): Kyle works at the Mozilla Corporation on the Gecko rendering engine that powers the Firefox web browser. He earned a Bachelor’s degree in mathematics from the University of Florida before moving to San Francisco. He blogs at blog.kylehuey.com .

* Clint Talbert (Talos): Clint has been involved in the Mozilla project for almost a decade, first as a volunteer and then as an employee. He currently leads the Automation and Tools team with a mandate to automate everything that can be automated, and a personal vendetta to eliminate idle cycles on any automation machine. You can follow his adventures in open source and writing at clinttalbert.com .

* Joel Maher (Talos): Joel has over 15 years of experience automating software. In the last 5 years at Mozilla, Joel has hacked the automation and tools at Mozilla to extend to mobile phones as well as taken ownership of Talos to expand tests, reliability and improve regression detection. While his automation is running, Joel likes to get outdoors and tackle new challenges in life. For more automation adventures, follow along at elvis314.wordpress.com .

* Audrey Tang (Ethercalc): A self-educated programmer and translator based in Taiwan, Audrey currently works at Socialtext with the job title “Untitled Page”, as well as at Apple on localization and release engineering. Audrey has previously designed and led the Pugs project, the first working Perl 6 implementation, and served in language design committees for Haskell, Perl 5, and Perl 6, with numerous contributions to CPAN and Hackage. Follow Audrey on Twitter at @audreyt.

* C. Titus Brown (Khmer): Titus has worked in evolutionary modeling, physical meteorology, developmental biology, genomics, and bioinformatics. He is now an Assistant Professor at Michigan State University, where he has expanded his interests into several new areas, including reproducibility and maintainability of scientific software. He is also a member of the Python Software Foundation, and blogs at http://ivory.idyll.org .

* Eric McDonald (Khmer): Eric McDonald is a developer of scientific software with an emphasis on high performance computing (HPC), the area in which he has worked much of the past 13 years. Having previously worked with several varieties of physicists, he now helps bioinformaticians. He holds a bachelor’s degree in Computer Science, Mathematics, and Physics. Eric has been a fan of FOSS since the mid-nineties.

* Douglas C. Schmidt (DaNCE): Dr. Douglas C. Schmidt is a Professor of Computer Science, Associate Chair of the Computer Science and Engineering program, and a Senior Researcher at the Institute at Software Integrated Systems, all at Vanderbilt University. Doug has published 10 books and more than 500 technical papers covering a wide range of software-related topics, and led the development of ACE, TAO, CIAO, and CoSMIC for the past two decades.

* Aniruddha Gokhale (DaNCE): Dr. Aniruddha S. Gokhale is an Associate Professor in the Department of Electrical Engineering and Computer Science, and Senior Research Scientist at the Institute for Software Integrated Systems (ISIS) both at Vanderbilt University. He has over 140 technical articles to his credit, and his current research focuses on developing novel solutions to emerging challenges in cloud computing and cyber physical systems.

* William R. Otte (DaNCE): Dr. William R. Otte is a Research Scientist at the Institute for Software Integrated Systems (ISIS) at Vanderbilt University. He has nearly a decade of experience developing open source middleware and modeling tools for distributed, real-time and embedded systems, working with both government and industrial partners including DARPA, NASA, Northrup Grumman and Lockheed-Martin. He has published numerous technical articles and reports describing these advances and has participated in the development of open standards for component middleware.

* Manik Surtani (Infinispan): Manik is a core R&D engineer at JBoss, Red Hat’s middleware division. He is the founder of the Infinispan project, and Platform Architect of the JBoss Data Grid. He is also the spec lead of JSR 347 (Data Grids for the Java Platform), and represents Red Hat on the Expert Group of JSR 107 (Temporary caching for Java). His interests lie in cloud and distributed computing, big data and NoSQL, autonomous systems and highly available computing.

* Arseny Kapoulkine (Pugixml): Arseny has spent his entire career programming graphics and low-level systems in video games, ranging from small niche titles to multi-platform AAA blockbusters such as FIFA Soccer. He enjoys making slow things fast and fast things even faster. He can be reached at mail@zeuxcg.org or on Twitter at @zeuxcg.

* Arjan Scherpenisse (Zotonic): Arjan is one of the main architects of Zotonic and manages to work on dozens of projects at the same time, mostly using Zotonic and Erlang. Arjan bridges the gap between back-end and front-end Erlang projects. Besides issues like scalability and performance, Arjan is often involved in creative projects. Arjan is a regular speaker at events.

* Marc Worrell (Zotonic): Marc is a respected member of the Erlang community and was the initiator of the Zotonic project. Marc spends his time consulting for large Erlang projects, the development of Zotonic and is the CTO of Maximonster, the builders of MaxClass and LearnStone.

## 贡献者

* Tavish Armstrong(编辑): 
Tavish在Concordia 大学攻读软件工程并希望在2014年春季毕业。他的博客是[http://tavisharmstrong.com](http://tavisharmstrong.com).

* Michael Snoyman(校对)：Michael是FP Complete的软件工程师。他创建并领导了Yesod Web 框架的开发。他提供了一种健壮的，高性能的Web应用程序。

* Andreas Voellmy(校对)：Andreas 是耶鲁大学计算机科学的博士候选人。Andreas uses Haskell in his research on software-defined networks and has pubished open source Haskell packages. 例如在nettle-openflow中就使用Haskell程序控制路由。Andreas也为GHC项目贡献过，并且维护了GHC的IO管理器。

* llya Gngonk(Chrome):llya 是一名Web性能工程师和开发人员，在google中倡导Web快速开发团队。



------------------

## 致谢

如果没有Amy Brown 和Greg Wilson的帮助这本书将不会与大家见面。他们请求我编辑这本书并相信我能够完成。我也非常感激Tony Arkles 在早期的撰稿中给予的帮助，同时感谢我们的技术复审。

* Colin Morris
* Corey Chivers
* Greg Wilson
* Julia Evans
* Kamal Marhubi
* Kim Moir
* Laurie MacDougall Sookraj
* Logan Smyth
* Monica Dinculescu
* Nikita Pchelin
* Natalie Black
* Pierre-Antoine Lafayette

编审和帮助者的团队确保了这本书得以出版：

* Adam Fletcher
* Amy Brown
* Danielle Pham
* Erik Habbinga
* Jeff Schwab
* Jessica McKellar
* Michael Baker
* Natalie Black
* Alexandra Phillips
* Peter Rood

Amy Brown,Bruno Kinoshita和Danielle Pham 应当得到特殊的感谢，他们在这本书的构建，图表，排版。
编写这本书是一个艰难的任务，但是当有朋友的鼓励是这将变得从容。自始至终Natalie Black, Julia Evans和 Kamal Marhubi保有耐心和热情。

## Contributing 

Dozens of volunteers worked hard to create this book.but there is still a lot to do. If you'd like to help, you can do sso by reporting errors,translating the content into other languages,or describing other open source systems.Please contact us at aosa@aosabook.org if you would like to get involved.

## 贡献

尽管有数十名志愿者努力的工作，但是仍然有很多需要做的，如果你乐于帮助，可以通过反馈错误来做这件事，翻译本书内容为其他的语言。或者描述其他的开源系统，如果你想参与请联系aosa@aosabook.org。

## Colophon

_In the print edition,this appears on the last page. Notes on fonts are specific to the print and PDF editions._
The cover font is Museo from the exljibris foundry by Jos Buivenga.The text font is TEXGyre Termes and the headingfont is TEXGyre Heros.both by Boguslaw Jackowski and Janusz M.Nowacki.The code font is Inconsolata by Raph Levien.

The front cover photo is of the former workings of the former workings of the turret clock of St.Stephen's Cathedral in Vienna.The working can now be seen in the Vienna Clock Museum.The picture was taken by Michelle Enemark.The cover was designed by Amy Brown.

The book was built with open source software(with the exception of the cover).Programs like LaTex,Pandoc,Python and Calibre(ebook-convert) were especially helpful.

## 后记

_在印刷版上,这一页将出现在最后一页。注意在印刷版和PDF上字体是特殊的_
封面的字体是exljibris foundry，由Jos Buivenga提供。正文字体是TEXGyre Termes，标题字体是TEXGyre Heros，两者来自于Boguslaw Jackowski 和Janusz M.Nowacki。代码字体是Inconsolata来自于Raph Levien。

封面图片是基于之前在维也纳Stephen的教堂街道的turret clock工作时的图片，可以在维也纳的Clock博物馆看到。这张图片是通过Michelle Enemark获得的，封面由Amy Brown设计。

这本书使用开源软件构建（封面除外）。例如LaTex，Pandoc,Python和Calibre起到了关键的帮助。
