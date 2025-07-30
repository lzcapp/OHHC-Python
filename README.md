# OpenHappyHackingCalendar-Python
《编程日历》的Python实现版本，基于[OpenHappyHackingCalendar](https://github.com/Sneezry/OpenHappyHackingCalendar)项目改编，与原项目基本一致。

## 结果展示

HTML样式展示：

- [2022](https://github.lzc.app/OHHC-Python/Calendar-2022.html)
- [2023](https://github.lzc.app/OHHC-Python/Calendar-2023.html)
- [2024](https://github.lzc.app/OHHC-Python/Calendar-2024.html)
- [2025](https://github.lzc.app/OHHC-Python/Calendar-2025.html)
- [2026](https://github.lzc.app/OHHC-Python/Calendar-2026.html)

PDF样式展示：

- [2022](https://github.lzc.app/OHHC-Python/Calendar-2022.pdf)
- [2023](https://github.lzc.app/OHHC-Python/Calendar-2023.pdf)
- [2024](https://github.lzc.app/OHHC-Python/Calendar-2024.pdf)
- [2025](https://github.lzc.app/OHHC-Python/Calendar-2025.pdf)
- [2026](https://github.lzc.app/OHHC-Python/Calendar-2026.pdf)

## 环境依赖

Python 3 (Python 3.9.1)

本项目使用了以下几个Python第三方库（加粗者为需要另行安装）：

- `json`
- **`jsonpath`**
- **`lunar_python`** (一个阴历/阳历转换库：[lunar](http://6tail.cn/calendar/api.html#overview.html))
- `html`
- **`requests`**

在测试过程中发现：需要电脑安装`openssl`。

除此之外，因为项目需要爬取维基百科中对编程语言的介绍，所以需要可以访问维基百科。

如遇`Caused by SSLError`错误，是urllib3版本的问题，可以换用`1.25.11`或者其他低版本，在原环境中重装低版本`urllib3`：

```python
pip install urllib3==1.25.11
```

Prism库：[下载](https://prismjs.com/download#themes=prism&languages=markup+css+clike+javascript+abap+actionscript+ada+apacheconf+apl+applescript+arduino+asciidoc+aspnet+autohotkey+autoit+bash+basic+batch+bison+brainfuck+bro+c+csharp+cpp+coffeescript+crystal+css-extras+d+dart+diff+django+docker+eiffel+elixir+erlang+fsharp+flow+fortran+gherkin+git+glsl+go+graphql+groovy+haml+handlebars+haskell+haxe+http+icon+inform7+ini+j+java+jolie+json+julia+keyman+kotlin+latex+less+livescript+lolcode+lua+makefile+markdown+markup-templating+matlab+mel+mizar+monkey+n4js+nasm+nginx+nim+nix+nsis+objectivec+ocaml+opencl+oz+parigp+parser+pascal+perl+php+php-extras+powershell+processing+prolog+properties+protobuf+pug+puppet+pure+python+q+qore+r+jsx+reason+renpy+rest+rip+roboconf+ruby+rust+sas+sass+scss+scala+scheme+smalltalk+smarty+sql+stylus+swift+tcl+textile+twig+typescript+vbnet+verilog+vhdl+vim+wiki+xojo+yaml)

ASpace：

```shell
git submodule update --init --recursive
```

## 配置文件

在`config.json`中有以下参数可以配置：

- `year`：日历的年份
- `monthly`：是否在日历中显示单独的月份界面
- `punched`：日历是否打孔，效果很差:)
- `qr`：是否在日历中增加二维码

## 运行

下载程序 → 安装好环境 → 运行index.py

输出为`Calendar-[YYYY].html`，您可以用“打印”的方式将其转换为PDF格式文件。
