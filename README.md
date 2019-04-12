- scaffolds
        模版文件夹,当您新建文章时，Hexo 会根据 scaffold 来建立文件
        新建的markdown文件中默认填充的内容
- source
        资源文件夹是存放用户资源的地方
        。除 _posts 文件夹之外，开头命名为 _ (下划线)的文件 / 文件夹和隐藏的文件将会被忽略。Markdown 和 HTML 文件会被解析并放到 public 文件夹，而其他文件会被拷贝过去。
- hexo new [layout] <title>
        新建一篇文章。如果没有设置 layout 的话，默认使用 _config.yml 中的 default_layout 参数代替。如果标题包含空格的话，请使用引号括起来。
- hexo g 生成静态文件 hexo g -d 生成后立马部署 -w 监视文件变动
- hexo publish [layout] <filename> 发表草稿
- hexo server 启动服务器 
- hexo d 部署 之前需要生成静态文件
- hexo render <file1> [file2].... 渲染文件
- hexo clean 清楚缓存 清除缓存文件 (db.json) 和已生成的静态文件 (public)。
- hexo list 列出网站资料
- hexo version
- hexo --safe 在安全模式下，不会载入插件和脚本。当您在安装新插件遭遇问题时，可以尝试以安全模式重新执行。
- hexo --config custom.yml
        自定义配置文件的路径，执行后将不再使用 _config.yml。
- hexo --draft 显示 source/_drafts 文件夹中的草稿文章。
- hexo new draft "testDraft" 创建一篇新草稿。
- hexo new layout "testlayout"创建一篇新文章。