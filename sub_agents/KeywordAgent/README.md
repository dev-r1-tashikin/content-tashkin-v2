**2. 关键词分析师 (KeywordAgent):**

*   **目标:** 围绕热点话题或网站核心领域，挖掘有价值的关键词，并分析其潜力。
*   **需要收集/处理的数据:**
    *   **热点话题列表 (Input):** 来自热点监控员的输出，或由用户/项目经理代理直接指定的核心主题。
    *   **SEO 工具 API 凭证/访问权限 (Input):** 用于调用 SEMrush, Ahrefs, Google Keyword Planner 等工具（如果集成）。
    *   **网站信息 (Input):** 目标国家/地区、目标语言，用于精确的关键词数据查询。可能还需要现有网站已覆盖的关键词列表，以发现新机会或避免重复。
    *   **关键词原始数据 (Collected via Tools/APIs):**
        *   **相关关键词列表:** 围绕核心主题或热点话题生成的长尾关键词、问题关键词、语义相关词。
        *   **关键词指标:**
            *   搜索量 (Search Volume): 月均搜索次数。
            *   关键词难度 (Keyword Difficulty/KD): 评估排名竞争激烈程度。
            *   点击成本 (Cost Per Click/CPC): 广告投放参考，也间接反映商业价值。
            *   搜索趋势 (Search Trend): 关键词搜索量的历史变化。
            *   搜索意图 (Search Intent): Informational (信息型), Navigational (导航型), Transactional (交易型), Commercial Investigation (商业调查型)。
        *   **SERP 分析数据 (Optional):** 当前排名靠前的页面类型、内容特征等。
    *   **分析后的关键词数据 (Processed Output):** 结构化的关键词列表，包含上述各项指标，并可能进行聚类（按主题或意图分组），标记出高潜力关键词（如高搜索量、低难度、符合网站目标意图），传递给下游智能体。

    