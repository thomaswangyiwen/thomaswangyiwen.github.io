---
layout: post
title: "Some JaneStreet Capital Interview Questions"
description: ""
category: "Interview"
tags: [brainTeasers]
---
{% include JB/setup %}


###Set1
Here are some leaked telephone interview(1st round) questions from JaneStreet Capital from [YanWen Jiang](http://blog.renren.com/blog/229272878/493791508?bfrom=01020100200 YanWenJiang):


1. It is noon. The hour hand and minute hand overlap. When is the next time these two hands overlap again?

2. There are 3 coins. One coin has heads on both sides, one coin has tails on both sides, the third one has head on one side and tail on the other side. Now I pick up one coin and toss. I get head. What is the chance that the coin I picked has heads on both sides?

3. There are 25 horses. Each time you can race 5 horses together. Now you need to pick the top three horses among them. How many races do you need to conduct?

Answers：

1.1:05:300/11

2. 2/3

3. 7 races

###Set2

1.A company has a value V which is uniformly distributed between 0 and 1. you are planning to place a bid B for the company. If B is smaller than V, then your bid loses and you get nothing; if B is larger than V, you get to purchase the company at price B, and the company will end up being worth 1.5 * V. What price B should you bid to maximize your profit?

A:(Unknown)

###Set3

1. mental arithmetics (no calculator, no paper and pen)

43-87=?

11%*182=?

38*42=? What is the percentage you are confident with your answer?

2. I roll a die, and I will give you an amount in pounds equal to the number on the die. For example, if I get 5, I will give you 5 pounds. What is the price you are willing to pay for this game?(a: 3.5)


now say that when you roll the die, you are allowed to either take the money that you get with the roll, or roll a second time. But you have to take whatever it is of the second roll. what is the price you willing to pay to play?(a: 4.25)


3. 3 coins, what is the probability that I get two heads? If 4 coins, what is the probability that I get at least two heads? How confident you are with this answer?(a: 0.5, 11/16)


4. One normal ball has length 8-inch weighs 80kg, what is a 12-inch ball weigh? (a: 270kg)


5. If I drop a ball from 10 meters high, it will always rebound half the distance, e.g. the first time, it rebounds 5m high, then the second time 2.5m, etc. So how long does the ball travel after it finally stops? Confident?(a: 30m)


最后，如果有人有志做quant，我很建议大家看看Crack 的"Heard on the street"这本书。

###Set4
1. You have 3000 apples at Edingburgh want to transfer as many apples as you can to London. You have a truck, the maximum capacity of which is 1000 apples. London is 1000 miles away from Cambridge and when the truck is carrying apples, for every mile it drives, it will drop one apple. What is the maximum number of apples you can deliver to London?


Answer: 
1) In three separate trips, we will transfer the 3000 apples to our first stopping point. At the first stopping point, we want to have as close to 2000 apples as possible. This way, when we start moving again, we have as close to 1000 apples as possible in our truck.
This leads us to solving: 3000-3*x=2000; x~333.33 miles (round up to 334), where x is the distance in miles we travel to the first stopping point. Note that we multiply 'x' times 3 since we are taking the apples in three separate runs. After truckin' the 3000 apples, in three separate runs, 334 miles, we have 3000-3*334=1998 apples left and 666 miles left to go.

2) At the second stopping point, we want to have as close to 1000 apples as possible. This way, when we start moving again, we have as close to 1000 apples as possible in our truck. This leads us to solving: 1998-2*y=2000 =&gt; y=499, where y is the first stopping point. Note that we multiply 'x' times2 since we are taking the apples in two separate runs. Now, we have 1998-2*499=1000 apples left and 167 miles left to go.
3) We then load up the truck with a 1000 apples and travel 167 miles. At the end, we have 1000-167=833 apples


2. 抛一个10个面的dice，数字分别为1-10。记下每次抛后的面值并做累加，一旦总和超过100则停止。请问最终最有可能得到的总和值为多少？


Answer: 我用Monte-Carlo仿真计算结果为104，但不知理论解法如何。

###Set5
Pre-Interview
(Ten minutes)

1) Mental Math: One million minus one hundred eleven.
2) Mental Math: Fifty-four percent of one hundred ten.
3) Game: With one die, suppose in a round, you earn the amount of dollars equal to the value of the upwards face of the die. (eg. you earn $6 if you roll a six.) Now also suppose after your first roll, you are given the opportunity to cancel your first and roll again, taking that value as the final value. What should your strategy be?
4) What's the closest integer to the square root of 1420.
5) You and a roommate are hosting a party. You invite 10 other pairs of roommates. During the party you poll everyone at the party (excluding yourself) and ask how many hands each person shook. Two conditions:
a) Each person did not shake his roommate's hand.
b) Each person shook a different number of hands.
Question: How many hands did you roommate shake?
6) a) You roll a die, and are given an amount in dollar equal to the number on the die. What would you pay to play this game if you played it a lot of times? 
b) now say that when you roll the die, you're allowed to either take the money that you'd get with the roll, or roll a second time; if you roll a second time, you're obligated to take the number of dollars that you get with the second roll. Now what is the worth of the game? 
c) Same thing as above, except you have an option to play the game a third time.

Interview
(Thirty minutes)

1) Suppose you are given the opportunity to bid for a treasure chest, which you know with 100% confidence to be priced anywhere between $0-$1000. If you bid equal to or above the price, you win the treasure chest (at the cost of your bid). If you bid below the price, you do not earn the treasure chest. Now, also suppose you have a friend who is willing to buy the treasure chest from you for one and a half times the price of the treasure chest (should you obtain the chest). What should your bid be?

2) In Baseball, the batting average is the number of hits over the number of at bats. Player A has a greater batting average than Player B in the first half of the season and the second half of the season. Is it possible that Player B would have a higher batting average for the entire season?

3) How much calories does a Big Mac have? Would you bet $1 on it? How about $10?

4) How many tons does the ocean weigh?

5) How much would you be willing to bet on it being within 25% of that at even odds?

6) A company has a value V which is uniformly distributed between 0 and 1. you are planning to place a bid B for the company. If B is smaller than V, then your bid loses and you get nothing; if B is larger than V, you get to purchase the company at price B, and the company will end up being worth 1.5 * V. What price B should you bid to maximize your profit?

7) On a sheet of paper, you have 100 statements written down. the first says, "at most 0 of these 100 statements are true." the second says, "at most 1 of these 100 statements are true." ... the nth says, "at most (n-1) of these 100 statements are true. ... the 100th says, "at most 99 of these statements are true." how many of the statements are true?

8) You have two decks of cards: one has 13 reds and 13 blacks, and the other has 26 reds and 26 blacks. We play a game in which you select one of the two decks, and pick two cards from it; you win the game if you select two black cards. Which deck should you select to maximize your chances of winning? Try to do this problem in your head, without writing any calculations down.

9) You have a deck of 52 cards, and you keep taking pairs of cards out of the deck. if a pair of cards are both red, then you win that pair; if a pair of cards are both black, then I win that pair; if a pair of cards has one red and one black, then it's discarded. If, after going through the whole deck, you have more pairs than I do, then you win $1, and if I have more pairs than you do, I win $1. What is the value of this game in the long run?

###Summary

JaneStreet Capital's questions are typically hard to answer. It needs practices to survive the interview. More inf can be found [here](http://www.glassdoor.com/Interview/Jane-Street-Trader-Intern-Interview-Questions-EI_IE255549.0,11_KO12,25.htm JaneStreetInterview) and [official statement](https://blogs.janestreet.com/interviewing-at-jane-street/ official statement)