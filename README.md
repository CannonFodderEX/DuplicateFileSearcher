# DuplicateFileSearcher
Fuzzy compare file names to search for duplicate files.

Mainly designed and tested for Comic and Anime files. Can be used for other files.

The algorithm will reconize series number like 上巻|下巻|序章|前編|中編|後編|総集編|番外編|完結編|上|下 and digit.
Currently the algorithm removes tags encased in () and [] first, then do the compare. Plans to compare tags in the future.

require .net Framework 4.5.2 or above.

Support searching windows shared folder (SMB).

Use parallel computing for better CPU efficiency, tested search for duplicate in 22000 files, finished in about 100 seconds.

The program uses 2 open source project called SimMetrics and Shell, I forgot where the source come from since it was a long time ago.

The user settings are stored in "settings", so I was forced to add strong name for this program, to avoid the system create a seperate user.config for every compile.


通过模糊比较文件名查找重复的文件。

主要针对漫画和动画文件名设计和测试，也可以用于其他文件。

会区别上巻|下巻|序章|前編|中編|後編|総集編|番外編|完結編|上|下 和阿拉伯数字的系列编号。
目前的处理是去除文件名中()和[]包裹的tag再进行比较，未来考虑升级对tag的比较。

需要.net Framework 4.5.2或以上。

支持搜索windows共享文件夹(SMB)。

使用并行计算提高CPU使用率和搜索速度，实测22000个文件的比较大概需要1分40秒。

项目使用了SimMetrics和Shell两个开源包，因为时间久远已经不记得来源了。

由于用户设置保存在settings中，不得不加上强名称签名用于避免每次重新编译系统自动使用不同的user.config
