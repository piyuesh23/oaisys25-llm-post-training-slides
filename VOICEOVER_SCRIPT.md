# 🎤 Voiceover Script
## "Beyond the Hype: What Post-Training Can (and Can't) Do for LLMs"

**Duration:** 40-42 minutes (+ 5-8 min Q&A)  
**Tone:** Professional yet conversational, with strategic humor  
**Pace:** ~140-160 words per minute

---

## SLIDE 1: TITLE SLIDE [30 seconds]

**[Pause for audience to settle]**

Good morning everyone! Welcome to "Beyond the Hype: What Post-Training Can and Can't Do for LLMs."

I'm excited to be here at OAISYS'25, and I promise you this: by the end of this session, you'll know exactly when to fine-tune your models, when to use RAG, and most importantly — when to just write better prompts and save yourself weeks of work.

This is a practical guide to model enhancement without breaking your model, your budget, or your spirit.

Let's dive in.

---

## SLIDE 2: SESSION OVERVIEW [1 minute]

So here's what we're covering today.

First, we're going to bust some myths. And I mean really bust them. We'll tackle five of the most common misconceptions about post-training that I see practitioners making every single day.

Then, we'll give you a decision framework — a practical guide for choosing the right approach for your specific problem.

We'll decode essential ML terminology with metaphors that actually make sense, not academic definitions that put you to sleep.

We'll look at how LLMs actually work under the hood — just enough to make smart decisions.

And finally, we'll walk through your complete post-training toolkit, common pitfalls to avoid, and key takeaways you'll actually remember tomorrow.

Sound good? Let's start with the myths.

---

## SLIDE 3: MYTH #1 - FINE-TUNING = ADDING KNOWLEDGE [3 minutes]

Myth number one: "Fine-tuning equals adding knowledge."

I hear this all the time: "If I fine-tune ChatGPT on our Q4 budget spreadsheet, it'll know all the numbers!"

No. It won't.

Here's the reality: Fine-tuning teaches behavior, tone, and patterns — not facts.

Think of it like teaching your dog a new trick. You're not uploading "knowledge" into its brain. You're reinforcing response patterns. The dog learns HOW to behave, not WHAT the world is.

So what's the solution if you need the model to know specific facts?

Use RAG — Retrieval-Augmented Generation. Give it access to the actual documents at runtime. Otherwise, you're just training it to sound really confident about numbers it's completely making up.

And trust me, a confident hallucination is worse than no answer at all.

---

## SLIDE 4: MYTH #2 - MORE DATA = BETTER MODEL [2.5 minutes]

Myth number two: "More data equals a better model."

The assumption: "Let's throw ALL our data at the model. More is better, right?"

The reality: More bad data equals more bad outputs. Quality beats quantity every single time.

The truth: You need to curate your training data like you're Marie Kondo-ing your closet. Does this data spark actual value? No? Then thank it for its service and throw it out.

Here's the key insight: Fine-tuning on messy, contradictory, or irrelevant data is like studying for a test by reading the entire internet. You'll learn chaos.

One hundred clean, high-quality examples will beat ten thousand messy ones every time. Remember that.

---

## SLIDE 5: MYTH #3 - RAG IS BASICALLY CHEATING [2.5 minutes]

Myth number three: "RAG is basically cheating."

The myth: "Using RAG means the model isn't really learning!"

Hot take: RAG isn't cheating. It's the right tool for the job.

Retrieval-Augmented Generation gives the model access to external knowledge at runtime. It's like letting someone use a calculator during a math test. Is that cheating? No. It's using the right tool to get accurate results.

Use RAG when:
- Your data changes frequently
- You need citations and sources
- The information wasn't in the training data
- You want to avoid hallucinations

RAG is your friend. Embrace it.

---

## SLIDE 6: MYTH #4 - YOU CAN TRAIN AWAY HALLUCINATIONS [2.5 minutes]

Myth number four: "You can train away hallucinations."

The hard truth: Hallucinations — those moments when ChatGPT invents facts with the confidence of a game show host — are baked into how LLMs work.

They're next-token prediction machines, not truth oracles. Fine-tuning won't magically fix this.

So what actually helps?

Better prompting. Clear, specific instructions.

RAG for grounding. Give it actual sources to work from.

Confidence scoring. Know when it's uncertain.

And teach it to say "I don't know." That's better than making things up.

You can't eliminate hallucinations, but you can reduce them dramatically with the right techniques.

---

## SLIDE 7: MYTH #5 - MODELS UNDERSTAND YOUR VAGUE VIBES [2 minutes]

Myth number five: "Models understand your vague vibes."

What you said: "Just make it sound more... professional?"

What the model heard: "Execute undefined_vibe.exe... ERROR 404."

LLMs need specificity. They're pattern-matching machines. They need clear, specific instructions.

Instead of hoping fine-tuning will telepathically understand your brand voice, give concrete examples. Show, don't tell.

Pro tip: If your prompt is vague, your output will be vague. Garbage in, artisanal garbage out.

Be specific. Be clear. Get better results.

---

## SLIDE 8: REAL-WORLD EXAMPLE [3 minutes]

Now let's look at a real-world example. Customer support bot transformation.

The wrong approach: A company decided to fine-tune on all their historical support tickets.

Cost: Five thousand dollars upfront.
Time: Three weeks.
Result: Outdated information, hallucinated policies.
Accuracy: Sixty-five percent.

Not great.

The right approach: RAG plus prompt engineering.

Cost: Five hundred dollars per month.
Time: Three days.
Result: Always current, cites sources.
Accuracy: Ninety-two percent.

The lesson: Fine-tuning taught the bot HOW to respond, but RAG gave it WHAT to say.

The combination of better prompting plus RAG delivered results ten times faster at one-tenth the cost.

That's the power of choosing the right tool.

---

## SLIDE 9: THE REALITY CHECK [3 minutes]

Let's talk about the reality check: cost, time, and expertise requirements.

Prompt engineering: Free. Takes hours to days. Low expertise required. Best for quick wins and iteration.

RAG: Dollar sign to two dollar signs. Takes days to a week. Medium expertise. Best for dynamic knowledge.

Fine-tuning: Two to three dollar signs. Takes one to three weeks. High expertise. Best for tone, style, and format.

RLHF or DPO: Three to four dollar signs. Takes weeks to months. Very high expertise. Best for alignment and safety.

Pro tip: Always start with the cheapest, fastest option. Graduate to more expensive methods only when you've exhausted simpler approaches.

Don't jump straight to fine-tuning when better prompts would solve your problem.

---

## SLIDE 10: THE DECISION FRAMEWORK [3 minutes]

So how do you decide what to use? Here's your decision framework.

Outdated or missing information? Use RAG. Give the model access to external, current knowledge bases.

Wrong tone or style? Use fine-tuning. Teach it how to talk, not what to know.

Bad at math, logic, or APIs? Use function calling. Let code handle code things.

Prompt isn't working? Try better prompting first. Rewrite it before going nuclear.

This framework will save you weeks of wasted effort. Use it.

---

## SLIDE 11-12: ML GLOSSARY [6 minutes total]

Now let's decode some essential terminology. I promise these definitions will actually make sense.

**Model:** The "brain" created after training. It's basically a mathematical pattern-matcher.

**Tokens:** Breaking text into crumbs so the model can digest it. "ChatGPT" becomes "Chat," "G," "PT."

**Embeddings:** The model's secret love language. Words get converted into numbers that capture meaning.

**Weights:** The billions of tiny knobs inside the model that get adjusted during training.

**Attention:** The part of the model that decides which words matter most in a sentence.

**Training:** Feeding the model lots of data so it can learn patterns. Like teaching a dog tricks, but with math.

[NEXT SLIDE]

**Inference:** Using the trained model to answer questions or make decisions. The model's "showtime."

**Labels:** The answer the model is supposed to learn. The actual house price in your training data.

**Overfitting:** When the model memorizes training data instead of learning to generalize. It's like a student who memorized the practice test but can't handle new questions.

**Underfitting:** When the model hasn't learned enough — too simple to capture useful patterns.

**Parameters:** The "knobs" inside the model that get tuned during training. Similar to weights but more general.

**Bias:** A systematic mistake. The model favors one type of outcome unfairly.

Got it? Good. Let's keep moving.

---

## SLIDE 13: HOW LLMs ACTUALLY WORK [2 minutes]

Quick architecture lesson. How do LLMs actually work?

Next-token prediction. LLMs predict the next most likely token. They don't have a "truth database" — they're sophisticated autocomplete on steroids.

And sometimes the most likely next word is confidently wrong.

Training gaps. The model never saw certain information, so it interpolates based on patterns. It's like a student who didn't study for a test and is winging the essay question with "vibes."

That's why RAG is so powerful — it fills those gaps with actual information.

---

## SLIDE 14: LIVE DEMO - SMS SPAM DETECTION [4 minutes]

Now let's see fine-tuning in action with a live demo.

**[SWITCH TO JUPYTER NOTEBOOK]**

The task: Fine-tune DistilGPT2 for SMS spam detection. We have a dataset of 5,572 SMS messages — some legitimate, some spam.

Let me walk you through what we did here.

First, we loaded the pre-trained DistilGPT2 model — completely untrained for this specific task. We evaluated it on our test set as a baseline.

The results? Accuracy of 85.7%, but here's the kicker: F1-score of zero. Precision zero. Recall zero. The model was basically guessing "ham" for everything. It couldn't detect spam at all.

Then we fine-tuned it. Three epochs on our training data. We're teaching it the patterns of spam versus legitimate messages — the behavior, the style, the structure.

**[SHOW TRAINING PROGRESS IF TIME PERMITS]**

After fine-tuning, look at these results:

Accuracy jumped to 99.1%. That's impressive, but look at the other metrics.

F1-score: 96.8%. From zero to nearly perfect.

Precision: One hundred percent. Perfect. Every message it flags as spam actually IS spam.

Recall: 93.8%. It catches almost all spam messages.

**[SHOW INFERENCE EXAMPLES]**

Let's test it on some real examples.

"Congratulations! You've won a one thousand dollar gift card!" — Spam, 99.9% confidence. Correct.

"Hey, just wanted to check in and see how you're doing." — Ham, 100% confidence. Correct.

"URGENT! Your mobile number has been selected for a free prize!" — Spam, 100% confidence. Nailed it.

**[RETURN TO SLIDES]**

Key insight: Fine-tuning transformed a model that couldn't detect spam at all into one with near-perfect precision.

This is fine-tuning done right. We're not teaching it facts about spam. We're teaching it to recognize patterns — the behavior of spam messages versus legitimate ones.

And that's exactly what fine-tuning is good for.

---

## SLIDE 15: HOW FINE-TUNING WORKS [2 minutes]

Now let me show you what actually happened under the hood.

**[NOTE: Diagrams are clickable - audience can open full-size versions in new tabs]**

**[SHOW PIPELINE DIAGRAM]**

On the left, you see the complete pipeline. We started with raw data — 5,572 SMS messages. We preprocessed it, split it into training, validation, and test sets. Then we tokenized the text, loaded the pre-trained DistilGPT2 model, evaluated the baseline, fine-tuned for 3 epochs, and achieved 99% accuracy.

Ten steps from raw data to production-ready model.

**[SHOW TRAINING LOOP DIAGRAM]**

And on the right, here's what happens during each epoch. The training data feeds batches of 16 messages to the model. The model makes predictions. We compare those predictions to the true labels and calculate the loss — that's the error. We compute gradients and send them to the optimizer, which updates the model's weights.

After each epoch, we evaluate on the validation set and save the best model based on F1-score.

This loop ran three times — three epochs — and each time, the model got better at recognizing spam patterns.

This is the magic of fine-tuning. We're not teaching it facts. We're adjusting billions of tiny weights to recognize patterns in the data.

**[OPTIONAL: If someone asks for details]**
> "Feel free to click on either diagram to see the full-size version in a new tab. The details are all there if you want to study them later."

---

## SLIDE 16: POST-TRAINING METHODS [4 minutes]

Your complete toolkit. Five post-training methods.

Number one: Prompt engineering. Start here. Always. It's free and fast.

Number two: RAG. For knowledge that changes or wasn't in training.

Number three: Fine-tuning, also called SFT. For behavior, tone, and task-specific patterns.

Number four: Function calling. For precision tasks like math, APIs, structured data.

Number five: Preference optimization — RLHF or DPO. For alignment and safety.

The key principle: Quality over quantity. In training data, prompts, and everything else. Curate ruthlessly. Test relentlessly. Iterate constantly.

---

## SLIDE 17: COMMON PITFALLS TO AVOID [3 minutes]

Learn from others' expensive mistakes. Five common pitfalls.

Pitfall one: Training without a baseline. You won't know if you improved or made things worse.

Pitfall two: Mixing knowledge and behavior. Use RAG for facts, fine-tuning for style. Don't mix them.

Pitfall three: Ignoring data quality. One hundred clean examples beat ten thousand messy ones.

Pitfall four: Over-optimizing test sets. You've memorized the test, not learned the task.

Pitfall five: Skipping prompt engineering. Try better prompts first — it's free and takes minutes, not weeks.

Avoid these, and you'll save yourself months of frustration.

---

## SLIDE 18: WHEN NOT TO POST-TRAIN [3 minutes]

Red flags that should make you stop.

It's actually a UX problem. Fix the interface, not the model.

You have fewer than fifty quality examples. Not enough for fine-tuning.

You haven't tried better prompts. Ninety percent of "we need fine-tuning" problems can be solved with better prompt engineering.

You're chasing benchmarks, not value. Your users don't care about BLEU scores.

Your data is messy or contradictory. Clean your data or don't train at all.

You have no clear success criteria. If you can't define "better," you can't measure if training worked.

If you see these red flags, stop. Rethink your approach.

---

## SLIDE 19: THE POST-TRAINING CHEAT SHEET [2 minutes]

Your quick reference guide.

Start with WHY. Have a clear reason before you begin.

Evaluate, THEN train. Know your baseline first.

Use SFT, then PO, then RL. Follow the proven recipe.

Curate clean, balanced data. Quality over quantity, always.

Run evals after each step. Measure progress continuously.

When done right, you get a reliable assistant. The goal is consistency and alignment.

Remember: Post-training isn't magic — it's cooking. Pick good ingredients, taste often, and don't burn the kitchen.

---

## SLIDE 20: KEY TAKEAWAYS [2 minutes]

What to remember tomorrow.

Post-training doesn't equal magic. It's a powerful toolkit — use the right tool for the right job.

Start simple, scale smart. Prompt engineering, then RAG, then fine-tuning, then function calling. In that order.

Hallucinations are features, not bugs. You can reduce them with RAG, grounding, and smart prompting, but you can't eliminate them.

Quality beats quantity. In data, prompts, and everything else.

Test relentlessly. Iterate constantly.

---

## SLIDE 21: FINAL WISDOM [1 minute]

Final wisdom.

Post-training is powerful, but it's not a magic wand.

Use it when it makes sense.

Not when trends tell you to.

Let's go forth and build something awesome!

---

## SLIDE 22: THANK YOU [30 seconds]

Thank you!

Remember: You don't need bigger models — you need smarter training.

Questions? Let's continue the conversation.

---

## Q&A SESSION [5-8 minutes]

**[Be ready for common questions:]**

**Q: "How much data do I really need for fine-tuning?"**
A: Minimum hundreds of high-quality examples. For most tasks, 500-1000 clean examples is a good starting point. But quality matters more than quantity.

**Q: "Can I use RAG and fine-tuning together?"**
A: Absolutely! RAG for facts, fine-tuning for tone. They complement each other beautifully.

**Q: "What's the biggest mistake you see people make?"**
A: Jumping straight to fine-tuning without trying better prompts first. Ninety percent of the time, better prompts solve the problem.

**Q: "How do I measure success?"**
A: Define clear metrics before you start. Accuracy, latency, user satisfaction, cost per query. Pick what matters for your use case and measure it.

**Q: "Is RLHF worth it for small teams?"**
A: Usually no. RLHF is expensive and complex. Unless you're building a product-level model, stick with simpler methods.

---

## CLOSING REMARKS [30 seconds]

Thank you all for your attention today. I hope this gives you a practical framework for making smart decisions about post-training.

Remember: Start simple. Test relentlessly. Iterate constantly.

And most importantly — don't let the hype drive your decisions. Let the data and your specific needs guide you.

Now go build something awesome!

---

**END OF SCRIPT**

**Total Speaking Time:** ~46-48 minutes (includes 4-min live demo + 2-min diagrams)  
**Q&A Buffer:** 2-4 minutes  
**Total Session:** 48-52 minutes

**Note:** 
- The live demo can be shortened to 2-3 minutes by skipping training progress visualization
- The diagram slide can be shortened to 1 minute or skipped entirely if running over time
- Focus on results and inference examples for maximum impact

---

## 🎯 DELIVERY TIPS

1. **Pace:** Aim for 140-160 words per minute
2. **Pauses:** Use strategic pauses after key points
3. **Energy:** High energy for myths, measured for technical sections
4. **Humor:** Land the jokes, but don't force them
5. **Audience:** Make eye contact, gauge understanding
6. **Time:** Check time at slide 10 (should be ~20 min mark)
7. **Flexibility:** Be ready to speed up or slow down
8. **Q&A:** Encourage questions throughout if audience is engaged

---

**Script Status:** ✅ READY FOR REHEARSAL
