---
title: Shojinka - Flexible Manpower
---

My QA team was divided into 4, drug vs non-drug (Dental, EHC) and adjudication engine was supporting application.
I'll focus on the two app teams. Just as Toyota can't control which cars customers will want, we couldn't control which features the customers wanted. Sometimes we'd have lots of work for the drug team, but not for the non-drug.

Here's how we got to level utilisation so that nobody was sitting idly for months.
1. First the drug app team had virtually no work for a release (3-6 months) so I had them make regressions using Robot Framework. This worked well but I realised it'll do nothing for our lead time. This is because there wasn't going to be any more drug app work for the forseable future.
2. Next I asked them to help out the non-drug team. They tried creating regression automation to help the non-drug testers execute tests faster. The problem was that the old tests they were reading lacked a lot of detail. This mean they had to keep asking those SME for clarification which just slowed them down. This also didn't help the lead time.
3. Finally, I decided to get the non-drug testers to write the tests so clearly that they could be farmed out to the drug app testers. This was already a practice done by the drug-engine testers. Though the non-drug app testers were slowed down by putting in more detail, the lead time went down because the drug app testers were doing the execution. The side effect of these super clear test cases was that we could also automatically convert them to test automation mid release eventually eliminating the end of release exercise to select tests for regression automation.
