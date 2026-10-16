# GISCI241 — Project images / 项目图片与标注

Toshka–Lake Nasser region, southern Egypt / 埃及南部 Toshka–Lake Nasser 地区。

本文件夹仅包含 12 张用户上传的原始图片和本说明，不包含代码或统计数据文件。原图内容未编辑，文件名已按年份及类型整理。

## 标注依据 / Caption provenance

年份依据本对话中用户确认的顺序：最初四张为 2013、2018、2019、2024；后续三张分类图为 2019、2018、2013。NDVI 和 MNDWI 的 2024 年份依据同一分析阶段的上下文标注，原图本身未显示年份。前四张来自早期全年浏览流程，后续图来自分类分析阶段；请勿将两种合成窗口混为一谈。

## 图例 / Legends

- 真彩色：Landsat 8 B4/B3/B2 对应红/绿/蓝显示通道。
- NDVI：棕色表示较低值，浅色至青绿色表示较高值；原代码显示范围为 −0.2 至 0.8。
- MNDWI：棕色表示较低值，青绿色表示较高值；原代码显示范围为 −0.6 至 0.6。
- 初步分类：浅棕色 Other；绿色 Vegetation；蓝色 Water。规则为 MNDWI > 0 判为水体，非水体中 NDVI > 0.2 判为植被，其余有效像元为 Other。
- 变化图：绿色 Other → Vegetation；蓝色 Other → Water；橙色 Vegetation → Other；紫色 Vegetation → Water；金黄色 Water → Other；粉红色 Water → Vegetation。未变化像元被掩膜，底图仍可见；底图颜色不是变化类别。

这些是地图截图，不是带地理参考的栅格。分类是初步阈值分类，没有独立精度验证。Other 不等于单一裸地类别，Vegetation 不等于全部耕地。

## 图片目录 / Gallery

### 2013 True colour / 真彩色（早期全年合成）

![2013 True colour / 真彩色（早期全年合成）](figures/01_true_colour_2013_exploratory.png)

原始文件 / Original: `image(20261013-192659).png`

### 2018 True colour / 真彩色（早期全年合成）

![2018 True colour / 真彩色（早期全年合成）](figures/02_true_colour_2018_exploratory.png)

原始文件 / Original: `image(20261013-192707).png`

### 2019 True colour / 真彩色（早期全年合成）

![2019 True colour / 真彩色（早期全年合成）](figures/03_true_colour_2019_exploratory.png)

原始文件 / Original: `image(20261013-192714).png`

### 2024 True colour / 真彩色（早期全年合成）

![2024 True colour / 真彩色（早期全年合成）](figures/04_true_colour_2024_exploratory.png)

原始文件 / Original: `image(20261013-192721).png`

### 2024 NDVI / 归一化植被指数

![2024 NDVI / 归一化植被指数](figures/05_ndvi_2024.png)

原始文件 / Original: `image(20261013-193735).png`

### 2024 MNDWI / 改进归一化差异水体指数

![2024 MNDWI / 改进归一化差异水体指数](figures/06_mndwi_2024.png)

原始文件 / Original: `image(20261013-193752).png`

### 2024 Preliminary land cover / 初步土地覆盖分类

![2024 Preliminary land cover / 初步土地覆盖分类](figures/07_land_cover_2024.png)

原始文件 / Original: `image(20261013-194108).png`

### 2024 True colour / 分类阶段的真彩色参照图

![2024 True colour / 分类阶段的真彩色参照图](figures/08_true_colour_2024.png)

原始文件 / Original: `image(20261013-194128).png`

### 2019 Preliminary land cover / 初步土地覆盖分类

![2019 Preliminary land cover / 初步土地覆盖分类](figures/09_land_cover_2019.png)

原始文件 / Original: `image(20261013-194736).png`

### 2018 Preliminary land cover / 初步土地覆盖分类

![2018 Preliminary land cover / 初步土地覆盖分类](figures/10_land_cover_2018.png)

原始文件 / Original: `image(20261013-194757).png`

### 2013 Preliminary land cover / 初步土地覆盖分类

![2013 Preliminary land cover / 初步土地覆盖分类](figures/11_land_cover_2013.png)

原始文件 / Original: `image(20261013-194816).png`

### 2013–2024 Land-cover changes / 土地覆盖变化

![2013–2024 Land-cover changes / 土地覆盖变化](figures/12_changes_2013_2024.png)

原始文件 / Original: `image(20261013-195320).png`

## 上传 GitHub

下载后解压，将整个 `GISCI241_Images` 文件夹拖入仓库的 Add file → Upload files 页面并提交。打开该文件夹的 README.md 即可查看图片及标注。也可直接上传 ZIP 作为下载附件，但仓库中不会直接展开显示其中的图片。
