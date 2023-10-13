---
# Documentation: https://wowchemy.com/docs/managing-content/

title: "95710E1 Exam 3 Note"
subtitle: ""
summary: ""
authors: []
tags: []
categories: []
date: 2023-10-12T19:34:01-04:00
lastmod: 2023-10-12T19:34:01-04:00
featured: false
draft: false
editable: false
math: true

# Featured image
# To use, add an image named `featured.jpg/png` to your page's folder.
# Focal points: Smart, Center, TopLeft, Top, TopRight, Left, Right, BottomLeft, Bottom, BottomRight.
image:
  caption: ""
  focal_point: ""
  preview_only: false

# Projects (optional).
#   Associate this post with one or more of your projects.
#   Simply enter your project's folder or file name without extension.
#   E.g. `projects = ["internal-project"]` references `content/project/deep-learning/index.md`.
#   Otherwise, set `projects = []`.
projects: []
---
## Review 3 Exam

### **Market power and Price discrimination**

**First degree price discrimination**

Selling at each customer's ***individual reservation price*** (at each customer's maximum willlingness to pay price).

-   producer must identify each customer's "type"

-   each customer pay their reservation price

-   consumer surplus is zero

-   producer gets all surplus

-   Pareto efficient!

**Second degree price discrimination**

Selling of the same versions but at different ***quantity*** and ***quality***

-   Quantity based

-   Quality based (versioning): basic, pro, Enterprise

-   Goldilock pricing for versioning is 3 versions, will always sell most at the middle version

**Third degree price discrimination**

Selling based on ***groups*** of customers (Sex, age, geographic location )

-   producer must identify the price sensitivity of groups

-   producer set price that maximizes each groups' profit

-   producer must prevent resale

-   example is student discount

**Other Pricing Strategy**

Bundling: Selling different things together

- example: apple music, newspaper
- this not really price discrimination

### Cost in the short and long run

- **Short Run**: In microeconomics, the short run is a period in which at least one input (like equipment or buildings) is fixed, while others are variable. Due to this, there are both fixed and variable costs in the short run.
  - **Fixed Costs**: Costs that do not change with the level of production. For example, the rent paid for a factory.
  - **Variable Costs**: Costs that change with the level of production. For example, costs of raw materials or wages.
- **Long Run**: In the long run, **all inputs are variable**, and there are no fixed costs. Firms can adjust all factors of production, such as building a bigger factory or reducing the size of their operations.
- Review of **Law of Diminishing Marginal Product/Increasing Marginal Cost**
  - ***diminishing marginal product*** is that there will be a increase in production initially per unit in crease in input (like labor) into the production but will eventually have decreasing production per unit input.

  - This causes per the cost of production per unit will start to increase.

### Return to scale, economies of scale

Constant return to scale

- increase of productive input (aka. productive factors) by t, the output also increase by t.
- all units cost the same to produce

Increasing return to scale

- increase of productive input by factor t, theo output will increase more than t times.
- avg cost go down ("economy of scale") and lonng run MC go down

Decreasing return to scale

- if we icnrease the productive input by factor t, the output go up less than t times.
- the more you produce the more each unit cost to produce
- (the last units cost more than the earlier ones: u-shaped long term average cost curves with upward sloping AC for higher production levels)

### Cost in IT industries

- Cost function in IT doesn't increase
  - high fixed cost
  - low variable costs
  - declining avg costs
  - MC maybe lower than avg costs
- IT industry will NOT be perfectly competitive
  - the large first-copy cost is only justified when firm can control a significant portion of the market
- Likely
  - Quasi-monopoly with dominant firm controlling most of the market, with cost leadership due to size/scale economies
  -  Oligopoly, with dominant firms controlling most of the market

### Strategies for IT firms

- achieve cost leadership through economies of scale and economies of scope.
- exploit first-mover advantages

## Game Theory

Definition: Study of strategic interactions rational players

- assumption: players are rational (want to maximize their payoff), has common knowledge

Payoff: a player's benefits/costs arising from their own actions and the actions of the others.

### Action vs. Strategy

- An action is a **choice**.
- A strategy a set of actions based on con

### Strictly Dominant Strategy

A strategy that has a (strictly) lower payoff than another strategy regardless of the other player’s or players’ strategy(ies).

- The other player will make sure that the other will never get to play the strictly dominant strat.

### Nash Equilibrium

A set of strategies, one for each player, is a Nash equilibrium if NO player can **unilaterally** change their strategy and receive a higher payoff

# Oligopoly

Few firms running a single industry.

- # of producer: few dominant
- size of firms: smaller than mono.
- profit: zero
- strategy: non-strategic; oli. have "various behavioral patterns, from collusion (cooperative behavior, like forming cartels) to non-cooperative behavior (competing aggressively)"

### Oligopoly Strategies:

Simultaneous games:

- Quantity (Cournot model)
- Price (Bertrand model)

Sequential games:

- Quantity leadership (Stackelberg model)
- price leadership

## Cournot Model

Simultaneous quantity setting:

- Assume firms choose quantity first, then market **equilibrium price** is the **inverse demand curve**
- The two firms choose the **quantity without knowledge of what the other**'s choice (simultaneous).
- Each has the same common demand function, their own cost functions, profit maximization behavior
- Solve a Cournot problem for firm 1 by using [f1's cost function, market demand function (common)].
  - Cost function for firm 1: c(q1)= xxx
  - Market demand: Q = xxx - p; market price (inverse of demand): p(Q)
  - market quantity, **Q = q1+q2+...**, is the sum of all the firms' **total production quantity**;
  - firm 1 produce at **q1**
  - Solve profit maximization condition for firm 1 to get q1*; equation is = TR1 - TC1 = **q1 * p*(Q) - c(q1)**; then, derivative with respect to q1 and set it to zero to get expression for q1*
  - Then do the the other firms to solve the system for q1**, q2**, ...

## Stackelberg Model

- Quantity leadership: one firm chooses quantity first (the leader, and could be dominant firm), and the other choose to respond (the follower).
  - The leader considers the follower's profit maximization problem.
  - The follower solves the optimization problem given the leader's choice.
    - solves the reaction function and then put in the leader's value.
  - the **leader calculates the follower's reaction function and substitutes it (the function) into its own maximization**
- Solve the profit maximization equation for the **leader (using q1 as quantity of the leader, q1 = q_leader = q_l )**:
  - Get the follower's maximization problem, which should be expressed in q2 = (xxx-q1)/yyy
  - Put the profit maximization equation into its own profit function (the leader's PROFIT function not derivative yet!)
    - getting: =  q1* p(Q) - c(q1) = q1 * (xx -q1 -q2) - c(q1) = q1*(xx-q1-((xxx-q1)/yyy) ) - c(q1)
    - solve q1 then solve q2 using its equation

### Bertrand model

Simultaneous price setting.

- firms choose price and don't change it; quantity can adapt quickly.
- **Bertrand’s paradox:** if we assume no capacity constraints and equal MC, even with just 2 firms the Bertrand equilibrium is the competitive outcome (i.e. p = MC)

## Asymmetric Information

Participants on one side of the market are **more informed** about attributes of a certain transaction than participants on the other side.

1. Hidden information (maybe about features and quality of a product), which may cause "**adverse selection**"
2. Hidden action (actions of a party after a contract is signed), which may cause "**moral hazard**"

## Hidden Information

> Gains-to-trade (i.e. economic surplus for buyers and sellers) can be generated when buyers are well informed

### Expected Value

EV = sum over values of possible outcome times their probabilities

> There exist a market for cars with two conditions, one is the good type (plum) and the other is the bad type (lemon). A seller would sell "plum" higher than $2000 and "lemon" higher than 1000, and a buyer would buy a "plum" lower than $2400 and "lemon" lower than $1200.

Assume the fractions of "plums" and "lemons" are q and (1-q).

Assume buyer know only q, but not which is which.

The seller knows which is which.

Then, EV = $1200 * (1-q) + $2400*q.

Suppose, EV > $2000. Then, seller can negotiate a price between EV and $2000, which gives high gain for the seller.

Suppose, EV < $2000. Then, seller cannot negotiate a price above $2000. Sellers of good cars will exit the market. Buyers would know only "lemons" exist in market, causing highest price willing to pay for a car lower than $1200.

**Lemons market and adverse selection**

High proportions of "lemons" "crowds out" "plums".

- This is **adverse selection**

Existence of "lemons", in this case, inflicts external cost on buyers and sellers of "plums".

### Signaling

"Plum" seller tell buyer that this market is good, improving everything.

- Reduce information asymmetry
- Reduce adverse selection
- Reduce inefficiencies in the market

## Hidden Action and Moral Hazard

One party to a contract or transaction may change their behavior after the contract or transaction has been concluded.

**Examples**

Government disaster aid programs

Disincentives to protect property?

Unemployment benefits

Reduced incentives to work?

Financial bail-out

Increases banks’ future risk-taking?

### Principle-agent problem

A principle that hires an agent to do something without the ability to oversee the agent's actions. If the agent has incentives to not act in the best interests of the principle then this would be a problem.

- The principle would want to design a contract that counteract this problem. For instance, by paying the agent on performance.
  - Examples
    - Employer and employee
    - Investor and financial advisor
    - Teacher and student

## Loss Aversion (behavior economics)

## Collusion

Firms acting together as a unit, almost like a monopoly; forming a "cartel". This can help them raise the price higher than what they can do in the Cournot case.

- Explicit collusion
  - Joint Executive Committee, 1880-1886
  - Cartels
- Tacit collusion
  - hard to prosecute, hard to differentiate from good business practice

### Cartels

Illegal in most countries, but there are some international cartels

- PMEC, or the diamond cartel

###  Strategic Behavior

- Entry deterrence: keeping firms from entering this market
  - capacity expansion
    - limited pricing
    - blockade entry
    - entry accommodation
    -
    - product proliferation
    - contracts
  -
- predation
  - predatory pricing
  - non-pricing predation
    - abuse dominant position

### Mergers and Acquisitions
