# uibe-citation-format

引注格式是按照[《对外经济贸易大学法学院学位论文脚注及参考文献体例（2021）》](http://law.uibe.edu.cn/jwjx/jwgg/ss/091c012043a64aff8e7ad1d64256d933.htm)中的内容修改的，做了些许改动。由于CSL本身功能存在一定限制，因此**并非**完全开箱即用。

本配置可供多种文献管理软件使用，主要是zotero。

## 使用前注意

- 请在MS Word中设置引注的语言：`Zotero > Document Preferences > Language > English (UK)`
- 所有中文引文的Language（语言）字段应当有值（可以填写任意值，推荐`zh-cn`），所有英语/外语的引文的Language（语言）字段**应当留空**。由于中文、英文有不同的引注格式，配置文件依赖该字段判断应当使用哪种格式。
- 如果不希望出现嵌套的"《》"，所有中文引文的title字段中的"《》"应当被更换为"<>"
- 所有不包括在格式手册内的引文，均套用网络资源模板（中/英文），这些引文的*URL*应当有值。

另外，

- 根据体例要求，页码应当是**引文本身/参考内容**所在的页码，请注意插入引注时手动指定
- 文献体例要求 Bibliography 包括中文著作、中文论文、英文著作、英文论文，现在存在以下问题
  - 其他文献仍然会生成 Bibliography，但是会列在所有内容最后，显示为 Delete this please, this should not be included in Bibliography. 可以在更新后手动删除
  - Bibliography 会按照要求排序
  - Bibliography 不会按照要求生成“一、中文著作”等小标题

## 格式参考

如果没有某个字段，对应的前后缀也就没了。如果有出错的地方，请提[issue](https://github.com/wunewww/uibe-law-citation-format/issues)。

所有的时间格式都自带年月日。可以在zotero对应字段中填写zotero可以识别的任意格式。

注意：所有的{page}段均为插入引注时指定，与zotero软件中的{pages}和{# of pages}不同

### 中文引文

- Book
  - {authors}：《{title}》，{publisher}{year}年版，第{page}页。
  - 古籍也为本模板
    - 《{title}》。
  - 译著也为本模板
    - {authors}：《{title}》，{translators}译，{publisher}{year}年版，第{page}页。
- Journal Article
  - {authors}：《{title}》，载《{publication}》{year}年第{issue}期，第{page}页。
- Conference Paper
  - 本模板对应格式手册中的集刊、论文集
  - {authors}：《{title}》，载{editors}主编：《{conference name}》（{year}），{publisher}{year}年版，第{page}页。
- Thesis
  - 对应学位论文
  - {authors}：《{title}》，{university}{year}年{type}论文，第{page}页。
- Web Page
  - {authors}：《{title}》，{URL}，{accessed date}访问
- Newspaper Article
  - {authors}：《{title}》，载《{publication}》{date}，第{page}版。
- Dictionary Entry
  - 对应辞书
  - 《{dictionary title}》，{publisher}{year}年版，第{page}页。

### 英语引文

英语引文参考文献体例中要求不同的字号大小实在过于阴间，没有自动设置不同字号大小的功能

- Book
  - {AUTHORS}, {TITLE} {page} ({translators/editors}, {edition} {year}).
  - 版本号可能多少有点不同
- Journal Article
  - {authors}, *{title}*, {issue} {publication} {page}, ({page} {year}).
  - 网页上文本描述和举例格式不一样
- Conference Paper
  - 对应论文集
  - {authors}, *{title}*, *in* {pages} {CONFERENCE NAME} {page} ({editors} {year}).
- Newspaper
  - {authors}, {title}, {publication}, {date}, at {page}.
- Web Page
  - {authors}, *{title}*, {URL} (last visited {accessed date}).
  - 网页上下面说网站名称大写，但是网站中的格式里没有网站名称。
- Case
  - 经过多次尝试，合理的格式如下
  - {title}, {Docket Number}, {history}, {first page} ({author} {year}).
  - {docket number}中填写案号
  - {history} 中填写文书性质，如 "Appellate Body"
  - 如果需要，在{first page}中写段落，如"para.13"
  - 本格式可以涵盖网页中列举的所有例子
- Statute
  - 对应法律条款和宪法条款
  - {name of act}, {code} §§ {code number} ({year}).
  - 宪法条款只写{name of act}和{code number}即可，`§`会自动去掉一个

缩写和简写就自己写在对应字段中吧。

## 关于作者

wuniu <niuzhl@outlook.com>
