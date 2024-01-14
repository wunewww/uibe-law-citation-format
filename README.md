# uibe-citation-format

引注格式是按照[《对外经济贸易大学法学院学位论文脚注及参考文献体例（2021）》](http://law.uibe.edu.cn/jwjx/jwgg/ss/091c012043a64aff8e7ad1d64256d933.htm)中的内容修改的，做了些许改动。由于CSL本身功能存在一定限制，因此**并非**完全开箱即用。

## 使用前注意

- 请在MS Word中设置引注的语言：`Zotero > Document Preferences > Language > English (UK)`
- 所有中文引文的Language（语言）字段应当有值（可以填写任意值，推荐`zh-cn`），所有英语/外语的引文的Language（语言）字段**应当留空**。由于中文、英文有不同的引注格式，配置文件依赖该字段判断应当使用哪种格式。
- 如果不希望出现嵌套的"《》"，所有中文引文的title字段中的"《》"应当被更换为"<>"
- 所有不包括在格式手册内的引文，均套用网络资源模板（中/英文），这些引文的*URL*应当有值。

## 格式参考

如果没有某个字段，对应的前后缀也就没了。如果有出错的地方，请提issue。

### 中文引文

- Book
  - {authors}：《{title}》，{publisher}{year}年版，第{page}页。
  - 古籍也为本模板
    - 《{title}》。
  - 译著也为本模板
    - {authors}：《{title}》，{traslators}译，{publisher}{year}年版，第{page}页。
- Journal Article
  - {authors}：《{title}》，载《{publication}》{year}年第{issue}期，第{page}页。
- Conference Paper
  - 本模板对应格式手册中的集刊、论文集
  - {authors}：《{title}》，载{editors}主编：《{conference name}》（{year}），{pubulisher}{year}年版，第{page}页。
- Thesis
  - 对应学位论文
  - {authors}：《{title}》，{university}{year}年{type}论文，第{page}页。
- Web Page
  - {authors}：《{title}》，{URL}，{date}访问
- Newspaper Article
  - {authors}：《{title}》，载《{publication}》{date}，第{page}版。
