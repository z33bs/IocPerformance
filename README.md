# Ioc Performance
[![Build Status](https://github.com/danielpalme/IocPerformance/workflows/Smoketest/badge.svg)](https://github.com/danielpalme/IocPerformance/workflows/Smoketest/badge.svg)

Source code of my performance comparison of the most popular .NET IoC containers:  
[www.palmmedia.de/Blog/2011/8/30/ioc-container-benchmark-performance-comparison](https://www.palmmedia.de/Blog/2011/8/30/ioc-container-benchmark-performance-comparison)

Author: Daniel Palme  
Blog: [www.palmmedia.de](https://www.palmmedia.de)  
Twitter: [@danielpalme](https://twitter.com/danielpalme)  

## Results
### Explantions
**First value**: Time of single-threaded execution in [ms]  
**Second value**: Time of multi-threaded execution in [ms]  
**_*_**: Benchmark was stopped after 1 minute and result is extrapolated.  
### Basic Features
|**Container**|**Singleton**|**Transient**|**Combined**|**Complex**|
|:------------|------------:|------------:|-----------:|----------:|
|**No**|41<br/>49|49<br/>59|69<br/>76|99<br/>103|
|**[abioc 0.8.0](https://github.com/JSkimming/abioc)**|26<br/>43|**33**<br/>**56**|**51**<br/>82|**67**<br/>**78**|
|**[Autofac 6.1.0](https://github.com/autofac/Autofac)**|702<br/>499|882<br/>597|2369<br/>1492|7249<br/>4391|
|**[Caliburn.Micro 1.5.2](https://github.com/Caliburn-Micro/Caliburn.Micro)**|465<br/>270|533<br/>322|1583<br/>906|7403<br/>3712|
|**[Catel 5.12.11](http://www.catelproject.com)**|232<br/>282|3883<br/>4263|9072<br/>9828|21140<br/>22450|
|**[DryIoc 4.7.2](https://github.com/dadhi/DryIoc)**|61<br/>58|93<br/>79|93<br/>111|115<br/>115|
|**[DryIocZero 4.0.0](https://github.com/dadhi/DryIoc)**|110<br/>96|88<br/>89|98<br/>105|220<br/>169|
|**[Dynamo 3.0.2](http://martinf.github.io/Dynamo.IoC)**|95<br/>70|104<br/>86|207<br/>158|685<br/>381|
|**[Grace 7.2.0](https://github.com/ipjohnson/Grace)**|29<br/>**39**|42<br/>59|58<br/>81|77<br/>82|
|**[Lamar 5.0.0](https://jasperfx.github.io/lamar/)**|70<br/>70|163<br/>87|100<br/>115|129<br/>118|
|**[LightInject 6.4.0](https://github.com/seesharper/LightInject)**|46<br/>47|45<br/>57|88<br/>99|153<br/>143|
|**[Maestro 3.6.5](https://github.com/JonasSamuelsson/Maestro)**|410<br/>312|404<br/>307|652<br/>477|1547<br/>1204|
|**[Mef 4.0.0.0](https://github.com/MicrosoftArchive/mef)**|22679<br/>11820|37640<br/>25052|57462<br/>68730*|112712*<br/>131716*|
|**[Mef2 5.0.0.0](https://blogs.msdn.com/b/bclteam/p/composition.aspx)**|259<br/>178|252<br/>192|355<br/>263|657<br/>444|
|**[MicroResolver 2.3.5](https://github.com/neuecc/MicroResolver)**|25<br/>**39**|34<br/>59|55<br/>**77**|92<br/>89|
|**[Microsoft Extensions DependencyInjection 5.0.1](https://github.com/aspnet/Extensions)**|73<br/>67|103<br/>86|126<br/>115|146<br/>120|
|**[Microsoft.VisualStudio.Composition 16.4.11](https://blogs.msdn.com/b/bclteam/p/composition.aspx)**|9074<br/>4916|13891<br/>9399|19760<br/>14962|57910<br/>51972|
|**[Mugen MVVM Toolkit 6.5.0](https://github.com/MugenMvvmToolkit/MugenMvvmToolkit)**|102<br/>138|409<br/>715|2052<br/>2590|9348<br/>11352|
|**[MvvmCross 7.1.2](https://github.com/MvvmCross/MvvmCross)**|240<br/>281|1470<br/>1585|3607<br/>4008|10040<br/>11160|
|**[Ninject 3.3.4](http://ninject.org)**|3473<br/>2563|8686<br/>6969|23529<br/>17635|63579*<br/>49285|
|**[Rezolver 2.1.0](http://rezolver.co.uk)**|121<br/>100|137<br/>126|194<br/>171|328<br/>238|
|**[SimpleInjector 5.2.1](https://simpleinjector.org)**|58<br/>66|78<br/>84|124<br/>114|152<br/>116|
|**[Singularity 0.18.0](https://github.com/Barsonax/Singularity)**|**24**<br/>**39**|39<br/>59|66<br/>82|76<br/>84|
|**[Spring.NET 2.0.1](http://www.springframework.net/)**|950<br/>987|9711<br/>11447|26941<br/>23873|74745*<br/>57777|
|**[Stashbox 3.5.0](https://github.com/z4kn4fein/stashbox)**|35<br/>42|63<br/>69|69<br/>96|86<br/>86|
|**[StructureMap 4.7.1](http://structuremap.net/structuremap)**|1121<br/>717|1281<br/>856|3410<br/>2166|8312<br/>6052|
|**[Unity 5.11.10](https://github.com/unitycontainer/unity)**|216<br/>148|1443<br/>835|3326<br/>1995|9503<br/>4739|
|**[Windsor 5.1.1](http://castleproject.org)**|461<br/>333|1839<br/>1127|8062<br/>5972|19313<br/>13001|
|**[ZenIoc 1.0.1](https://github.com/zenmvvm/ZenIoc)**|306<br/>198|267<br/>188|674<br/>440|1809<br/>1103|
|**[Zenject 8.0.0](https://github.com/modesttree/Zenject)**|479<br/>448|1370<br/>1070|3689<br/>3065|11142<br/>10106|
### Advanced Features
|**Container**|**Property**|**Generics**|**IEnumerable**|**Conditional**|**Child Container**|**Asp Net Core**|**Interception With Proxy**|
|:------------|-----------:|-----------:|--------------:|--------------:|------------------:|---------------:|--------------------------:|
|**No**|186<br/>134|70<br/>75|193<br/>176|53<br/>63|644<br/>596|<br/>|469<br/>438|
|**[abioc 0.8.0](https://github.com/JSkimming/abioc)**|<br/>|<br/>|799<br/>506|<br/>|<br/>|<br/>|<br/>|
|**[Autofac 6.1.0](https://github.com/autofac/Autofac)**|7216<br/>4433|2119<br/>1390|7780<br/>4789|1766<br/>1138|95939*<br/>83541*|40409<br/>35736|22350<br/>12007|
|**[Caliburn.Micro 1.5.2](https://github.com/Caliburn-Micro/Caliburn.Micro)**|9157<br/>4733|<br/>|5965<br/>3393|<br/>|<br/>|<br/>|<br/>|
|**[Catel 5.12.11](http://www.catelproject.com)**|<br/>|8668<br/>9519|<br/>|<br/>|<br/>|<br/>|3819<br/>4186|
|**[DryIoc 4.7.2](https://github.com/dadhi/DryIoc)**|161<br/>180|221<br/>143|678<br/>670|257<br/>214|<br/>|2979<br/>1308|1283<br/>1451|
|**[DryIocZero 4.0.0](https://github.com/dadhi/DryIoc)**|294<br/>205|92<br/>92|302<br/>229|380<br/>270|<br/>|<br/>|<br/>|
|**[Dynamo 3.0.2](http://martinf.github.io/Dynamo.IoC)**|828<br/>455|<br/>|<br/>|<br/>|<br/>|<br/>|<br/>|
|**[Grace 7.2.0](https://github.com/ipjohnson/Grace)**|134<br/>113|55<br/>78|296<br/>242|**58**<br/>83|61817*<br/>37329|759<br/>815|1287<br/>764|
|**[Lamar 5.0.0](https://jasperfx.github.io/lamar/)**|91<br/>96|98<br/>112|558<br/>385|<br/>|<br/>|4685<br/>4364|<br/>|
|**[LightInject 6.4.0](https://github.com/seesharper/LightInject)**|185<br/>150|61<br/>77|294<br/>239|384<br/>285|<br/>|2268<br/>1643|1548<br/>1062|
|**[Maestro 3.6.5](https://github.com/JonasSamuelsson/Maestro)**|4824<br/>3118|472<br/>354|1400<br/>942|<br/>|<br/>|12236<br/>10304|6134<br/>4361|
|**[Mef 4.0.0.0](https://github.com/MicrosoftArchive/mef)**|124500*<br/>133833*|137086*<br/>114221*|97231*<br/>100896*|<br/>|<br/>|<br/>|<br/>|
|**[Mef2 5.0.0.0](https://blogs.msdn.com/b/bclteam/p/composition.aspx)**|1431<br/>1012|290<br/>226|1343<br/>895|<br/>|<br/>|<br/>|<br/>|
|**[MicroResolver 2.3.5](https://github.com/neuecc/MicroResolver)**|**39**<br/>**62**|<br/>|262<br/>195|<br/>|<br/>|<br/>|<br/>|
|**[Microsoft Extensions DependencyInjection 5.0.1](https://github.com/aspnet/Extensions)**|<br/>|121<br/>100|359<br/>254|<br/>|<br/>|3934<br/>2551|<br/>|
|**[Microsoft.VisualStudio.Composition 16.4.11](https://blogs.msdn.com/b/bclteam/p/composition.aspx)**|44285<br/>31830|<br/>|42023<br/>35658|<br/>|<br/>|<br/>|<br/>|
|**[Mugen MVVM Toolkit 6.5.0](https://github.com/MugenMvvmToolkit/MugenMvvmToolkit)**|436<br/>705|<br/>|9749<br/>7094|<br/>|**4370**<br/>**3103**|<br/>|<br/>|
|**[MvvmCross 7.1.2](https://github.com/MvvmCross/MvvmCross)**|1448<br/>1642|7519<br/>8328|<br/>|<br/>|5508<br/>3588|<br/>|<br/>|
|**[Ninject 3.3.4](http://ninject.org)**|62765*<br/>47908|24256<br/>15895|64193*<br/>49074|19294<br/>12954|73303000*<br/>50234113*|<br/>|20215<br/>15029|
|**[Rezolver 2.1.0](http://rezolver.co.uk)**|520<br/>385|183<br/>145|669<br/>408|<br/>|9589857*<br/>5697265*|86587*<br/>56374|<br/>|
|**[SimpleInjector 5.2.1](https://simpleinjector.org)**|271<br/>202|90<br/>95|634<br/>415|109<br/>92|<br/>|<br/>|5457<br/>3398|
|**[Singularity 0.18.0](https://github.com/Barsonax/Singularity)**|<br/>|**54**<br/>80|**241**<br/>**193**|<br/>|<br/>|**631**<br/>**652**|<br/>|
|**[Spring.NET 2.0.1](http://www.springframework.net/)**|52419<br/>51992|<br/>|<br/>|<br/>|<br/>|<br/>|43647<br/>43419|
|**[Stashbox 3.5.0](https://github.com/z4kn4fein/stashbox)**|123<br/>117|66<br/>**73**|278<br/>213|62<br/>**70**|336256*<br/>224444*|1461<br/>1088|**835**<br/>**562**|
|**[StructureMap 4.7.1](http://structuremap.net/structuremap)**|8697<br/>5284|2271<br/>1460|8399<br/>5170|<br/>|3215578*<br/>1887211*|65269*<br/>41725|7859<br/>4464|
|**[Unity 5.11.10](https://github.com/unitycontainer/unity)**|9045<br/>5814|9842<br/>6443|17755<br/>12048|3547<br/>2046|147355*<br/>74313*|61350*<br/>39009|56226<br/>31096|
|**[Windsor 5.1.1](http://castleproject.org)**|40830<br/>22225|15542<br/>9318|19361<br/>10763|<br/>|242149*<br/>176823*|<br/>|18018<br/>8775|
|**[ZenIoc 1.0.1](https://github.com/zenmvvm/ZenIoc)**|264<br/>195|276<br/>209|704<br/>488|314<br/>222|602490*<br/>471765*|<br/>|<br/>|
|**[Zenject 8.0.0](https://github.com/modesttree/Zenject)**|15829<br/>13135|9021<br/>6513|17932<br/>12687|3082<br/>2428|22250<br/>18595|<br/>|<br/>|
### Prepare
|**Container**|**Prepare And Register**|**Prepare And Register And Simple Resolve**|
|:------------|-----------------------:|------------------------------------------:|
|**No**|2<br/>|2<br/>|
|**[abioc 0.8.0](https://github.com/JSkimming/abioc)**|6327<br/>|6556<br/>|
|**[Autofac 6.1.0](https://github.com/autofac/Autofac)**|651<br/>|682<br/>|
|**[Caliburn.Micro 1.5.2](https://github.com/Caliburn-Micro/Caliburn.Micro)**|55<br/>|56<br/>|
|**[Catel 5.12.11](http://www.catelproject.com)**|9916<br/>|9346<br/>|
|**[DryIoc 4.7.2](https://github.com/dadhi/DryIoc)**|101<br/>|85<br/>|
|**[DryIocZero 4.0.0](https://github.com/dadhi/DryIoc)**|**0**<br/>|**1**<br/>|
|**[Dynamo 3.0.2](http://martinf.github.io/Dynamo.IoC)**|16240<br/>|16527<br/>|
|**[Grace 7.2.0](https://github.com/ipjohnson/Grace)**|234<br/>|1340<br/>|
|**[Lamar 5.0.0](https://jasperfx.github.io/lamar/)**|2285<br/>|2849<br/>|
|**[LightInject 6.4.0](https://github.com/seesharper/LightInject)**|131<br/>|1686<br/>|
|**[Maestro 3.6.5](https://github.com/JonasSamuelsson/Maestro)**|149<br/>|162<br/>|
|**[Mef 4.0.0.0](https://github.com/MicrosoftArchive/mef)**|17<br/>|2299<br/>|
|**[Mef2 5.0.0.0](https://blogs.msdn.com/b/bclteam/p/composition.aspx)**|4715<br/>|6984<br/>|
|**[MicroResolver 2.3.5](https://github.com/neuecc/MicroResolver)**|27322<br/>|67518<br/>|
|**[Microsoft Extensions DependencyInjection 5.0.1](https://github.com/aspnet/Extensions)**|27<br/>|35<br/>|
|**[Microsoft.VisualStudio.Composition 16.4.11](https://blogs.msdn.com/b/bclteam/p/composition.aspx)**|7904<br/>|8540<br/>|
|**[Mugen MVVM Toolkit 6.5.0](https://github.com/MugenMvvmToolkit/MugenMvvmToolkit)**|15<br/>|19<br/>|
|**[MvvmCross 7.1.2](https://github.com/MvvmCross/MvvmCross)**|11<br/>|16<br/>|
|**[Ninject 3.3.4](http://ninject.org)**|130706*<br/>|126470*<br/>|
|**[Rezolver 2.1.0](http://rezolver.co.uk)**|20835<br/>|27706<br/>|
|**[SimpleInjector 5.2.1](https://simpleinjector.org)**|735<br/>|3327<br/>|
|**[Singularity 0.18.0](https://github.com/Barsonax/Singularity)**|314<br/>|874<br/>|
|**[Spring.NET 2.0.1](http://www.springframework.net/)**|25014<br/>|24884<br/>|
|**[Stashbox 3.5.0](https://github.com/z4kn4fein/stashbox)**|66<br/>|582<br/>|
|**[StructureMap 4.7.1](http://structuremap.net/structuremap)**|1325<br/>|7389<br/>|
|**[Unity 5.11.10](https://github.com/unitycontainer/unity)**|122<br/>|287<br/>|
|**[Windsor 5.1.1](http://castleproject.org)**|2949<br/>|3445<br/>|
|**[ZenIoc 1.0.1](https://github.com/zenmvvm/ZenIoc)**|77<br/>|964<br/>|
|**[Zenject 8.0.0](https://github.com/modesttree/Zenject)**|199<br/>|201<br/>|
### Charts
![Basic features](https://www.palmmedia.de/blogimages/5225c515-2f25-498f-84fe-6c6e931d2042.png)
![Advanced features](https://www.palmmedia.de/blogimages/e0401485-20c6-462e-b5d4-c9cf854e6bee.png)
![Prepare](https://www.palmmedia.de/blogimages/67b056a5-9da8-40b4-9ae6-0c838cdac180.png)
### Machine
The benchmark was executed on the following machine:  
**CPU**: Intel(R) Core(TM) i5-6260U CPU @ 1.80GHz  
**Memory**: 15,89GB
