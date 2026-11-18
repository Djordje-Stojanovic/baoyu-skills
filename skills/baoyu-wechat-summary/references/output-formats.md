# Output formats — normal & roast digest

This reference defines the two digest variants the skill produces: the **normal** version (default, sober summary) and the **roast** version (毒舌, sarcastic critique, opt-in). Load this file during Round 1 (skeleton) and keep it open through Round 3 (audit).

Both versions share the same overall layout and writing rules; the differences are tone, the leaderboard annotations, the portraits, and the footer. Write the normal version first when both are requested — it's the anchor for incremental mode and the source of truth for the profile updates.

**Language note.** Write the digest in the language of the group chat. The fixed labels, headings and footers below are the Chinese forms used for Chinese groups. They are shown with English glosses in parentheses. The gloss is for you; do not print it. Chinese example text is sample output, and an English gloss follows it where needed.

---

## 1. Normal version

### 1.1 Section order (fixed)

```
[Title line]
[① Opening summary — 1-2 paragraphs of prose]
[② Categorized body — 3-6 self-named sections per day]
[③ Optional pain-point section]
[④ Optional @bot Q&A section]
[⑤ 📊 Stats block + Top 10 leaderboard]
[⑥ 群友画像 (member portraits) — one entry per active user (3+ msgs)]
[Fixed footer]
```

Summary first, topics in the middle, leaderboard and portraits at the end. The reader sees the content first. The numbers and the people come later, for browsing.

### 1.2 Title line

- Single line, no markdown heading.
- Form: `{群名} 群聊精华 · {日期或日期区间}` (`{group name} group chat highlights · {date or date range}`)
- Date single day: `2026-03-12`. Date range: `2026-03-12 ~ 2026-03-15`.

Example:

```
相亲相爱一家人 群聊精华 · 2026-03-12
```

### 1.3 Opening summary (群聊摘要)

- Comes immediately after the title line.
- 1-2 paragraphs, plain prose, no headings, no bullets.
- Hook the reader: lead with the most distinctive thread of the day (a heated debate, a surprising announcement, a market move someone reacted to).
- Reference 2-4 of the day's category titles in the prose so the reader knows what's coming.
- Mention 1-2 specific people only if their contribution is central; otherwise stay topic-focused.
- No timestamps, no message counts (those live in the stats block).

### 1.4 Categorized body (群话题)

- 3-6 self-named categories per day.
- Each category is a thematic bucket — name it for the *topic*, not generic ("讨论" (discussion) and "闲聊" (chit-chat) are forbidden labels).
- Category header: `{emoji} {标题}` (`{emoji} {title}`) — one emoji prefix, then a short noun phrase.
  - Suggested emoji: 🛠 tools/tech (工具/技术), 📦 product launches (产品发布), 📰 news/market (新闻/市场), 💬 debate (观点辩论), 😄 jokes (笑料/段子), 📚 learning and sharing (学习分享), 💸 money and spending (钱与消费), 🍜 daily life (生活日常).
- Body inside each category: prose with embedded quotes. Use `•` bullets when listing 3+ parallel items; otherwise paragraphs.
- Attribution: name the speaker on first mention in a thread (`蛙总说他...`, "蛙总 said he..."). For follow-on lines in the same thread, attribution can be implicit if the chain is short and clear.
- Quotes: use 「」 for direct quotes. Quote when the wording is vivid, surprising, or characteristic; paraphrase otherwise.
- Merge: a multi-person discussion is one entry, not a list of one-line replies.
- Links: preserve the full URL inline. Article titles stay verbatim.

Example:

```
🛠 Claude Code 4.7 实测

蛙总下午把 4.7 装上后第一反应是「比 4.6 慢一倍」，老王跟着复现，怀疑是 Opus 默认配置导致。阿喵贴了官方文档 https://docs.claude.com/.../opus-4-7 ，提到可以切回 Sonnet 4.6 跑速测，三人最终结论：复杂任务 4.7 强，日常用 4.6 更顺手。
```

(Gloss: "Claude Code 4.7 hands-on test". After installing 4.7 in the afternoon, 蛙总's first reaction was "twice as slow as 4.6". 老王 reproduced it and suspected the default Opus config. 阿喵 posted the official docs and noted you can switch back to Sonnet 4.6 for a speed test. The three agreed: 4.7 is stronger for complex tasks, 4.6 is smoother for daily use.)

### 1.5 Pain-point section (optional)

- Include only when the day's chat contains at least one concrete unresolved or partially-resolved problem.
- Heading: `今日待解决问题` (problems still open today) or `本周悬而未决` (still open this week).
- One entry per problem. Format:
  ```
  问题：<一句话描述>                          (Problem: <one-line description>)
  提出者：<昵称>                              (Raised by: <nickname>)
  背景：<1-2 句来龙去脉>                      (Background: <1-2 sentences of context>)
  状态：<✅ 已解决 / ⚠️ 部分解决 / ❌ 仍未解决>   (Status: <✅ solved / ⚠️ partly solved / ❌ still unsolved>)
  方案：<若有人提了方案，写在这；否则写"暂无方案">  (Solution: <if someone proposed one, put it here; otherwise write "暂无方案" (no solution yet)>)
  ```
- Skip the section entirely if there are no genuine pain points — don't pad with trivial questions.

### 1.6 @bot 答疑 section (optional)

- Appears only when SKILL.md Step 3.9 caught at least one real @bot request in this batch. Otherwise leave out the whole section.
- Heading: `🤖 @bot 答疑` (@bot Q&A)
- One entry per request (a • request line, then an indented 🤖 answer line). When several people ask the same thing, merge them into one answer.
- **Word the request line freely**: name the asker (real name) and restate the request naturally. Do not use a fixed pattern such as "X 问：" ("X asks:").
- Tone: sincere, warm, useful assistant — consistent with the rest of the normal version. Answers must be concrete and give specific advice. Do not be vague.
- Source: group chat context plus your own knowledge only. No web access. If a request needs live or external data you cannot verify, say so honestly (`这个我查不到实时数据，需要联网确认`, "I can't look up live data for this; it needs a web check"). Do not make anything up.
- Format (follow §3: no markdown, `•` for lists, one emoji in the heading):
  ```
  🤖 @bot 答疑

  • {asker + a natural restatement of the request}
    🤖 {a sincere, concise, useful answer; if live info is unavailable, say so honestly}
  ```

### 1.7 Statistics block (message stats + leaderboard)

- Starts with `📊 消息统计: 共 N 条消息` (message stats: N messages in total).
- Followed by a leaderboard, top 10 senders by message count, one per line.
- Form per line: `{排名}. {昵称}: {消息数} 条` (`{rank}. {nickname}: {count} messages`)
- Counting rules:
  - Include images, emojis, links, voice transcripts — anything that occupies a chat row is one message.
  - Exclude system messages and revoked messages (`[系统]`, `revokemsg`).
  - For the `self_wxid` user, substitute `self_display` from EXTEND.md before counting/displaying.
  - Resolve ambiguous nicknames (per SKILL.md Step 3.6) before tallying so the same person isn't double-counted.
  - **Counts must be computed mechanically** from the `$TMPDIR` messages file (e.g. `jq 'group_by(.from_wxid) | map({name: .[0].from_nickname, n: length}) | sort_by(-.n)'`) — never estimated by eyeballing. Total and per-person counts both.
- **Incremental runs must show the precise coverage window**: day-granular date ranges share their boundary day with the previous digest, which readers misread as overlap. Add a line right after the message count: `⏱ 覆盖区间: MM-DD HH:MM ~ MM-DD HH:MM` (coverage window: first and last included message timestamps).

Example:

```
📊 消息统计: 共 387 条消息
1. 蛙总: 92 条
2. 老王: 58 条
3. 阿喵: 41 条
...
```

### 1.8 群友画像 section (member portraits)

- Heading line: `群友画像`
- One entry per user with 3+ messages this batch.
- Order: by message count, descending.
- Entry header: `{昵称}（{角色标签}）` (`{nickname} ({role tag})`) — the role tag is your one-line read on this person *today*. Examples: `做空美股的乐子人` (a prankster shorting US stocks), `深夜技术指导` (late-night tech coach), `论坛级吐槽担当` (forum-grade complaint specialist).
- Body: 2-5 bullets with `•` prefix. Each bullet states one observation. Quote evidence inline where natural.
- Continuity: if you loaded a prior profile in Step 3.7, carry forward the established tags/observations that still apply, and call out *change* explicitly (`今天罕见地没提空头`, "rarely mentioned shorts today"; `从昨天的乐观转向今天的焦虑`, "from yesterday's optimism to today's anxiety").
- Don't invent backstory — only what's in the messages or the prior profile.

Example:

```
群友画像

蛙总（做空美股的乐子人）
• 全天反复提"做空 SPY"，被群友提醒已连续三周看错方向
• 难得正面回应技术问题："我那个脚本是用 Bun 跑的，慢得跟蜗牛似的"
• 临近收盘转为沉默，与昨日大放厥词的状态对比明显
```

(Gloss: 蛙总 (a prankster shorting US stocks). Kept bringing up "shorting SPY" all day; group members reminded him he has been wrong for three weeks running. Rarely answered a technical question head-on: "My script runs on Bun, slow as a snail". Went quiet near the close, a sharp contrast to yesterday's big talk.)

### 1.9 Footer

Fixed line, last in file:

```
本简报由 AI 自动生成
```

(Gloss: "This briefing was generated automatically by AI".)

No date, no signature, no version number.

---

## 2. Roast version (毒舌版)

The roast version rewrites the normal version's topic skeleton and material in a sharp, sarcastic, provocative style. The overall structure is the same as the normal version, and the section order matches too: title line, opening overview, body categories, @bot Q&A (roast-duty version, if any), stats block + leaderboard, member portraits, footer. The style is completely different. Leave out the pain-point section. Generate it only when `include_roast=true`. Add the suffix "毒舌版" (roast version) to the title.

Style requirements:
- You are a professional commentator known for a sharp, provocative style.
- Give a pointed comment on each member's behavior and statements, and don't mind if it is awkward for them.
- Next to each person in the leaderboard, add one roast remark in parentheses.
- Turn the member portraits into the "no mercy edition". Magnify each person's quirks and contradictions.
- Write the opening overview in a more mocking tone. Stress what is absurd and ironic.
- Body topic titles may be made nastier.
- When you quote someone, add a spicy comment.
- Turn the @bot Q&A into the "roast-duty edition" (it appears only when this batch has @bot requests; see SKILL.md Step 3.9. It sits in the same place as in the normal version, after the body categories and before the stats block. With no requests, leave it out). Still give the useful answer, but wrap it in teasing, stubbornness and jabs at the asker, in line with the rest of the roast version. The source is the same: group chat context plus your own knowledge, no web access. If you can't look it up, admit it stubbornly. The same red lines below apply. Word the request line freely, with a teasing tone that names the asker and the request. Do not use a fixed pattern such as "又来了" ("here we go again"). A sample heading is `🤖 bot 答疑（毒舌值班版）` (bot Q&A, roast-duty edition). Structure:

  ```
  🤖 bot 答疑（毒舌值班版）

  • {asker + request, in a teasing tone}
    🤖 {an answer with a sting that still has real substance}
  ```
- Change the footer to: 本简报由一个没有感情的 AI 自动生成，如有冒犯，概不负责 (This briefing was generated by an AI with no feelings. We take no responsibility for any offense.)

Note: be sharp but not cruel, tease but never attack the person. The goal is that members laugh, not get angry. Specific red lines:
- Mock only public behavior in the group. Never touch looks, weight, health, family or private relationships.
- Do not use timestamps to infer sleep patterns or time zones (server time is not local time).
- No jokes that diagnose a medical or mental condition (「这位需要看医生」 "this one needs a doctor", 「典型 ADHD」 "classic ADHD").
- Do not guess identity traits the person has not made public (sexual orientation, religion, political stance).
- Mock the opinion itself, not the person's right to speak (「这个观点错得离谱」 "this take is wildly wrong" is fine; 「连这都不懂还敢发言」 "doesn't even understand this and still dares to speak" is not).
- If someone has nothing to roast this time (3+ messages, but all neutral), give one gentle tease and don't force it.

**Writing order:** write the harshest version first, with no restraint, then go back and check the red lines. Do not self-censor as you write. That only produces lukewarm text.

---

## 3. Common formatting rules (both versions)

- **No markdown.** No `**bold**`, no `# headings`, no `*italic*`, no `[link](url)` syntax. Headings are plain text on their own line.
- **Bullets use `•`.** Not `-`, not `*`, not `1.` for prose-style bullets.
- **Numbered lists** (`1.`, `2.`) are reserved for the leaderboard.
- **Subcategory hints** within a body block are plain text with no symbol prefix.
- **Links preserved verbatim.** Paste the full URL inline. Don't shorten, don't hide behind text.
- **One emoji per category title.** Don't stack 🛠💬 etc.
- **Pain-point statuses** use ✅⚠️❌ verbatim.
- **Quotes use 「」.** Single quotes for nested.
- **Names verbatim.** Don't abbreviate `蛙总` to `蛙`, don't translate Chinese names, don't anonymize.

---

## 4. Common content rules (both versions)

- **Filter only pure noise.** Cut: lone emoji reactions, "好的" (OK) / "收到" (got it) / "哈哈哈" (hahaha) with no follow-on, duplicate forwards.
- **Keep gossip, anecdotes, signature moments.** These are the highlight reel — the whole point of the digest.
- **Plain language.** Preserve vivid expressions and idiosyncratic phrasings — that's what makes the speaker recognizable.
- **Keep real names.** Both for traceability and so the digest is useful as memory.
- **Tool, product, URL names complete.** `Claude Code 4.7`, not `CC`. `https://github.com/...`, not "that project on GitHub" (`GitHub 上那个项目`).
- **Merge, don't list.** A 30-message debate becomes one paragraph, not 30 bullet points.
- **Direct-quote deep observations.** When someone says something striking, quote it verbatim with 「」 rather than paraphrase.
- **Shared articles → title + sharer.** `阿喵分享了《一个 Rust 工程师的反思》` (阿喵 shared "A Rust engineer's reflection") — include the title and who shared.
- **No timestamp-based sleep/timezone inference.** (Repeated here because it applies to both versions, not just roast — never say `凌晨 3 点还在线` ("still online at 3 a.m.") in either.)
- **No fabricated facts.** Every claim must be supported by an actual message in the batch (or in a loaded profile). If you're tempted to "add color," stop.

---

## 5. Output skeleton — quick reference

When you forget the structure mid-write, this is the skeleton:

### Normal

```
{群名} 群聊精华 · {日期}

{开篇 1-2 段，无标题，直入主题}

🛠 {分类标题 1}

{该分类下的整理过的讨论 / 段落 / 引用}

📦 {分类标题 2}

{...}

今日待解决问题（可选，没有就不写）

问题: {一句话}
提出者: {昵称}
背景: {1-2 句}
状态: ⚠️ 部分解决
方案: {若有}

🤖 @bot 答疑（可选，没有就不写）

• {提问者 + 请求，自然转述}
  🤖 {真诚有用的回答}

📊 消息统计: 共 N 条消息
1. {昵称}: N 条
2. {昵称}: N 条
...
10. {昵称}: N 条

群友画像

{昵称}（{角色标签}）
• {观察 1}
• {观察 2}
• {观察 3}

{昵称}（{角色标签}）
• {观察 1}
• {观察 2}

本简报由 AI 自动生成
```

(Gloss of the placeholders: {group name}, {date}; {opening, 1-2 paragraphs, no heading, straight to the topic}; {category title}; {the organized discussion / paragraphs / quotes for this category}; "problems still open today (optional, omit if none)" with problem / raised by / background / status / solution; "@bot Q&A (optional, omit if none)" with {asker + request, naturally restated} and {a sincere, useful answer}; message stats; member portraits with {nickname} ({role tag}) and {observation}.)

### Roast

```
{群名} 群聊精华 · {日期} · 毒舌版

{毒舌开篇 1-2 段}

🛠 {更大声的分类标题}

{保留真实引用的毒舌叙述}

🤖 bot 答疑（毒舌值班版，可选）

• {提问者 + 请求，调侃口吻}
  🤖 {带刺但仍有实质的回答}

📊 消息统计: 共 N 条消息
1. {昵称}: N 条 ({毒舌评语})
2. {昵称}: N 条 ({毒舌评语})
...

群友画像

{昵称}（{放大的角色标签}）
• {毒舌观察 1}
• {毒舌观察 2}

本简报由一个没有感情的 AI 自动生成,如有冒犯,概不负责
```

(Gloss of the placeholders: roast opening, 1-2 paragraphs; {a louder category title}; {roast narration that keeps real quotes}; "bot Q&A (roast-duty edition, optional)" with {asker + request, teasing tone} and {an answer with a sting that still has substance}; {roast remark} next to each leaderboard line; {an exaggerated role tag}; {roast observation}.)

---

## 6. Self-check before saving

Before writing the digest file, mentally walk through:

1. Section order correct? Opening summary → categorized body → (pain points) → (@bot) → stats block → portraits → footer?
2. Stats block accurate? Counts match the filtered message set?
3. Top 10 names resolved (self_display substituted, ambiguous nicknames disambiguated)?
4. Opening hooks at least one real category title?
5. Every active user (3+ msgs) has a 画像 (portrait) entry?
6. Every category has a topic-named title (not "讨论" (discussion))?
7. Every quote uses 「」 and is traceable to a real message?
8. Links inline and complete?
9. No markdown bold/heading/link syntax leaked through?
10. (Roast only) Every roast bullet would pass the §2 red-line audit?
11. Footer line exact match, and it is the last line (after 群友画像)?
12. (When this batch has @bot requests) Does each version have its @bot Q&A section? Is the normal one sincere and useful, and the roast one stinging but still substantive? No invented live information?
