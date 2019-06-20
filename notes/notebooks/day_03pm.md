# Case study: NLP in practice.

NLP applications:
* document summarization
* language translation
* spoken language systems

# AI for helping reply to emails. 
Smart reply from Google
Makes ~12% of email replies on mobile devices.

Challenges:
* universally accessible
* protect privacy of user data
* fast and efficient

Design
Email context --> potential replies

utilize recurrent neural networks.
like the problem of predicting the next word in a sentance,
we need to predict the potential response to an incoming email.

Utilize the Long-short-term memory model. 

Thought vector - captures semantic meaning of what is being said.
Like how a word vector captures the semantic meaning of a word.

## Incorporating heirarchical structure
language is heirarchical
for example:
letters > words > sentances > paragraphs > sections > chapters > books > ect

# Overcoming privacy concerns
Federation learning...

email and response are encoded as binary vectors
response similarity can be measured by calculating their Hamming distance
