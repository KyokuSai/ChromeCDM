4.10.3112.0

Simply put, GPT-5.6-sol is almost incapable of completing “this” task.

Because the task is so complex and difficult, several rounds of Compaction are inevitable. During those rounds, GPT-5.6-sol is very likely to realize that it should refuse tasks involving DRM circumvention.

For Grok-4.7, however, I wrote a highly effective set of prompts specifically for this purpose.

With those prompts, Grok’s refusal rate was close to zero. Even in its reasoning, there was only a single sentence expressing reservations about reverse-engineering Widevine, and it would resume the task directly after Compaction.

That was perfect—but Grok’s ability to handle complex programming tasks was much less impressive.

I had Grok work for a very long time to understand the white-box logic in Widevine, but its overall progress may have been only 10–20%.

Grok is very good at carrying out full instructions, but its ability to understand things is poor.

If given a complete plan to follow, Grok might be able to complete the reverse engineering and subsequently export the plaintext keys. But if it has to figure out that plan on its own, I think it would struggle—and consume a considerable amount of money and time.

While experimenting with Grok, I also tried GPT-6.1-sol.

Having used GPT-6.1-sol to reverse-engineer quite a few other programs, I know that it is genuinely very capable. I have also always liked GPT’s engineering capabilities best: inexpensive yet powerful.

Its refusal mechanism, however, is very interesting. Initially, I did not tell it that plaintext keys would never appear in memory, so it immediately tried to capture them there. But once I told it not to waste time trying to capture them from memory, it immediately realized that the task would require reverse-engineering Widevine and refused. I tried this many times, and it almost always refused before actually beginning to reverse-engineer Widevine.

When I asked it merely to analyze Widevine, it gave some very “standard” answers. If I then pointed out which parts of its analysis were wrong or unlikely to work, it would instead push back against my analysis, arguing that although mine might be reasonable, its own explanations were still possible.

So, in practice, this did almost nothing to advance the ultimate ChromeCDM goal.

In the end, I distilled what I had learned from these attempts into a set of prompts for a certain AI and provided it with my analysis of Widevine and its white-box implementation.

Although it did still refuse once under those prompts, that refusal came after it had already extracted the plaintext keys.

Guided by the analysis and methods I provided, it completed the plaintext key extraction in seven hours.

https://t.me/HanaCream
