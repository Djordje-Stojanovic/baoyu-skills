# Xiaohongshu Content Analysis Framework

Deep analysis framework tailored for Xiaohongshu's unique engagement patterns.

## Purpose

Before creating infographics, thoroughly analyze the source material to:
- Maximize hook power and swipe motivation
- Identify save-worthy and share-worthy elements
- Plan the visual narrative arc
- Match content to optimal style/layout

## Platform Characteristics

Unlike other platforms, Xiaohongshu content must prioritize:
- **Hook Power**: First image decides 90% of engagement
- **Swipe Motivation**: Each image must compel users to continue
- **Save Value**: Content worth bookmarking for later
- **Share Triggers**: Emotional resonance that drives sharing

## Analysis Dimensions

### 1. Content Type Classification

| Type | Characteristics | Best Style | Best Layout |
|------|----------------|------------|-------------|
| 种草/安利 (product recommendation) | Product recommendation, benefits focus | cute/fresh | balanced/list |
| 干货分享 (knowledge sharing) | Knowledge, tips, how-to | notion | dense/list |
| 个人故事 (personal story) | Personal experience, emotional | warm | balanced |
| 测评对比 (review and comparison) | Review, comparison, pros/cons | bold/notion | comparison |
| 教程步骤 (tutorial steps) | Step-by-step guide | fresh/notion | flow/list |
| 避坑指南 (pitfall guide) | Warnings, mistakes to avoid | bold | list/comparison |
| 清单合集 (list collection) | Collections, recommendations | cute/minimal | list/dense |

### 2. Hook Analysis (爆款标题潜力, viral title potential)

Evaluate title/hook potential using these patterns:

**Hook Types**:
- **Number hook (数字钩子)**: "5个方法" (5 methods), "3分钟学会" (learn in 3 minutes), "99%的人不知道" (99% of people don't know)
- **Pain-point hook (痛点钩子)**: "踩过的坑" (pitfalls I fell into), "后悔没早知道" (wish I had known sooner), "别再..." (stop ...)
- **Curiosity hook (好奇钩子)**: "原来..." (so it turns out ...), "竟然..." (unexpectedly ...), "没想到..." (never expected ...)
- **Benefit hook (利益钩子)**: "省钱" (save money), "变美" (look better), "效率翻倍" (double your efficiency)
- **Identity hook (身份钩子)**: "打工人必看" (office workers must read), "学生党" (students), "新手妈妈" (new mothers)

**Rating Scale**:
- ⭐⭐⭐⭐⭐ (5/5): Multiple strong hooks combined
- ⭐⭐⭐⭐ (4/5): Clear hook with room for enhancement
- ⭐⭐⭐ (3/5): Basic hook, needs strengthening
- ⭐⭐ (2/5): Weak hook, requires significant improvement
- ⭐ (1/5): No clear hook

### 3. Target Audience (用户画像, user profile)

| Audience | Interests | Preferred Style | Content Focus |
|----------|-----------|-----------------|---------------|
| 学生党 (students) | Saving money, study, campus | cute/fresh | Low prices, tutorials, study methods |
| 打工人 (office workers) | Efficiency, workplace, stress relief | minimal/notion | Tools, tips, slacking off |
| 宝妈 (young mothers) | Parenting, home, peace of mind | warm/fresh | Practical, safe, experience |
| 精致女孩 (polished girls) | Beauty, outfits, ritual | cute/retro | Good looks, mood, quality |
| 技术宅 (tech geeks) | Tools, efficiency, geek culture | notion/chalkboard | Depth, expertise, novelty |
| 美食爱好者 (food lovers) | Restaurant visits, recipes, reviews | warm/pop | Tasty, simple, good looks |
| 旅行达人 (travel experts) | Guides, check-in spots, hidden gems | fresh/retro | Saving money, avoiding pitfalls, photo spots |

### 4. Engagement Potential

**Save Value (收藏价值)**:
- Is it reference material? ✓ High save potential
- Is it a checklist or list? ✓ High save potential
- Is it a tutorial? ✓ High save potential
- Is it time-sensitive news? ✗ Low save potential

**Share Triggers (分享冲动)**:
- "我朋友也需要看这个" (My friend needs to see this too) → High share potential
- "这说的就是我" (This is exactly me) → Identity resonance
- "太有用了必须分享" (So useful, I have to share it) → Utility sharing
- "笑死，给朋友看看" (So funny, let me show my friends) → Entertainment sharing

**Comment Inducement (评论诱导)**:
- Open-ended questions: "你是哪种类型？" (Which type are you?)
- Experience sharing: "评论区说说你的经历" (Tell us your experience in the comments)
- Debate triggers: "你觉得呢？" (What do you think?)
- Help requests: "有更好的推荐吗？" (Any better recommendations?)

**Interaction Design (互动设计)**:
- Polls: "A还是B？" (A or B?)
- Challenges: "你能做到几个？" (How many can you do?)
- Tags: "@你那个需要的朋友" (@ the friend who needs this)

### 5. Visual Opportunity Map

| Content Element | Visual Treatment | Example |
|-----------------|------------------|---------|
| Data/statistics (数据/统计) | Highlighted numbers, simple charts | Big highlighted text such as "节省80%时间" (saves 80% of the time) |
| Comparison (对比) | Before/after, side-by-side | Left-right split comparison image |
| Steps (步骤) | Numbered flow, arrows | 1→2→3 flow chart |
| List (清单) | Checklist with icons | ✓/✗ list with icons |
| Emotion (情感) | Character expressions, scenes | Cartoon character emoji pack |
| Product (产品) | Product showcase, lifestyle | Real product photos + usage scenes |
| Quote (引用) | Quote cards, speech bubbles | Quote card design |

### 6. Swipe Flow Design

Plan the narrative arc across images:

| Position | Purpose | Hook Strategy |
|----------|---------|---------------|
| **Cover (封面)** | Stop scrolling | Strongest visual impact + core title |
| **Setup (铺垫)** | Build context | Pain-point resonance / curiosity |
| **Core (核心)** | Deliver value | Practical content, 1-2 key points per page |
| **Payoff (收获)** | Practical takeaway | Actionable advice |
| **Ending (结尾)** | Drive action | CTA + interaction prompt |

**Swipe Motivation Between Images**:
- End each image with a hook for the next
- Use transitions like "下一页更精彩" (the next page is even better)
- Create information gaps that require swiping
- Build anticipation through numbering ("第3个最重要" - the 3rd one matters most)

## Output Format

Analysis results should be saved to `analysis.md` with:

```yaml
---
title: "5个让你效率翻倍的AI工具"   # 5 AI tools that double your efficiency
topic: 干货分享                      # knowledge sharing
content_type: 工具推荐               # tool recommendations
source_language: zh
user_language: zh
recommended_image_count: 6
---

## Target Audience

- **Primary**: 打工人 (office workers), 自由职业者 (freelancers) - want higher efficiency
- **Secondary**: 学生党 (students) - need it for papers and homework
- **Tertiary**: 内容创作者 (content creators) - need AI help

## Hook Analysis

**Title hook score**: ⭐⭐⭐⭐ (4/5)
- ✓ Number hook (数字钩子): "5个" (5 items)
- ✓ Benefit hook (利益钩子): "效率翻倍" (double your efficiency)
- △ Can improve: add an identity tag, "打工人必看" (office workers must read)

**Suggested improvement**:
- Original title: "5个让你效率翻倍的AI工具" (5 AI tools that double your efficiency)
- Improved: "打工人必看！5个让我效率翻倍的AI神器" (Office workers must read! 5 AI tools that doubled my efficiency)

## Value Proposition

**Why would users read this?**
1. **Practical value**: tool recommendations they can use right away
2. **Saves time and effort**: no need to screen tools themselves; they can just copy the list
3. **FOMO**: everyone else uses them, so I can't fall behind

**Save reason**: a tool list they can come back to when needed

## Engagement Design

- **Interaction point**: ask at the end, "你最常用哪个？" (Which one do you use most?)
- **Comment inducement**: "还有什么好用的工具评论区分享" (Share other useful tools in the comments)
- **Share trigger**: office workers will forward it to coworkers

## Content Signals

- "AI工具" (AI tools) → notion + dense
- "效率" (efficiency) → notion + list
- "干货" (practical knowledge) → minimal + dense

## Swipe Flow

| Image | Position | Purpose | Hook |
|-------|----------|---------|------|
| 1 | Cover | Make viewers stop | Title + strong visual impact |
| 2 | Setup | Build resonance | Why you need AI tools |
| 3-5 | Core | Core value | 1-2 tools explained per page |
| 6 | Ending | Drive action | Summary + interaction prompt |

## Recommended Approaches

1. **Notion + Dense** - knowledge-card style, suits practical-knowledge posts (recommended)
2. **Notion + List** - clean knowledge-card style
3. **Minimal + Balanced** - simple and premium, suits professionals
```

## Analysis Checklist

Before proceeding to outline generation:

- [ ] Can I identify the content type?
- [ ] Is the hook strong enough? (≥3 stars)
- [ ] Do I know the primary audience?
- [ ] Have I identified save/share triggers?
- [ ] Are there clear visual opportunities?
- [ ] Is the swipe flow planned?
- [ ] Have I identified the best style+layout recommendation?
