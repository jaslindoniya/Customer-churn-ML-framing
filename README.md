# Customer Churn - ML Framing & Baseline

# Why I Didn't Build an ML Model First

Everyone jumps to build an ML model for churn. I didn't.

The business was losing Rs.5000 per churned customer. My first question was: Can we solve this with a simple rule?

### What I found:

I looked at 12 sample customers (original data is 7000).
- Customers who stay: ~18 months with us
- Customers who leave: ~4 months, with lots of support tickets

So I wrote a simple rule:
"If a customer is with us <6 months, raised 3+ tickets, and didn't login for 10 days -> they will churn"

Result? **91.7% accuracy.**

No ML. Just 3 lines of logic.

### So what's the point?

If a simple rule gives 91.7%, any ML model I build must beat 95% to be worth it. Otherwise, why add complexity?

### What's inside this repo:

- `baseline_churn.ipynb` - My EDA and that simple rule
- `churn_sample.csv` - The sample data
- `responsible-data-card.md` - Where data came from, bias, risks
- `problem-framing-memo.md` - What decision we are taking and when

### My learnings:

1.  Always build a baseline first
2.  A missed churn (FN) costs Rs.5000, a wrong offer (FP) costs Rs.500 - so recall is more important
3.  If the model is confused (40-60% confidence), better to send to a human than guess
4.  If precision drops below 40% for 2 weeks, go back to the simple rule

This is a framing project, not a modeling project. Framing is 80% of the work.

---
Made for internship task - happy to get feedback!
