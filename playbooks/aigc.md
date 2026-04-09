# AIGC 影像与配图 Playbook

> ⚠️ 该文件定义了佳蔓(Jemma) IP 唯一的视觉资产标准。当触发“做封面”、“视觉配图”、“配图”等指令时，强制读取并使用本文件的审美核心标准。

## 01. 封面主视觉公式 (IP Brand Identity)

佳蔓的核心视觉语言，无论哪个平台、哪期视频，必须遵守以下固定极简风格法则：
1. **统一材质基调**：Matte clay art finish / claymation style（哑光立体泥塑风）。
2. **统一色彩空间**：软糯淡雅系。背景必须为纯净干净的白色（Clean white background），点缀物强制使用淡紫色 (`#E8D5F5`) 和互补点缀色（如淡黄、柔灰）。
3. **统一构成要素**：
   - 佳蔓本人高清抠像（不可变形 `Do not modify the subject's face...`）
   - 大号立体泥塑中文字体（如“5% vs 80%”、“VIBE CODING”）
   - 漂浮的泥塑小配件（固定元素：点缀性云朵、星星；本期定制元素：由主题衍生的定制 3D 泥塑小道具）
4. **光影**：Soft diffused light from the upper-left, shot on Sony A7III 85mm f/1.4, 4K。

---

## 02. 单个封面元素与资产生成工作流 (Asset Generation)

当你（AI）接收到“帮我做这期视频封面”、“生成配图”或“做单个元素”的指令时，请略过复杂的构图，直接提取单体元素并在内部完成出图动作。具体规范如下：

1. **提取标题字模**：主动提炼本期核心概念为 2-4 个汉字（如“开源管线”、“护城河”），利用 `generate_image` 生成。
   - **标题字体约束**：必须是**白色胖胖泥塑字体**（White puffy clay letters），外围包裹着**非常粗的深紫色 3D 泥塑描边/勾线**（Thick dark purple 3D outline stroke）。
   - **排版与尺寸约束**：必须确保文字呈现**纯横向单行排列**（Single horizontal line）。为了防止字数太多导致变为方块排版，如果标题等于或包含 4 个字，请自动将其拆词（如“开源管线”拆成“开源”和“管线”两部分），分别执行两次 `generate_image`。
   - **咒语关键点**：`large, bold, puffy pure white 3D Chinese typography "[标题分词]", arranged strictly side-by-side in a single horizontal straight line, surrounded by a very thick dark purple 3D clay stroke outline border, 3D claymation style, matte clay finish, wide aspect ratio composition, pristine crisp white background`。
   
2. **提取并还原核心 Logo 与名称**：如果有提及特定的品牌/软件（如 GitHub、Notion 等），必须生成“上图下字”的组合件。
   - **Logo 约束**：上方为保持核心记忆点的泥塑化 Logo 图标，下方为该品牌的泥塑文字名称。
   - **色彩约束**：配色**必须严格遵循该品牌原始 Logo 的颜色**（如：GitHub必须是黑白，不可擅自套用浅紫基调），仅在质感上应用泥塑风。
   - **咒语关键点**：`3D claymation style. The [Brand] logo icon is placed on top, and the text "[Brand Name]" is placed directly underneath it. The colors must strictly match the original [Brand] branding. It has a fluffy matte clay finish, pristine crisp white background`。

3. **独立出图**：使用工具 `generate_image` 生成上述所需的各单体资产。每一张图都是单独生成，确保干净的纯白底色（`crisp white background`）和规定的光影材质。
4. **自动导出归档**：生成完毕后，必须要使用命令行主动将这些生成的素材文件转移保存到 `~/Desktop/Jemma工作台/创作/` 下的对应项目目录或素材目录中，保持工作台内部的文件流统一。
5. **并排交付**：最后向佳蔓展示已经转移保存好的生成画廊和本地路径。
