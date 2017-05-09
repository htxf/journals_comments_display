# journals_comments_display
web端展示获取到的小木虫论坛中文期刊点评信息

在[这里](https://github.com/htxf/muchong_bbs_journals_comments_crawler)将想要的信息都存储到了一个json文件中。

想要的效果是，列出31个期刊的名字，点击某个期刊名，出现该期刊的基本信息和网友的评论。

刚学了学Vue，用Vue来写。根据[这篇教程](https://www.qcloud.com/community/article/430630001490779316?fromSource=gwzcw.60069.60069.60069)构建的目录。有pages、components，不用router。

index下有两个部分，期刊名和期刊具体信息。期刊名用v-for来写；期刊具体信息用v-show来决定显示与否，写在一个component中。
期刊具体信息下有两部分，一部分该期刊基本信息，另一部分是该期刊的所有网友评论。期刊基本信息只是简单的展示来自父组件的信息。所有网友的评论是另一个组件，用v-for来全部展示，其中的信息来自父组件的父组件……

最后build时由于只需要本地打开index.html就可用，查询资料将config目录下的index.js 中build里对应的assetsPublicPath字段改成了./就ok了。

将最终build的dist也压缩上传了。
