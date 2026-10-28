# 03 · 美式复古（Amekaji）资料摘录

> 抓取日期：2026-10-28（Asia/Shanghai）
> 只记录**真正抓到的原文**；抓不到的一律写「未取得」，不做推测填充。

---

## A. 已取得的 [物证]

### A1. Red Wing Classic Moc 875 —— 官网商品页（HTTP 200）

URL：`https://www.redwingshoes.com/mens/heritage/classic-moc/classic-moc-00875.html`

页面标题：`Men's Classic Moc 6-Inch Boot in Brown Leather 875`

正文可确认字段（页面原样）：
- 品名块：`Classic Moc®` / `Heritage #875` / `Current Price: $329.99`
- 副标题：`Men's 6-Inch Boot in Oro Legacy Leather`
- 徽标：`Made in USA`
- 颜色选项：`Oro`
- 视频说明原文：`This video has no audio. It depicts a model wearing Classic Moc® and showing different angles of the boot.`

**能从中推出什么（可直接用于风格包的硬事实）**
1. 高度：**6 英寸**（Men's 6-Inch Boot）
2. 皮革：**Oro Legacy**（官方色名，非通用「棕色」）
3. 产地：Made in USA
4. 价格：USD 329.99
5. 系列归属：Heritage（复古线，与 Work 线分开）
6. 名称里的 **Moc / Moc Toe** = 鞋头带 U 形缝线的「莫克头」

**未取得**：鞋楦宽度、鞋底材质描述、皮厚度、绱底工艺（沿条）。商品详情段落被页面截断。

### A2. Red Wing Heritage 分类页（HTTP 200）

URL：`https://www.redwingshoes.com/mens/heritage/classic-moc/?currency=USD`

筛选面板原文（证明官方把 Classic Moc 当「复古线」卖，且按皮种切分）：
- `Leather Type`：`Full Grain` / `Roughout`
- `Featured Leather Colors`：`Oro Legacy` / `Sandstone`
- `Price`：`$300-350` / `$350-400`
- `Built in USA`：`Made in USA`
- `Color`：`Brown` / `Black` / `Green` / `Blue`

**能推出的**：Heritage 线有 Roughout（反绒/磨砂皮）这一支，价格带 300–400 美元。

### A3. Levi's 官方档案文章（HTTP 200）

URL：`https://www.levi.com/US/en_US/blog/article/from-the-archives-501-born`
标题：`STEP INSIDE THE LEVI'S® ARCHIVES: A 501® FOR WOMEN IS BORN`（December 2021，分类 Community）

原文可引用句：
- `Since the introduction of the first pair of Lady Levi's® in 1930, wearing Levi's® has been a bold statement for independent women.`
- `But back in 1981 when the Women's 501® was first introduced, it was a cultural signal to women who wanted a story of their own.`
- `No more borrowing a pair of 501's® from your brother or father.`
- `The story of Lady Levi's® starts in the American West with practical, tough women.`
- `But the art of customizing blue jeans was born in the 1960s, with designers like Love Melody in NYC. She'd cut up pre-loved 501's®, add rhinestones, crystals and turn them into something sexy, audacious and personalized.`
- `Like precious memories saved in a time capsule, 40 years later people had hung onto those pieces.`

**能推出的**：501 的时间轴物证 —— Lady Levi's 1930 年首次推出，Women's 501 1981 年推出，牛仔裤自定义改制的文化起点在 1960 年代。**注意：这是女装的档案线**，男装 501 的原始年份（1873 / 1890 等）本页未给。

### A4. Levi's 官网导航与分类结构（HTTP 200，levi.pt 英文站）

URL：`https://levi.pt/en/product/501-original-fit-jeans-00501-0162`

导航栏原始分类项（证明官方对 501 的品类归属）：
- `Styles We Love` → `501® Original Jeans` 指向 `/products/gender/men/category/jeans/fit-number/501®/fit/Straight`
- 牛仔裤版型分类：`Straight Jeans` / `Loose & Baggy Jeans` / `Slim Jeans` / `Skinny Jeans` / `Tapered Jeans`
- 其他系列：`502™ Taper` / `511™ Slim` / `555™ Relaxed Straight` / `578™ Baggy`

**能推出的 [物证]**：**501 在官方分类里属于 Straight（直筒）**；502 属 Taper（锥）、511 属 Slim（修身）、555 属 Relaxed Straight、578 属 Baggy。
**未取得**：501 的门襟、腰位、裤长、缩水率等正文描述 —— 该页正文被导航结构淹没，条目详情未渲染成文本。

### A5. Levi's 首页与菜单（HTTP 200）
- 复古子线存在且可购买：`Levi's® Vintage Clothing`、`Levi's® Made In Japan`、`Levi's® Blue Tab™`
- 经典品类命名仍是 `Truckers & Sherpas`（对应中文圈说的「牛仔夹克 / Trucker Jacket」）

---

## B. 抓取失败清单（如实记录）

| 目标 | URL | 结果 |
|---|---|---|
| Levi's 美国站 501 商品页 | `https://www.levi.com/US/en_US/clothing/men/jeans/501-original-fit-jeans/p/005012583` | **HTTP 403 Access Denied**（Akamai edgesuite 拦截） |
| Levi's 美国站 501（另一 SKU） | `.../p/005013312` | **HTTP 403** |
| Levi's 501 fit guide 博文 | `https://www.levi.com/US/en_US/blog/article/levis-501-fit-guide` | **HTTP 404** |
| Red Wing 875 旧路径 | `https://www.redwingshoes.com/red-wing-shoe-875-0875.html` | **HTTP 404** |
| Red Wing 875 另一路径 | `https://www.redwingshoes.com/heritage/mens/classic-moc/0875.html` | **HTTP 404** |
| Kular Fashion（第三方 501 描述） | `https://www.kularfashion.com/product/levis-501-original-jeans-ferry-blue-38249` | **HTTP 403**（Cloudflare 挑战页） |
| Levi's NZ 集合页 | `https://levis.co.nz/collections/men-501-jeans` | HTTP 200 但正文字段为空（JS 渲染） |
| Levi's 男装牛仔裤指南 | `https://levi.pt/en/features/men-jeans` | HTTP 200 但正文被导航吞掉 |

**结论**：Levi's 的**商品正文（版型描述）取不到**；能拿到的只有**分类归属、系列命名、档案文章**。
所以风格包里关于 501 的裤子形制描述，只有「Straight 直筒」这一条是 [物证]，其余（中腰、扣门襟、裤长盖鞋面）只能标 [推断] 或「部分确认」。

---

## C. [学术] 层

本次 `web_search` 在「美式复古 / Amekaji / KCI」方向命中了学术论文级别结果的标题与摘要级信息，但：
- 未取得全文 PDF
- 未取得论文中的频次统计表、样本量、编码方案原文

**因此本资料集不提供任何论文引文。**风格包中所有涉及「当年怎么穿」的断言，标记为 [归纳]（圈内共识 + 服装史常识），不冒充学术结论。

若后续要补齐，需要：论文 DOI → 期刊全文（多为付费墙）→ 或作者 preprint。

---

## D. 给风格包的口径

1. 形制（鞋 / 裤型的**可验证特征**）：用 A1、A4。
2. 时间轴：用 A3（有限，仅女装档案线）。
3. 颜色纪律、正反例、冲突仲裁：全部 [推断] / [归纳]，不挂学术名头。
4. 与商务正装 / 黑暗机能 / 老钱的边界：由本包自行定义，理由是这三包的判据已在本项目内写定。