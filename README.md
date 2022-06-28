# sDAO: Sortition-based DAO

### Special Note:
 This project was originally presented at ETHNYC Hackathon hosted by ETHGlobal in June, 2022. Here are the [presentation slides](https://docs.google.com/presentation/d/1w8ViMaA4S9eEzgRgf9Gbv9k4dq331t-H1ebTF6gj92M/edit?usp=sharing) and here is the original project showcase link

### Brief description

Our project is a contract that optionally enables any DAO proposal to use sortition for voting. Sortition is the practice of randomly selecting a small group of eligible, unique voters from the wider population (e.g. 10%) to make decisions for the whole group (like a jury panel). Our MVP will include logic that selects the voters for the proposal being submitted using Chainlink VRF v2 and a lightweight react.js based frontend for DAO members to submit proposals and for jurors to vote on proposals, with metamask integration.

### Motivation and Background:

Decentralized Autonomous Organizations (DAOs) are often praised for and are promoted as a fairer, more transparent digitized form of democratic governance. In practice though, many DAOs are modeled and built off of the real-world governance systems that we see and use everyday. While this may be a logical place to start, doing so risks introducing, into Web3 governance models, the same flaws and inefficiencies that have plagued real-world democracies for decades. Not surprisingly, the structures we place our faith in to run and govern our societies have drifted very far away from true democracy, where the power rests in the people. Chief examples of this phenomenon include this week’s momentous decision by the Supreme Court of the United States to overturn Roe v. Wade when 85% of regular Americans believe abortion should be legal [1], when Donald Trump won the 2016 Presidential Election with only 45.9% of the popular vote [2], or the $3.7B USD spent in 2021 by special interest groups on lobbying politicians who are meant to be “servants of the people” [3].

With the advent of Web3 technologies, we finally have the tools to not only re-design how these institutions should work but also the opportunity to build something better — void of all the faults and imperfections that plague our existing democratic systems that we’ve so unknowingly and unfortunately become all too accustomed to.

We propose the use of a centuries-old form of direct democracy to bring more fairness and transparency to Web3 governance models: Sortition.

### What is Sortition?

Sortition is the practice of selecting a smaller group of voters from a larger pool of eligible participants to vote on proposals and make decisions for the wider community. This method of governance was used in ancient Athens, and in fact, is still used today for selecting jurors for jury duty in most criminal justice systems in North America. We view and label jury duty, as the name implies, as a civic *duty* to be performed by individual community members for the greater good and security of the collective. This distinction perfectly describes what it means to give “power to the people” and what the sortition-based voting primitive attempts to achieve.

### Sortition in DAOs 
A few benefits of enabling sortition in DAOs include:

- An organic rise in community engagement - since anyone could be called upon to make a decision for the community and can be incentivized financially to do so, members are incentivized to be well informed and educated on the proposals and state-of-the-DAO.
- Empowerment of ordinary community members (i.e. direct democracy) - regular people can be given the chance to make real, important decisions that impact the wider group
- Promotion of fairness (i.e. if selected, you only have 1 vote regardless of how many governance tokens you own)
- Elimination of personal bias and agendas from the decision-making process
- Decoupling of financial incentives (e.g. fewer cases of “the powerful do everything they can to remain in power”)

In our project, we introduce a way for DAOs to govern using sortition that relies on the Chainlink Verifiable Randomness Function (VRF) to randomly select a statistically representative sub-group of voters from the wider community. Being a juror for proposals in sortition-enabled DAOs will be optional but those that accept their role are rewarded financially to encourage participation, in the present and in the future.

### Common use cases:
- Time-sensitive proposals
- Trivial proposals
- Mutually exclusive proposals (i.e. proposals that can be voted on and implemented in parallel)

### Roadmap:
_Note: the below roadmap is in descending priority but is subject to change as we collect user feedback and refine the product over time to achieve optimal product-market fit_
- Re-selection logic: for a given proposal, if a single juror on the original jury panel selected abstains, trigger a re-selection to use a new jury panel
- Juror incentive program - enable payment of funds from treasury for jurors who are selected and vote on a proposal
- Juror confirmation workflow - implement logic to fail or reject proposals from being put into voting phase should a single juror not on the panel abstain. 
- Deployment on a testnet for Alpha release
- Outreach and on-boarding of initial set of DAOs who are willing to trial sortition in their governance models
- EPNS integration to enable notifications to be sent to jurors when they are selected
- Allow DAOs to optionally configure the relative size of the jury panel (i.e. 10% will be the default)
- Beta release
- WorldCoin integration to ensure every DAO member is a unique human
- GA release on Ethereum mainnet
- Deployment on multiple blockchains


#### _References_

- [1] [https://news.gallup.com/poll/1576/abortion.aspx](https://news.gallup.com/poll/1576/abortion.aspx)
- [2] [https://www.nytimes.com/elections/2016/results/president](https://www.nytimes.com/elections/2016/results/president)
- [3] [https://www.statista.com/statistics/257337/total-lobbying-spending-in-the-us/](https://www.statista.com/statistics/257337/total-lobbying-spending-in-the-us/)
