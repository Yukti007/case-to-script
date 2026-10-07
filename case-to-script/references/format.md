# The diagnosis format

Every piece of content from this skill follows four parts, in this order.

| # | Part | What it must do | Failure sign |
|---|------|-----------------|--------------|
| 1 | **A specific problem someone has** | Name a person or role in a concrete situation, with a visible symptom | "Many companies struggle with..." |
| 2 | **The obvious move, and why it disappoints** | State what people try first, with evidence it falls short | Straw man, or no evidence |
| 3 | **What is actually going on** | Give the non-obvious mechanism underneath | A definition or a list of features |
| 4 | **The direction to look, and what it costs** | Point at where to dig next and name the real price | "Just do X" with no trade-off |

## Tests

- **Swap test:** replace the case with a different one. If the piece still reads fine, it is generic. Reject it.
- **Definition test:** does the piece open by defining a term? If yes, reject it.
- **Cost test:** does part 4 name a price (time, money, risk, trade-off)? If not, it is not finished.
- **Person test:** can you picture the one person in part 1? If not, make them more specific.

## Good example

**Case:** A two-person dental clinic in Pune added an AI chatbot to book appointments. Bookings did not go up.

1. **Problem:** The clinic owner paid for a booking chatbot, and three months later phone calls are still how 80% of patients book. (Illustrative figures.)
2. **Obvious move:** Blame the bot, switch vendors, or add more features. The next vendor gets the same result, because the bot was never the bottleneck.
3. **What is actually going on:** Patients who book by phone are not looking for a faster form. They are checking whether a human will pick up before they trust the clinic with a procedure. The bot removed the trust check without replacing it.
4. **Direction to look:** Treat the first phone call as a feature, and find out which bookings need reassurance and which are routine. Only automate the routine ones. The cost: someone has to answer the phone for the reassurance bookings, which is the exact time the owner hoped to save.

Why it works: one named person in one situation, an obvious move that fails for a stated reason, a mechanism the audience did not have, and a direction with an honest price.

## Bad example

**Topic:** "What is a chatbot and why small businesses need one."

1. Opens with a definition of chatbots.
2. Lists "5 benefits" (24/7 availability, cost savings, faster responses...).
3. Explains how large language models work.
4. Ends with "Start using AI in your business today!"

Why it fails:

- No specific person or problem, so it fails the person test.
- No obvious move that disappoints, because it only sells the idea.
- It explains a concept and diagnoses nothing, so it fails the definition test.
- No cost anywhere, so it fails the cost test.
- Any generic tech account could post it, so it fails the swap test.
