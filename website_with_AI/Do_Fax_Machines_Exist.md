# I Haven't Seen a Fax Machine in 20 Years. So I Built One.

I have not posted in a long while.

---

My friend Mike gave me the idea to put a fax service on the internet. First thing — I did not realize the U.S. still uses fax. My response was, "I have not seen a fax machine in 20 years." In the AI age, fax systems are still being used. Hard to believe.

As a challenge and an experiment, I built the fax service.

**So, punch line first: the system is 80% managed by AI.** I will get to why it is 80% in a minute.

---

## Vibe-Coding the Backend and Frontend

Both the backend and frontend were vibe-coded. When I hear "no coding experience is needed," I always think — okay, how? *"I don't understand!!"*

While building the backend, a practical thought hit me: if the average fax takes three minutes to complete and I only have one line, how many faxes can I do in a day? What if I have two lines?

In my dialog with Claude, I suggested round-robin scheduling. I wanted something simple because I can configure the number of concurrent faxes. Wait — I was having a conversation with something that is not human and cannot even see me.

Claude came back and suggested using a **least-recently-used algorithm** instead. I gave the go-ahead. I tested it and it seemed to work, based on the amount of testing I did. I burned **$100 USD** sending faxes — close to **2,000 pages**. I had Codex verify the implementation also. I put unwarranted faith in Codex.

## The Blind Spot Question

If someone had no development experience, would they have even thought about congestion? Would Claude or Codex raise that issue without being prompted? Not sure. I am just thinking about what level of complexity can be built with no experience. Will Claude or Codex or GLM 4.7 fill in the blind spots? Maybe when AGI hits. Showing my age.

## Infrastructure

The system is running on AWS ([faxitonce.com](https://faxitonce.com)) and is integrated with Stripe. I used Claude to set up the infrastructure. I am certified, so I gave instructions on what I wanted, then verified it was implemented correctly.

## Why 80% AI-Managed

An agent kicks off every hour to check for issues. If there is an error, I get an alert. When there is, I message Claude:

> "I just received an alert about an error. What happened?"

I get a response, then I use Claude to craft an email to the user. I review the email, then have it sent. I am not comfortable with emails being automatically sent yet.

I also do ad hoc questions early in the morning, around 6:00 AM:

> "How many faxes were sent yesterday?"
>
> "Provide me a sales report for the past two days."

Then I go back to Zzzz.

## Final Thought

I do not know if you can run a billion-dollar company by giving agency to a bunch of AI agents. Well, you can run a website with AI.

Just sharing.

---

*More coming on Anthropic Co-work.*
