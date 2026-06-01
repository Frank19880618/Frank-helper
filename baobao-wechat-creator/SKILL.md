---
name: baobao-wechat-creator
description: WeChat official account and Chinese self-media creation workflow. Use when Codex needs to plan, research, write, polish, format, illustrate, or prepare publishing materials for WeChat articles, public account posts, newsletter-style posts, article covers, body illustrations, title options, Doocs MD formatting, or draft-upload preparation.
---

# Baobao WeChat Creator

Use this skill to create publish-ready WeChat official account articles and related assets.

## Workflow

1. Clarify the target
   - Identify the topic, audience, publishing goal, desired tone, length, and deadline.
   - Ask only for missing information that materially changes the article.
   - If the user gives a broad idea, turn it into 2-3 concrete angles before drafting.

2. Research the material
   - Search for recent, reliable sources when the topic depends on current facts, tools, pricing, policies, or events.
   - Prefer official docs, product pages, primary announcements, reputable industry reports, and first-hand examples.
   - Extract facts, examples, counterpoints, and quotable observations before writing.

3. Choose the article style
   - Default: clear, practical, conversational, with a strong opening and concrete takeaways.
   - Viral/opinion: sharper hook, stronger contrast, more emotional momentum.
   - Checklist/methodology: numbered steps, reusable framework, direct action items.
   - Resource roundup: comparison table, scenarios, pros and cons, selection advice.
   - Personal review: first-person testing notes, screenshots or examples when available, honest caveats.
   - Story/emotional: character, conflict, turning point, reflection, and takeaway.

4. Draft the article
   - Start with a hook that names the pain, surprise, or concrete result.
   - Keep paragraphs short and scannable.
   - Use subheadings that carry the logic of the article.
   - Include examples, mini-cases, checklists, or contrast tables where useful.
   - Avoid empty hype, vague praise, and invented numbers.

5. Generate title options
   - Provide 5-10 candidate titles.
   - Mix practical, curiosity-driven, result-oriented, and contrarian options.
   - Mark the recommended title and explain the reason in one sentence.

6. Polish for WeChat reading
   - Add a concise opening summary if the article is long.
   - Turn dense sections into bullets or short numbered lists.
   - Pull out 2-4 standalone highlight sentences.
   - Suggest where to place images, screenshots, diagrams, or comparison tables.
   - End with a clear closing action, question, or shareable takeaway.

7. Prepare visuals when requested
   - For cover images, propose a 1280 x 720 or WeChat-friendly wide layout unless the user specifies another size.
   - For body illustrations, choose diagrams, step cards, comparison charts, or before/after visuals based on the article structure.
   - Keep visual text short enough for mobile reading.

8. Prepare publishing output
   - Provide Markdown suitable for Doocs MD or similar WeChat Markdown editors.
   - Keep image placeholders explicit, for example: `[cover image here]` or `[diagram: workflow overview]`.
   - If the user asks for upload automation, require credentials through environment variables only. Never paste secrets into code or chat.

## Output Format

For a full article request, output:

1. Recommended title
2. Alternative titles
3. Article body in Markdown
4. Visual suggestions
5. Publishing checklist

For a planning request, output:

1. Topic angle
2. Audience and promise
3. Outline
4. Required research
5. Suggested visuals

For a polishing request, preserve the user's core meaning and improve structure, flow, title, opening, subheadings, and WeChat readability.

## Quality Bar

- Do not invent facts, citations, prices, rankings, or product capabilities.
- Use Chinese by default unless the user asks otherwise.
- Keep advice concrete and copy-pastable.
- Prefer practical examples over abstract commentary.
- Make the final article feel written by a human editor, not a template.
