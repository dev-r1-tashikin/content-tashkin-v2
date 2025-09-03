# 结构化数据定义模板 (Structured Data Definition Template)

**数据对象名称:** [描述此数据结构的用途，例如: ProductInfo, UserPersona, KeywordList]
**格式:** [JSON / CSV / YAML / etc.]
**版本:** [版本号, 例如: 1.0]
**创建/更新日期:** [YYYY-MM-DD]

---

## 1. 目的与用途 (Purpose & Usage)

*   [简要说明创建此数据结构的背景和目的。]
*   [说明哪些 Agent 会生成或使用此数据结构。]

## 2. 字段定义 (Field Definitions)

| 字段名称 (Field Name) | 数据类型 (Data Type) | 描述 (Description)                                   | 是否必需 (Required) | 示例 (Example)                                      | 备注 (Notes)                                    |
| :-------------------- | :------------------- | :--------------------------------------------------- | :------------------ | :-------------------------------------------------- | :---------------------------------------------- |
| `id`                  | String               | 唯一标识符                                           | Yes                 | `"prod-covid-ag"`                                   |                                                 |
| `name`                | String               | 对象的可读名称                                       | Yes                 | `"reOpenTest COVID-19 Antigen Rapid Test Cassette"` |                                                 |
| `category`            | String               | 所属类别                                             | Yes                 | `"Infectious Diseases"`                             | 建议使用预定义的类别列表                          |
| `description`         | String               | 详细描述                                             | No                  | `"15分钟快速检测..."`                               |                                                 |
| `features`            | Array[String]        | 产品特点列表                                         | No                  | `["快速检测", "高准确性"]`                          |                                                 |
| `specifications`      | Array[Object]        | 规格参数列表，每个对象包含 'key' 和 'value' 字段 | No                  | `[{"key": "检测时间", "value": "15 分钟"}]`         |                                                 |
| `status`              | String               | 当前状态                                             | No                  | `"active"`                                          | 建议使用枚举值: `active`, `draft`, `archived` |
| ...                   | ...                  | ...                                                  | ...                 | ...                                                 | ...                                             |

---

## 3. 完整示例 (Complete Example)

```[格式，例如: json]
[在此处提供一个完整的数据结构示例]
{
  "id": "prod-covid-ag",
  "name": "reOpenTest COVID-19 Antigen Rapid Test Cassette",
  "category": "Infectious Diseases",
  "description": "15分钟快速检测...",
  "features": ["快速检测", "高准确性"],
  "specifications": [{"key": "检测时间", "value": "15 分钟"}],
  "status": "active"
}
```

---

**备注:** 此定义用于确保 Agent 生成和解析结构化数据时遵循统一的标准。
