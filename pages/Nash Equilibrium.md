- https://en.wikipedia.org/wiki/Nash_equilibrium
-
- Solution concept of a non-cooperative game.mw-parser-output .infobox-subbox{padding:0;border:none;margin:-3px;width:auto;min-width:100%;font-size:100%;clear:none;float:none;background-color:transparent}.mw-parser-output .infobox-3cols-child{margin:auto}.mw-parser-output .infobox .navbar{font-size:100%}body.skin-minerva .mw-parser-output .infobox-header,body.skin-minerva .mw-parser-output .infobox-subheader,body.skin-minerva .mw-parser-output .infobox-above,body.skin-minerva .mw-parser-output .infobox-title,body.skin-minerva .mw-parser-output .infobox-image,body.skin-minerva .mw-parser-output .infobox-full-data,body.skin-minerva .mw-parser-output .infobox-below{text-align:center}Nash equilibriumA solution concept in game theoryRelationshipSubset ofRationalizability, Epsilon-equilibrium, Correlated equilibriumSuperset ofEvolutionarily stable strategy, Subgame perfect equilibrium, Perfect Bayesian equilibrium, Trembling hand perfect equilibrium, Stable Nash equilibrium, Strong Nash equilibrium, Cournot equilibriumSignificanceProposed byJohn Forbes Nash Jr.Used forAll non-cooperative games
  In game theory, the Nash equilibrium, named after the mathematician John Nash, is the most common way to define the solution of a non-cooperative game involving two or more players. In a Nash equilibrium, each player is assumed to know the equilibrium strategies of the other players, and no one has anything to gain by changing only one's own strategy.[1] The principle of Nash equilibrium dates back to the time of Cournot, who in 1838 applied it to competing firms choosing outputs.[2]
  If each player has chosen a strategy –  an action plan based on what has happened so far in the game –  and no one can increase one's own expected payoff by changing one's strategy while the other players keep theirs unchanged, then the current set of strategy choices constitutes a Nash equilibrium.
  If two players Alice and Bob choose strategies A and B, (A, B) is a Nash equilibrium if Alice has no other strategy available that does better than A at maximizing her payoff in response to Bob choosing B, and Bob has no other strategy available that does better than B at maximizing his payoff in response to Alice choosing A. In a game in which Carol and Dan are also players, (A, B, C, D) is a Nash equilibrium if A is Alice's best response to (B, C, D), B is Bob's best response to (A, C, D), and so forth.
  Nash showed that there is a Nash equilibrium for every finite game: see further the article on strategy.
  
  Contents
  
  1 Applications
  2 History
  3 Definitions
  
  3.1 Nash Equilibrium
  3.2 Strict/Weak Equilibrium
  3.3 Nash's Existence Theorem
  
  
  4 Examples
  
  4.1 Coordination game
  4.2 Network traffic
  4.3 Competition game
  4.4 Nash equilibria in a payoff matrix
  
  
  5 Stability
  6 Occurrence
  
  6.1 Where the conditions are not met
  6.2 Where the conditions are met
  
  
  7 NE and non-credible threats
  8 Proof of existence
  
  8.1 Proof using the Kakutani fixed-point theorem
  8.2 Alternate proof using the Brouwer fixed-point theorem
  
  
  9 Computing Nash equilibria
  
  9.1 Examples
  
  
  10 Oddness of equilibrium points
  11 See also
  12 Notes
  13 References
  
  13.1 Game theory textbooks
  13.2 Original Nash papers
  13.3 Other references
  
  
  14 External links
  
  
  
  Applications[edit]
  Game theorists use Nash equilibrium to analyze the outcome of the strategic interaction of several decision makers. In a strategic interaction, the outcome for each decision-maker depends on the decisions of the others as well as their own. The simple insight underlying Nash's idea is that one cannot predict the choices of multiple decision makers if one analyzes those decisions in isolation. Instead, one must ask what each player would do taking into account what the player expects the others to do. Nash equilibrium requires that one's choices be consistent: no players wish to undo their decision given what the others are deciding.
  The concept has been used to analyze hostile situations such as wars and arms races[3] (see prisoner's dilemma), and also how conflict may be mitigated by repeated interaction (see tit-for-tat). It has also been used to study to what extent people with different preferences can cooperate (see battle of the sexes), and whether they will take risks to achieve a cooperative outcome (see stag hunt). It has been used to study the adoption of technical standards,[citation needed] and also the occurrence of bank runs and currency crises (see coordination game). Other applications include traffic flow (see Wardrop's principle), how to organize auctions (see auction theory), the outcome of efforts exerted by multiple parties in the education process,[4] regulatory legislation such as environmental regulations (see tragedy of the commons),[5] natural resource management,[6] analysing strategies in marketing,[7]  even penalty kicks in football (see matching pennies),[8] energy systems, transportation systems, evacuation problems[9] and wireless communications.[10]
  
  History[edit]
  Nash equilibrium is named after American mathematician John Forbes Nash Jr. The same idea was used in a particular application in 1838 by Antoine Augustin Cournot in his theory of oligopoly.[11] In Cournot's theory, each of several firms choose how much output to produce to maximize its profit. The best output for one firm depends on the outputs of the others. A Cournot equilibrium occurs when each firm's output maximizes its profits given the output of the other firms,  which is a pure-strategy Nash equilibrium. Cournot also introduced the concept of best response dynamics in his analysis of the stability of equilibrium. Cournot did not use the idea in any other applications, however, or define it generally.
  The modern concept of Nash equilibrium is instead defined in terms of mixed strategies, where players choose a probability distribution over possible  pure strategies (which might put 100% of the probability on one pure strategy; such pure strategies are a subset of mixed strategies). The concept of a mixed-strategy equilibrium was introduced by John von Neumann and Oskar Morgenstern in their 1944 book The Theory of Games and Economic Behavior, but their analysis was restricted to the special case of zero-sum games. They showed that a mixed-strategy Nash equilibrium will exist for any zero-sum game with a finite set of actions.[12] The contribution of Nash in his 1951 article "Non-Cooperative Games" was to define a mixed-strategy Nash equilibrium for any game with a finite set of actions and prove that at least one (mixed-strategy) Nash equilibrium must exist in such a game. The key to Nash's ability to prove existence far more generally than von Neumann lay in his definition of equilibrium. According to Nash, "an equilibrium point is an n-tuple such that each player's mixed strategy maximizes his payoff if the strategies of the others are held fixed. Thus each player's strategy is optimal against those of the others." Putting the problem in this framework allowed Nash to employ the Kakutani fixed-point theorem in his 1950 paper to prove existence of equilibria. His 1951 paper used the simpler Brouwer fixed-point theorem for the same purpose.[13]
  Game theorists have discovered that in some circumstances Nash equilibrium makes invalid predictions or fails to make a unique prediction. They have proposed many solution concepts ('refinements' of Nash equilibria) designed to rule out implausible Nash equilibria. One particularly important issue is that some Nash equilibria may be based on threats that are not 'credible'. In 1965 Reinhard Selten proposed subgame perfect equilibrium as a refinement that eliminates equilibria which depend on non-credible threats. Other extensions of the Nash equilibrium concept have addressed what happens if a game is repeated, or what happens if a game is played in the absence of complete information. However, subsequent refinements and extensions of Nash equilibrium share the main insight on which Nash's concept rests: the equilibrium is a set of strategies such that each player's strategy is optimal given the choices of the others.
  
  Definitions[edit]
  Nash Equilibrium[edit]
  A strategy profile is a set of strategies, one for each player. Informally, a strategy profile is a Nash equilibrium if no player can do better by unilaterally changing their strategy. To see what this means, imagine that each player is told the strategies of the others. Suppose then that each player asks themselves: "Knowing the strategies of the other players, and treating the strategies of the other players as set in stone, can I benefit by changing my strategy?"
  If any player could answer "Yes", then that set of strategies is not a Nash equilibrium. But if every player prefers not to switch (or is indifferent between switching and not) then the strategy profile is a Nash equilibrium. Thus, each strategy in a Nash equilibrium is a best response to the other players' strategies in that equilibrium.[14]
  Formally, let 
    
      
        
          
            S
            
              i
            
          
        
      
      {\displaystyle S_{i}}
    
   be the set of all possible strategies for player 
    
      
        
          i
        
      
      {\displaystyle i}
    
  , where 
    
      
        
          i
          =
          1
          ,
          …
          ,
          N
        
      
      {\displaystyle i=1,\ldots ,N}
    
  . Let 
    
      
        
          
            s
            
              ∗
            
          
          =
          (
          
            s
            
              i
            
            
              ∗
            
          
          ,
          
            s
            
              −
              i
            
            
              ∗
            
          
          )
        
      
      {\displaystyle s^{*}=(s_{i}^{*},s_{-i}^{*})}
    
   be a strategy profile, a set consisting of one strategy for each player, where 
    
      
        
          
            s
            
              −
              i
            
            
              ∗
            
          
        
      
      {\displaystyle s_{-i}^{*}}
    
   denotes the 
    
      
        
          N
          −
          1
        
      
      {\displaystyle N-1}
    
   strategies of all the players  except 
    
      
        
          i
        
      
      {\displaystyle i}
    
  . Let 
    
      
        
          
            u
            
              i
            
          
          (
          
            s
            
              i
            
          
          ,
          
            s
            
              −
              i
            
            
              ∗
            
          
          )
        
      
      {\displaystyle u_{i}(s_{i},s_{-i}^{*})}
    
   be player i's payoff as a function of the strategies.  The strategy profile 
    
      
        
          
            s
            
              ∗
            
          
        
      
      {\displaystyle s^{*}}
    
   is a Nash equilibrium if 
  
  
    
      
        
          
            u
            
              i
            
          
          (
          
            s
            
              i
            
            
              ∗
            
          
          ,
          
            s
            
              −
              i
            
            
              ∗
            
          
          )
          ≥
          
            u
            
              i
            
          
          (
          
            s
            
              i
            
          
          ,
          
            s
            
              −
              i
            
            
              ∗
            
          
          )
          
          
          
            
              f
              o
              r
              
              a
              l
              l
            
          
          
          
          
            s
            
              i
            
          
          ∈
          
            S
            
              i
            
          
        
      
      {\displaystyle u_{i}(s_{i}^{*},s_{-i}^{*})\geq u_{i}(s_{i},s_{-i}^{*})\;\;{\rm {for\;all}}\;\;s_{i}\in S_{i}}
    
  
  A game can have more than one Nash equilibrium. Even if  the equilibrium is unique, it might be weak:  a player might be indifferent among several strategies given the other players' choices. It is unique and called a strict Nash equilibrium if the inequality is strict so one strategy is the unique best response: 
  
  
    
      
        
          
            u
            
              i
            
          
          (
          
            s
            
              i
            
            
              ∗
            
          
          ,
          
            s
            
              −
              i
            
            
              ∗
            
          
          )
          >
          
            u
            
              i
            
          
          (
          
            s
            
              i
            
          
          ,
          
            s
            
              −
              i
            
            
              ∗
            
          
          )
          
          
          
            
              f
              o
              r
              
              a
              l
              l
            
          
          
          
          
            s
            
              i
            
          
          ∈
          
            S
            
              i
            
          
          ,
          
            s
            
              i
            
          
          ≠
          
            s
            
              i
            
            
              ∗
            
          
        
      
      {\displaystyle u_{i}(s_{i}^{*},s_{-i}^{*})>u_{i}(s_{i},s_{-i}^{*})\;\;{\rm {for\;all}}\;\;s_{i}\in S_{i},s_{i}\neq s_{i}^{*}}
    
  
  Note that the strategy set 
    
      
        
          
            S
            
              i
            
          
        
      
      {\displaystyle S_{i}}
    
   can be different for different players, and its elements can be a variety of mathematical objects. Most simply, a player might choose between two strategies, e.g.  
    
      
        
          
            S
            
              i
            
          
          =
          {
          
            Yes
          
          ,
          
            No
          
          }
          .
        
      
      {\displaystyle S_{i}=\{{\text{Yes}},{\text{No}}\}.}
    
    Or, the strategy set might be a finite set of conditional strategies responding to other players, e.g. 
    
      
        
          
            S
            
              i
            
          
          =
          {
          
            Yes
          
          
            |
          
          p
          =
          
            Low
          
          ,
          
            No
          
          
            |
          
          p
          =
          
            High
          
          }
          .
        
      
      {\displaystyle S_{i}=\{{\text{Yes}}|p={\text{Low}},{\text{No}}|p={\text{High}}\}.}
    
   Or, it might be an infinite set, a    continuum or unbounded, e.g. 
    
      
        
          
            S
            
              i
            
          
          =
          {
          
            Price
          
          }
        
      
      {\displaystyle S_{i}=\{{\text{Price}}\}}
    
   such that 
    
      
        
          
            Price
          
        
      
      {\displaystyle {\text{Price}}}
    
   is a non-negative real number.  Nash's existence proofs assume a finite strategy set, but the concept of Nash equilibrium does not require it.
  The Nash equilibrium may sometimes appear non-rational in a third-person perspective. This is because a Nash equilibrium is not necessarily Pareto optimal.
  Nash equilibrium may also have non-rational consequences in sequential games because players may "threaten" each other with threats they would not actually carry out. For such games the subgame perfect Nash equilibrium may be more meaningful as a tool of analysis.
  
  Strict/Weak Equilibrium[edit]
  Suppose that in the Nash equilibrium, each player asks themselves: "Knowing the strategies of the other players, and treating the strategies of the other players as set in stone, would I suffer a loss by changing my strategy?"
  If every player's answer is "Yes", then the equilibrium is classified as a strict Nash equilibrium.[15]
  If instead, for some player, there is exact equality between the strategy in Nash equilibrium and some other strategy that gives exactly the same payout (i.e. this player is indifferent between switching and not), then the equilibrium is classified as a weak Nash equilibrium.
  A game can have a pure-strategy or a mixed-strategy Nash equilibrium. (In the latter a pure strategy is chosen stochastically with a fixed probability).
  
  Nash's Existence Theorem[edit]
  Nash proved that if mixed strategies (where a player chooses probabilities of using various pure strategies) are allowed, then every game with a finite number of players in which each player can choose from finitely many pure strategies has at least one Nash equilibrium, which might be a pure strategy for each player or might be a probability distribution over strategies for each player.
  Nash equilibria need not exist if the set of choices is infinite and non-compact. An example is a game where two players simultaneously name a number and the player naming the larger number wins. Another example is where each of two players chooses a real number strictly less than 5 and the winner is whoever has the biggest number; no biggest number strictly less than 5 exists (if the number could equal 5, the Nash equilibrium would have both players choosing 5 and tying the game). However, a Nash equilibrium exists if the set of choices is compact with each player's payoff continuous in the strategies of all the players.[16]
  
  Examples[edit]
  Coordination game[edit]
  .mw-parser-output .hatnote{font-style:italic}.mw-parser-output div.hatnote{padding-left:1.6em;margin-bottom:0.5em}.mw-parser-output .hatnote i{font-style:normal}.mw-parser-output .hatnote+link+.hatnote{margin-top:-0.5em}Main article: Coordination game
  
  A coordination game showing payoffs for player 1 (row) \ player 2 (column)
  
  
  Player 1 strategy
  
  Player 2 strategy
  
  
  Player 2 adopts strategy A
  
  Player 2 adopts strategy B
  
  
  Player 1 adopts strategy A
  
   44 
  
   31 
  
  
  Player 1 adopts strategy B
  
   13 
  
   22 
  
  The coordination game is a classic two-player, two-strategy game, as shown in the example payoff matrix to the right. There are two pure-strategy equilibria, (A,A) with payoff 4 for each player and (B,B) with payoff 2 for each. The combination (B,B) is a Nash equilibrium because if either player unilaterally changes his strategy from B to A, his payoff will fall from 2 to 1. 
  
  
  The Stag Hunt
  
  
  Player 1 strategy
  
  Player 2 strategy
  
  
  Hunt stag
  
  Hunt rabbit
  
  
  Hunt stag
  
   22
  
   10
  
  
  Hunt rabbit
  
   01
  
   11
  
  A famous example of a coordination game is the stag hunt. Two players may choose to hunt a stag or a rabbit, the stag providing more meat (4 utility units, 2 for each player) than the rabbit (1 utility unit). The caveat is that the stag must be cooperatively hunted, so if one player attempts to hunt the stag, while the other hunts the rabbit, the stag hunter will totally fail, for a payoff of 0, whereas the rabbit-hunter will succeed, for a payoff of 1. The game has two equilibria, (stag, stag) and (rabbit, rabbit), because a player's optimal strategy depends on his expectation on what the other player will do. If one hunter trusts that the other will hunt the stag,  he should hunt the stag; however if he thinks  the other will hunt the rabbit, he too will   hunt the rabbit. This game is used as an analogy for social cooperation, since much of the benefit that people gain in society depends upon people cooperating and implicitly trusting one another to act in a manner corresponding with cooperation.
  
  
  Driving on a road against an oncoming car, and having to choose either to swerve on the left or to swerve on the right of the road, is also a coordination game. For example, with payoffs 10 meaning no crash and 0 meaning a crash, the coordination game can be defined with the following payoff matrix:
  
  
  The driving game
  
  
  Player 1 strategy
  
  Player 2 strategy
  
  
  Drive on the left
  
  Drive on the right
  
  
  Drive on the left
  
   1010
  
   00
  
  
  Drive on the right
  
   00
  
   1010
  
  In this case there are two pure-strategy Nash equilibria, when both choose to either drive on the left or on the right. If we admit mixed strategies (where a pure strategy is chosen at random, subject to some fixed probability), then there are three Nash equilibria for the same case: two we have seen from the pure-strategy form, where the probabilities are (0%, 100%) for player one, (0%, 100%) for player two; and (100%, 0%) for player one, (100%, 0%) for player two respectively. We add another where the probabilities for each player are (50%, 50%).
  
  
  Network traffic[edit]
  See also: Braess's paradox
    Sample network graph. Values on edges are the travel time experienced by a 'car' traveling down that edge. x is the number of cars traveling via that edge.
  An application of Nash equilibria is in determining the expected flow of traffic in a network. Consider the graph on the right. If we assume that there are x "cars" traveling from A to D, what is the expected distribution of traffic in the network?
  This situation can be modeled as a "game" where every traveler has a choice of 3 strategies, where each strategy is a route from A to D (one of ABD, ABCD, or ACD). The "payoff" of each strategy is the travel time of each route. In the graph on the right, a car travelling via ABD experiences travel time of (1+x/100)+2, where x is the number of cars traveling on edge AB. Thus, payoffs for any given strategy depend on the choices of the other players, as is usual. However, the goal, in this case, is to minimize travel time, not maximize it. Equilibrium will occur when the time on all paths is exactly the same. When that happens, no single driver has any incentive to switch routes, since it can only add to their travel time. For the graph on the right, if, for example, 100 cars are travelling from A to D, then equilibrium will occur when 25 drivers travel via ABD, 50 via ABCD, and 25 via ACD. Every driver now has a total travel time of 3.75 (to see this, note that a total of 75 cars take the AB edge, and likewise, 75 cars take the CD edge).
  Notice that this distribution is not, actually, socially optimal. If the 100 cars agreed that 50 travel via ABD and the other 50 through ACD, then travel time for any single car would actually be 3.5, which is less than 3.75. This is also the Nash equilibrium if the path between B and C is removed, which means that adding another possible route can decrease the efficiency of the system, a phenomenon known as Braess's paradox.
  
  Competition game[edit]
  
  A competition game
  
  
  Player 1 strategy
  
  Player 2 strategy
  
  
  Choose "0"
  
  Choose "1"
  
  Choose "2"
  
  Choose "3"
  
  
  Choose "0"
  
  0, 0
  
  2, −2
  
  2, −2
  
  2, −2
  
  
  Choose "1"
  
  −2, 2
  
  1, 1
  
  3, −1
  
  3, −1
  
  
  Choose "2"
  
  −2, 2
  
  −1, 3
  
  2, 2
  
  4, 0
  
  
  Choose "3"
  
  −2, 2
  
  −1, 3
  
  0, 4
  
  3, 3
  
  This can be illustrated by a two-player game in which both players simultaneously choose an integer from 0 to 3 and they both win the smaller of the two numbers in points. In addition, if one player chooses a larger number than the other, then they have to give up two points to the other.
  This game has a unique pure-strategy Nash equilibrium: both players choosing 0 (highlighted in light red). Any other strategy can be improved by a player switching their number to one less than that of the other player. In the adjacent table, if the game begins at the green square, it is in player 1's interest to move to the purple square and it is in player 2's interest to move to the blue square. Although it would not fit the definition of a competition game, if the game is modified so that the two players win the named amount if they both choose the same number, and otherwise win nothing, then there are 4 Nash equilibria: (0,0), (1,1), (2,2), and (3,3).
  
  Nash equilibria in a payoff matrix[edit]
  There is an easy numerical way to identify Nash equilibria on a payoff matrix. It is especially helpful in two-person games where players have more than two strategies. In this case formal analysis may become too long. This rule does not apply to the case where mixed (stochastic) strategies are of interest. The rule goes as follows: if the first payoff number, in the payoff pair of the cell, is the maximum of the column of the cell and if the second number is the maximum of the row of the cell - then the cell represents a Nash equilibrium.
  
  
  A payoff matrix – Nash equilibria in bold
  
  
  Player 1 strategy
  
  Player 2 strategy
  
  
  Option A
  
  Option B
  
  Option C
  
  
  Option A
  
  0, 0
  
  25, 40
  
  5, 10
  
  
  Option B
  
  40, 25
  
  0, 0
  
  5, 15
  
  
  Option C
  
  10, 5
  
  15, 5
  
  10, 10
  
  We can apply this rule to a 3×3 matrix:
  Using the rule, we can very quickly (much faster than with formal analysis) see that the Nash equilibria cells are (B,A), (A,B), and (C,C). Indeed, for cell (B,A) 40 is the maximum of the first column and 25 is the maximum of the second row. For (A,B) 25 is the maximum of the second column and 40 is the maximum of the first row. Same for cell (C,C). For other cells, either one or both of the duplet members are not the maximum of the corresponding rows and columns.
  This said, the actual mechanics of finding equilibrium cells is obvious: find the maximum of a column and check if the second member of the pair is the maximum of the row. If these conditions are met, the cell represents a Nash equilibrium. Check all columns this way to find all NE cells. An N×N matrix may have between 0 and N×N pure-strategy Nash equilibria.
  
  
  Stability[edit]
  The concept of stability, useful in the analysis of many kinds of equilibria, can also be applied to Nash equilibria.
  A Nash equilibrium for a mixed-strategy game is stable if a small change (specifically, an infinitesimal change) in probabilities for one player leads to a situation where two conditions hold:
  
  the player who did not change has no better strategy in the new circumstance
  the player who did change is now playing with a strictly worse strategy.
  If these cases are both met, then a player with the small change in their mixed strategy will return immediately to the Nash equilibrium. The equilibrium is said to be stable. If condition one does not hold then the equilibrium is unstable. If only condition one holds then there are likely to be an infinite number of optimal strategies for the player who changed.
  In the "driving game" example above there are both stable and unstable equilibria. The equilibria involving mixed strategies with 100% probabilities are stable. If either player changes their probabilities slightly, they will be both at a disadvantage, and their opponent will have no reason to change their strategy in turn. The (50%,50%) equilibrium is unstable. If either player changes their probabilities (which would neither benefit or damage the expectation of the player who did the change, if the other player's mixed strategy is still (50%,50%)), then the other player immediately has a better strategy at either (0%, 100%) or (100%, 0%).
  Stability is crucial in practical applications of Nash equilibria, since the mixed strategy of each player is not perfectly known, but has to be inferred from statistical distribution of their actions in the game. In this case unstable equilibria are very unlikely to arise in practice, since any minute change in the proportions of each strategy seen will lead to a change in strategy and the breakdown of the equilibrium.
  The Nash equilibrium defines stability only in terms of unilateral deviations. In cooperative games such a concept is not convincing enough. Strong Nash equilibrium allows for deviations by every conceivable coalition.[17] Formally, a strong Nash equilibrium is a Nash equilibrium in which no coalition, taking the actions of its complements as given, can cooperatively deviate in a way that benefits all of its members.[18] However, the strong Nash concept is sometimes perceived as too "strong" in that the environment allows for unlimited private communication. In fact, strong Nash equilibrium has to be Pareto efficient. As a result of these requirements, strong Nash is too rare to be useful in many branches of game theory. However, in games such as elections with many more players than possible outcomes, it can be more common than a stable equilibrium.
  A refined Nash equilibrium known as coalition-proof Nash equilibrium (CPNE)[17] occurs when players cannot do better even if they are allowed to communicate and make "self-enforcing" agreement to deviate. Every correlated strategy supported by iterated strict dominance and on the Pareto frontier is a CPNE.[19]  Further, it is possible for a game to have a Nash equilibrium that is resilient against coalitions less than a specified size, k. CPNE is related to the theory of the core.
  Finally in the eighties, building with great depth on such ideas Mertens-stable equilibria were introduced as a solution concept. Mertens stable equilibria satisfy both forward induction and backward induction. In a game theory context stable equilibria now usually refer to Mertens stable equilibria.
  
  Occurrence[edit]
  If a game has a unique Nash equilibrium and is played among players under certain conditions, then the NE strategy set will be adopted. Sufficient conditions to guarantee that the Nash equilibrium is played are:
  
  The players all will do their utmost to maximize their expected payoff as described by the game.
  The players are flawless in execution.
  The players have sufficient intelligence to deduce the solution.
  The players know the planned equilibrium strategy of all of the other players.
  The players believe that a deviation in their own strategy will not cause deviations by any other players.
  There is common knowledge that all players meet these conditions, including this one. So, not only must each player know the other players meet the conditions, but also they must know that they all know that they meet them, and know that they know that they know that they meet them, and so on.
  Where the conditions are not met[edit]
  Examples of game theory problems in which these conditions are not met:
  
  The first condition is not met if the game does not correctly describe the quantities a player wishes to maximize. In this case there is no particular reason for that player to adopt an equilibrium strategy. For instance, the prisoner's dilemma is not a dilemma if either player is happy to be jailed indefinitely.
  Intentional or accidental imperfection in execution. For example, a computer capable of flawless logical play facing a second flawless computer will result in equilibrium. Introduction of imperfection will lead to its disruption either through loss to the player who makes the mistake, or through negation of the common knowledge criterion leading to possible victory for the player. (An example would be a player suddenly putting the car into reverse in the game of chicken, ensuring a no-loss no-win scenario).
  In many cases, the third condition is not met because, even though the equilibrium must exist, it is unknown due to the complexity of the game, for instance in Chinese chess.[20] Or, if known, it may not be known to all players, as when playing tic-tac-toe with a small child who desperately wants to win (meeting the other criteria).
  The criterion of common knowledge may not be met even if all players do, in fact, meet all the other criteria. Players wrongly distrusting each other's rationality may adopt counter-strategies to expected irrational play on their opponents’ behalf. This is a major consideration in "chicken" or an arms race, for example.
  Where the conditions are met[edit]
  In his Ph.D. dissertation, John Nash proposed two interpretations of his equilibrium concept, with the objective of showing how equilibrium points can be connected with observable phenomenon.
  
  .mw-parser-output .templatequote{overflow:hidden;margin:1em 0;padding:0 40px}.mw-parser-output .templatequote .templatequotecite{line-height:1.5em;text-align:left;padding-left:1.6em;margin-top:0}(...) One interpretation is rationalistic: if we assume that players are rational, know the full structure of the game, the game is played just once, and there is just one Nash equilibrium, then players will play according to that equilibrium. 
  This idea was formalized by R. Aumann and A. Brandenburger, 1995, Epistemic Conditions for Nash Equilibrium, Econometrica, 63, 1161-1180 who interpreted each player's mixed strategy as a conjecture about the behaviour of other players and have shown that if the game and the rationality of players is mutually known and these conjectures are commonly known, then the conjectures must be a Nash equilibrium (a common prior assumption is needed for this result in general, but not in the case of two players. In this case, the conjectures need only be mutually known).
  A second interpretation, that Nash referred to by the mass action interpretation, is less demanding on players:
  
  [i]t is unnecessary to assume that the participants have full knowledge of the total structure of the game, or the ability and inclination to go through any complex reasoning processes. What is assumed is that there is a population of participants for each position in the game, which will be played throughout time by participants drawn at random from the different populations. If there is a stable average frequency with which each pure strategy is employed by the average member of the appropriate population, then this stable average frequency constitutes a mixed strategy Nash equilibrium.
  For a formal result along these lines, see Kuhn, H. and et al., 1996, "The Work of John Nash in Game Theory," Journal of Economic Theory, 69, 153–185.
  Due to the limited conditions in which NE can actually be observed, they are rarely treated as a guide to day-to-day behaviour, or observed in practice in human negotiations. However, as a theoretical concept in economics and evolutionary biology, the NE has explanatory power. The payoff in economics is utility (or sometimes money), and in evolutionary biology is gene transmission; both are the fundamental bottom line of survival. Researchers who apply games theory in these fields claim that strategies failing to maximize these for whatever reason will be competed out of the market or environment, which are ascribed the ability to test all strategies. This conclusion is drawn from the "stability" theory above. In these situations the assumption that the strategy observed is actually a NE has often been borne out by research.[21]
  
  NE and non-credible threats[edit]
    Extensive and Normal form illustrations that show the difference between SPNE and other NE. The blue equilibrium is not subgame perfect because player two makes a non-credible threat at 2(2) to be unkind (U).
  The Nash equilibrium is a superset of the subgame perfect Nash equilibrium. The subgame perfect equilibrium in addition to the Nash equilibrium requires that the strategy also is a Nash equilibrium in every subgame of that game. This eliminates all non-credible threats, that is, strategies that contain non-rational moves in order to make the counter-player change their strategy.
  The image to the right shows a simple sequential game that illustrates the issue with subgame imperfect Nash equilibria. In this game player one chooses left(L) or right(R), which is followed by player two being called upon to be kind (K) or unkind (U) to player one, However, player two only stands to gain from being unkind if player one goes left. If player one goes right the rational player two would de facto be kind to her/him in that subgame. However, The non-credible threat of being unkind at 2(2) is still part of the blue (L, (U,U)) Nash equilibrium. Therefore, if rational behavior can be expected by both parties the subgame perfect Nash equilibrium may be a more meaningful solution concept when such dynamic inconsistencies arise.
  
  Proof of existence[edit]
  Proof using the Kakutani fixed-point theorem[edit]
  Nash's original proof (in his thesis) used Brouwer's fixed-point theorem (e.g., see below for a variant). We give a simpler proof via the Kakutani fixed-point theorem, following Nash's 1950 paper (he credits David Gale with the observation that such a simplification is possible).
  To prove the existence of a Nash equilibrium, let 
    
      
        
          
            r
            
              i
            
          
          (
          
            σ
            
              −
              i
            
          
          )
        
      
      {\displaystyle r_{i}(\sigma _{-i})}
    
   be the best response of player i to the strategies of all other players.
  
  
    
      
        
          
            r
            
              i
            
          
          (
          
            σ
            
              −
              i
            
          
          )
          =
          
            
              
                a
                r
                g
                
                m
                a
                x
              
              
                σ
                
                  i
                
              
            
          
          ⁡
          
            u
            
              i
            
          
          (
          
            σ
            
              i
            
          
          ,
          
            σ
            
              −
              i
            
          
          )
        
      
      {\displaystyle r_{i}(\sigma _{-i})=\mathop {\underset {\sigma _{i}}{\operatorname {arg\,max} }} u_{i}(\sigma _{i},\sigma _{-i})}
    
  
  Here, 
    
      
        
          σ
          ∈
          Σ
        
      
      {\displaystyle \sigma \in \Sigma }
    
  , where 
    
      
        
          Σ
          =
          
            Σ
            
              i
            
          
          ×
          
            Σ
            
              −
              i
            
          
        
      
      {\displaystyle \Sigma =\Sigma _{i}\times \Sigma _{-i}}
    
  , is a mixed-strategy profile in the set of all mixed strategies and 
    
      
        
          
            u
            
              i
            
          
        
      
      {\displaystyle u_{i}}
    
   is the payoff function for player i. Define a set-valued function 
    
      
        
          r
          :
          Σ
          →
          
            2
            
              Σ
            
          
        
      
      {\displaystyle r\colon \Sigma \rightarrow 2^{\Sigma }}
    
   such that 
    
      
        
          r
          =
          
            r
            
              i
            
          
          (
          
            σ
            
              −
              i
            
          
          )
          ×
          
            r
            
              −
              i
            
          
          (
          
            σ
            
              i
            
          
          )
        
      
      {\displaystyle r=r_{i}(\sigma _{-i})\times r_{-i}(\sigma _{i})}
    
  . The existence of a Nash equilibrium is equivalent to 
    
      
        
          r
        
      
      {\displaystyle r}
    
   having a fixed point.
  Kakutani's fixed point theorem guarantees the existence of a fixed point if the following four conditions are satisfied.
  
  
    
      
        
          Σ
        
      
      {\displaystyle \Sigma }
    
   is compact, convex, and nonempty.
  
    
      
        
          r
          (
          σ
          )
        
      
      {\displaystyle r(\sigma )}
    
   is nonempty.
  
    
      
        
          r
          (
          σ
          )
        
      
      {\displaystyle r(\sigma )}
    
   is upper hemicontinuous
  
    
      
        
          r
          (
          σ
          )
        
      
      {\displaystyle r(\sigma )}
    
   is convex.
  Condition 1. is satisfied from the fact that 
    
      
        
          Σ
        
      
      {\displaystyle \Sigma }
    
   is a simplex and thus compact. Convexity follows from players' ability to mix strategies. 
    
      
        
          Σ
        
      
      {\displaystyle \Sigma }
    
   is nonempty as long as players have strategies.
  Condition 2. and 3. are satisfied by way of Berge's maximum theorem. Because 
    
      
        
          
            u
            
              i
            
          
        
      
      {\displaystyle u_{i}}
    
   is continuous and compact, 
    
      
        
          r
          (
          
            σ
            
              i
            
          
          )
        
      
      {\displaystyle r(\sigma _{i})}
    
   is non-empty and upper hemicontinuous.
  Condition 4. is satisfied as a result of mixed strategies. Suppose  
    
      
        
          
            σ
            
              i
            
          
          ,
          
            σ
            
              i
            
            ′
          
          ∈
          r
          (
          
            σ
            
              −
              i
            
          
          )
        
      
      {\displaystyle \sigma _{i},\sigma '_{i}\in r(\sigma _{-i})}
    
  , then  
    
      
        
          λ
          
            σ
            
              i
            
          
          +
          (
          1
          −
          λ
          )
          
            σ
            
              i
            
            ′
          
          ∈
          r
          (
          
            σ
            
              −
              i
            
          
          )
        
      
      {\displaystyle \lambda \sigma _{i}+(1-\lambda )\sigma '_{i}\in r(\sigma _{-i})}
    
  . i.e. if two strategies maximize payoffs, then a mix between the two strategies will yield the same payoff.
  Therefore, there exists a fixed point in  
    
      
        
          r
        
      
      {\displaystyle r}
    
   and a Nash equilibrium.[22]
  When Nash made this point to John von Neumann in 1949, von Neumann famously dismissed it with the words, "That's trivial, you know. That's just a fixed-point theorem." (See Nasar, 1998, p. 94.)
  
  Alternate proof using the Brouwer fixed-point theorem[edit]
  We have a game 
    
      
        
          G
          =
          (
          N
          ,
          A
          ,
          u
          )
        
      
      {\displaystyle G=(N,A,u)}
    
   where 
    
      
        
          N
        
      
      {\displaystyle N}
    
   is the number of players and 
    
      
        
          A
          =
          
            A
            
              1
            
          
          ×
          ⋯
          ×
          
            A
            
              N
            
          
        
      
      {\displaystyle A=A_{1}\times \cdots \times A_{N}}
    
   is the action set for the players. All of the action sets 
    
      
        
          
            A
            
              i
            
          
        
      
      {\displaystyle A_{i}}
    
   are finite. Let 
    
      
        
          Δ
          =
          
            Δ
            
              1
            
          
          ×
          ⋯
          ×
          
            Δ
            
              N
            
          
        
      
      {\displaystyle \Delta =\Delta _{1}\times \cdots \times \Delta _{N}}
    
   denote the set of mixed strategies for the players. The finiteness of the 
    
      
        
          
            A
            
              i
            
          
        
      
      {\displaystyle A_{i}}
    
  s ensures the compactness of 
    
      
        
          Δ
        
      
      {\displaystyle \Delta }
    
  .
  We can now define the gain functions. For a mixed strategy 
    
      
        
          σ
          ∈
          Δ
        
      
      {\displaystyle \sigma \in \Delta }
    
  , we let the gain for player 
    
      
        
          i
        
      
      {\displaystyle i}
    
   on action 
    
      
        
          a
          ∈
          
            A
            
              i
            
          
        
      
      {\displaystyle a\in A_{i}}
    
   be
  
  
    
      
        
          
            
              Gain
            
            
              i
            
          
          (
          σ
          ,
          a
          )
          =
          max
          {
          0
          ,
          
            u
            
              i
            
          
          (
          a
          ,
          
            σ
            
              −
              i
            
          
          )
          −
          
            u
            
              i
            
          
          (
          
            σ
            
              i
            
          
          ,
          
            σ
            
              −
              i
            
          
          )
          }
          .
        
      
      {\displaystyle {\text{Gain}}_{i}(\sigma ,a)=\max\{0,u_{i}(a,\sigma _{-i})-u_{i}(\sigma _{i},\sigma _{-i})\}.}
    
  
  The gain function represents the benefit a player gets by unilaterally changing their strategy. We now define 
    
      
        
          g
          =
          (
          
            g
            
              1
            
          
          ,
          …
          ,
          
            g
            
              N
            
          
          )
        
      
      {\displaystyle g=(g_{1},\dotsc ,g_{N})}
    
   where
  
  
    
      
        
          
            g
            
              i
            
          
          (
          σ
          )
          (
          a
          )
          =
          
            σ
            
              i
            
          
          (
          a
          )
          +
          
            
              Gain
            
            
              i
            
          
          (
          σ
          ,
          a
          )
        
      
      {\displaystyle g_{i}(\sigma )(a)=\sigma _{i}(a)+{\text{Gain}}_{i}(\sigma ,a)}
    
  
  for 
    
      
        
          σ
          ∈
          Δ
          ,
          a
          ∈
          
            A
            
              i
            
          
        
      
      {\displaystyle \sigma \in \Delta ,a\in A_{i}}
    
  . We see that
  
  
    
      
        
          
            ∑
            
              a
              ∈
              
                A
                
                  i
                
              
            
          
          
            g
            
              i
            
          
          (
          σ
          )
          (
          a
          )
          =
          
            ∑
            
              a
              ∈
              
                A
                
                  i
                
              
            
          
          
            σ
            
              i
            
          
          (
          a
          )
          +
          
            
              Gain
            
            
              i
            
          
          (
          σ
          ,
          a
          )
          =
          1
          +
          
            ∑
            
              a
              ∈
              
                A
                
                  i
                
              
            
          
          
            
              Gain
            
            
              i
            
          
          (
          σ
          ,
          a
          )
          >
          0.
        
      
      {\displaystyle \sum _{a\in A_{i}}g_{i}(\sigma )(a)=\sum _{a\in A_{i}}\sigma _{i}(a)+{\text{Gain}}_{i}(\sigma ,a)=1+\sum _{a\in A_{i}}{\text{Gain}}_{i}(\sigma ,a)>0.}
    
  
  Next we define:
  
  
    
      
        
          
            
              {
              
                
                  
                    f
                    =
                    (
                    
                      f
                      
                        1
                      
                    
                    ,
                    ⋯
                    ,
                    
                      f
                      
                        N
                      
                    
                    )
                    :
                    Δ
                    →
                    Δ
                  
                
                
                  
                    
                      f
                      
                        i
                      
                    
                    (
                    σ
                    )
                    (
                    a
                    )
                    =
                    
                      
                        
                          
                            g
                            
                              i
                            
                          
                          (
                          σ
                          )
                          (
                          a
                          )
                        
                        
                          
                            ∑
                            
                              b
                              ∈
                              
                                A
                                
                                  i
                                
                              
                            
                          
                          
                            g
                            
                              i
                            
                          
                          (
                          σ
                          )
                          (
                          b
                          )
                        
                      
                    
                  
                  
                    a
                    ∈
                    
                      A
                      
                        i
                      
                    
                  
                
              
              
            
          
        
      
      {\displaystyle {\begin{cases}f=(f_{1},\cdots ,f_{N}):\Delta \to \Delta \\f_{i}(\sigma )(a)={\frac {g_{i}(\sigma )(a)}{\sum _{b\in A_{i}}g_{i}(\sigma )(b)}}&a\in A_{i}\end{cases}}}
    
  
  It is easy to see that each 
    
      
        
          
            f
            
              i
            
          
        
      
      {\displaystyle f_{i}}
    
   is a valid mixed strategy in 
    
      
        
          
            Δ
            
              i
            
          
        
      
      {\displaystyle \Delta _{i}}
    
  . It is also easy to check that each 
    
      
        
          
            f
            
              i
            
          
        
      
      {\displaystyle f_{i}}
    
   is a continuous function of 
    
      
        
          σ
        
      
      {\displaystyle \sigma }
    
  , and hence 
    
      
        
          f
        
      
      {\displaystyle f}
    
   is a continuous function. As the cross product of a finite number of compact convex sets, 
    
      
        
          Δ
        
      
      {\displaystyle \Delta }
    
   is also compact and convex. Applying the Brouwer fixed point theorem to 
    
      
        
          f
        
      
      {\displaystyle f}
    
   and 
    
      
        
          Δ
        
      
      {\displaystyle \Delta }
    
   we conclude that 
    
      
        
          f
        
      
      {\displaystyle f}
    
   has a fixed point in 
    
      
        
          Δ
        
      
      {\displaystyle \Delta }
    
  , call it 
    
      
        
          
            σ
            
              ∗
            
          
        
      
      {\displaystyle \sigma ^{*}}
    
  . We claim that 
    
      
        
          
            σ
            
              ∗
            
          
        
      
      {\displaystyle \sigma ^{*}}
    
   is a Nash equilibrium in 
    
      
        
          G
        
      
      {\displaystyle G}
    
  . For this purpose, it suffices to show that
  
  
    
      
        
          ∀
          i
          ∈
          {
          1
          ,
          ⋯
          ,
          N
          }
          ,
          ∀
          a
          ∈
          
            A
            
              i
            
          
          :
          
          
            
              Gain
            
            
              i
            
          
          (
          
            σ
            
              ∗
            
          
          ,
          a
          )
          =
          0.
        
      
      {\displaystyle \forall i\in \{1,\cdots ,N\},\forall a\in A_{i}:\quad {\text{Gain}}_{i}(\sigma ^{*},a)=0.}
    
  
  This simply states that each player gains no benefit by unilaterally changing their strategy, which is exactly the necessary condition for a Nash equilibrium.
  Now assume that the gains are not all zero. Therefore, 
    
      
        
          ∃
          i
          ∈
          {
          1
          ,
          ⋯
          ,
          N
          }
          ,
        
      
      {\displaystyle \exists i\in \{1,\cdots ,N\},}
    
   and 
    
      
        
          a
          ∈
          
            A
            
              i
            
          
        
      
      {\displaystyle a\in A_{i}}
    
   such that 
    
      
        
          
            
              Gain
            
            
              i
            
          
          (
          
            σ
            
              ∗
            
          
          ,
          a
          )
          >
          0
        
      
      {\displaystyle {\text{Gain}}_{i}(\sigma ^{*},a)>0}
    
  . Note then that
  
  
    
      
        
          
            ∑
            
              a
              ∈
              
                A
                
                  i
                
              
            
          
          
            g
            
              i
            
          
          (
          
            σ
            
              ∗
            
          
          ,
          a
          )
          =
          1
          +
          
            ∑
            
              a
              ∈
              
                A
                
                  i
                
              
            
          
          
            
              Gain
            
            
              i
            
          
          (
          
            σ
            
              ∗
            
          
          ,
          a
          )
          >
          1.
        
      
      {\displaystyle \sum _{a\in A_{i}}g_{i}(\sigma ^{*},a)=1+\sum _{a\in A_{i}}{\text{Gain}}_{i}(\sigma ^{*},a)>1.}
    
  
  So let
  
  
    
      
        
          C
          =
          
            ∑
            
              a
              ∈
              
                A
                
                  i
                
              
            
          
          
            g
            
              i
            
          
          (
          
            σ
            
              ∗
            
          
          ,
          a
          )
          .
        
      
      {\displaystyle C=\sum _{a\in A_{i}}g_{i}(\sigma ^{*},a).}
    
  
  Also we shall denote 
    
      
        
          
            Gain
          
          (
          i
          ,
          ⋅
          )
        
      
      {\displaystyle {\text{Gain}}(i,\cdot )}
    
   as the gain vector indexed by actions in 
    
      
        
          
            A
            
              i
            
          
        
      
      {\displaystyle A_{i}}
    
  . Since 
    
      
        
          
            σ
            
              ∗
            
          
        
      
      {\displaystyle \sigma ^{*}}
    
   is the fixed point we have:
  
  
    
      
        
          
            
              
                
                  
                    σ
                    
                      ∗
                    
                  
                  =
                  f
                  (
                  
                    σ
                    
                      ∗
                    
                  
                  )
                
                
                  
                  ⇒
                  
                    σ
                    
                      i
                    
                    
                      ∗
                    
                  
                  =
                  
                    f
                    
                      i
                    
                  
                  (
                  
                    σ
                    
                      ∗
                    
                  
                  )
                
              
              
                
                
                  
                  ⇒
                  
                    σ
                    
                      i
                    
                    
                      ∗
                    
                  
                  =
                  
                    
                      
                        
                          g
                          
                            i
                          
                        
                        (
                        
                          σ
                          
                            ∗
                          
                        
                        )
                      
                      
                        
                          ∑
                          
                            a
                            ∈
                            
                              A
                              
                                i
                              
                            
                          
                        
                        
                          g
                          
                            i
                          
                        
                        (
                        
                          σ
                          
                            ∗
                          
                        
                        )
                        (
                        a
                        )
                      
                    
                  
                
              
              
                
                
                  
                  ⇒
                  
                    σ
                    
                      i
                    
                    
                      ∗
                    
                  
                  =
                  
                    
                      1
                      C
                    
                  
                  
                    (
                    
                      
                        σ
                        
                          i
                        
                        
                          ∗
                        
                      
                      +
                      
                        
                          Gain
                        
                        
                          i
                        
                      
                      (
                      
                        σ
                        
                          ∗
                        
                      
                      ,
                      ⋅
                      )
                    
                    )
                  
                
              
              
                
                
                  
                  ⇒
                  C
                  
                    σ
                    
                      i
                    
                    
                      ∗
                    
                  
                  =
                  
                    σ
                    
                      i
                    
                    
                      ∗
                    
                  
                  +
                  
                    
                      Gain
                    
                    
                      i
                    
                  
                  (
                  
                    σ
                    
                      ∗
                    
                  
                  ,
                  ⋅
                  )
                
              
              
                
                
                  
                  ⇒
                  
                    (
                    
                      C
                      −
                      1
                    
                    )
                  
                  
                    σ
                    
                      i
                    
                    
                      ∗
                    
                  
                  =
                  
                    
                      Gain
                    
                    
                      i
                    
                  
                  (
                  
                    σ
                    
                      ∗
                    
                  
                  ,
                  ⋅
                  )
                
              
              
                
                
                  
                  ⇒
                  
                    σ
                    
                      i
                    
                    
                      ∗
                    
                  
                  =
                  
                    (
                    
                      
                        1
                        
                          C
                          −
                          1
                        
                      
                    
                    )
                  
                  
                    
                      Gain
                    
                    
                      i
                    
                  
                  (
                  
                    σ
                    
                      ∗
                    
                  
                  ,
                  ⋅
                  )
                  .
                
              
            
          
        
      
      {\displaystyle {\begin{aligned}\sigma ^{*}=f(\sigma ^{*})&\Rightarrow \sigma _{i}^{*}=f_{i}(\sigma ^{*})\\&\Rightarrow \sigma _{i}^{*}={\frac {g_{i}(\sigma ^{*})}{\sum _{a\in A_{i}}g_{i}(\sigma ^{*})(a)}}\\[6pt]&\Rightarrow \sigma _{i}^{*}={\frac {1}{C}}\left(\sigma _{i}^{*}+{\text{Gain}}_{i}(\sigma ^{*},\cdot )\right)\\[6pt]&\Rightarrow C\sigma _{i}^{*}=\sigma _{i}^{*}+{\text{Gain}}_{i}(\sigma ^{*},\cdot )\\&\Rightarrow \left(C-1\right)\sigma _{i}^{*}={\text{Gain}}_{i}(\sigma ^{*},\cdot )\\&\Rightarrow \sigma _{i}^{*}=\left({\frac {1}{C-1}}\right){\text{Gain}}_{i}(\sigma ^{*},\cdot ).\end{aligned}}}
    
  
  Since 
    
      
        
          C
          >
          1
        
      
      {\displaystyle C>1}
    
   we have that 
    
      
        
          
            σ
            
              i
            
            
              ∗
            
          
        
      
      {\displaystyle \sigma _{i}^{*}}
    
   is some positive scaling of the vector 
    
      
        
          
            
              Gain
            
            
              i
            
          
          (
          
            σ
            
              ∗
            
          
          ,
          ⋅
          )
        
      
      {\displaystyle {\text{Gain}}_{i}(\sigma ^{*},\cdot )}
    
  . Now we claim that
  
  
    
      
        
          ∀
          a
          ∈
          
            A
            
              i
            
          
          :
          
          
            σ
            
              i
            
            
              ∗
            
          
          (
          a
          )
          (
          
            u
            
              i
            
          
          (
          
            a
            
              i
            
          
          ,
          
            σ
            
              −
              i
            
            
              ∗
            
          
          )
          −
          
            u
            
              i
            
          
          (
          
            σ
            
              i
            
            
              ∗
            
          
          ,
          
            σ
            
              −
              i
            
            
              ∗
            
          
          )
          )
          =
          
            σ
            
              i
            
            
              ∗
            
          
          (
          a
          )
          
            
              Gain
            
            
              i
            
          
          (
          
            σ
            
              ∗
            
          
          ,
          a
          )
        
      
      {\displaystyle \forall a\in A_{i}:\quad \sigma _{i}^{*}(a)(u_{i}(a_{i},\sigma _{-i}^{*})-u_{i}(\sigma _{i}^{*},\sigma _{-i}^{*}))=\sigma _{i}^{*}(a){\text{Gain}}_{i}(\sigma ^{*},a)}
    
  
  To see this, we first note that if 
    
      
        
          
            
              Gain
            
            
              i
            
          
          (
          
            σ
            
              ∗
            
          
          ,
          a
          )
          >
          0
        
      
      {\displaystyle {\text{Gain}}_{i}(\sigma ^{*},a)>0}
    
   then this is true by definition of the gain function.  Now assume that 
    
      
        
          
            
              Gain
            
            
              i
            
          
          (
          
            σ
            
              ∗
            
          
          ,
          a
          )
          =
          0
        
      
      {\displaystyle {\text{Gain}}_{i}(\sigma ^{*},a)=0}
    
  . By our previous statements we have that
  
  
    
      
        
          
            σ
            
              i
            
            
              ∗
            
          
          (
          a
          )
          =
          
            (
            
              
                1
                
                  C
                  −
                  1
                
              
            
            )
          
          
            
              Gain
            
            
              i
            
          
          (
          
            σ
            
              ∗
            
          
          ,
          a
          )
          =
          0
        
      
      {\displaystyle \sigma _{i}^{*}(a)=\left({\frac {1}{C-1}}\right){\text{Gain}}_{i}(\sigma ^{*},a)=0}
    
  
  and so the left term is zero, giving us that the entire expression is 
    
      
        
          0
        
      
      {\displaystyle 0}
    
   as needed.
  So we finally have that
  
  
    
      
        
          
            
              
                
                  0
                
                
                  
                  =
                  
                    u
                    
                      i
                    
                  
                  (
                  
                    σ
                    
                      i
                    
                    
                      ∗
                    
                  
                  ,
                  
                    σ
                    
                      −
                      i
                    
                    
                      ∗
                    
                  
                  )
                  −
                  
                    u
                    
                      i
                    
                  
                  (
                  
                    σ
                    
                      i
                    
                    
                      ∗
                    
                  
                  ,
                  
                    σ
                    
                      −
                      i
                    
                    
                      ∗
                    
                  
                  )
                
              
              
                
                
                  
                  =
                  
                    (
                    
                      
                        ∑
                        
                          a
                          ∈
                          
                            A
                            
                              i
                            
                          
                        
                      
                      
                        σ
                        
                          i
                        
                        
                          ∗
                        
                      
                      (
                      a
                      )
                      
                        u
                        
                          i
                        
                      
                      (
                      
                        a
                        
                          i
                        
                      
                      ,
                      
                        σ
                        
                          −
                          i
                        
                        
                          ∗
                        
                      
                      )
                    
                    )
                  
                  −
                  
                    u
                    
                      i
                    
                  
                  (
                  
                    σ
                    
                      i
                    
                    
                      ∗
                    
                  
                  ,
                  
                    σ
                    
                      −
                      i
                    
                    
                      ∗
                    
                  
                  )
                
              
              
                
                
                  
                  =
                  
                    ∑
                    
                      a
                      ∈
                      
                        A
                        
                          i
                        
                      
                    
                  
                  
                    σ
                    
                      i
                    
                    
                      ∗
                    
                  
                  (
                  a
                  )
                  (
                  
                    u
                    
                      i
                    
                  
                  (
                  
                    a
                    
                      i
                    
                  
                  ,
                  
                    σ
                    
                      −
                      i
                    
                    
                      ∗
                    
                  
                  )
                  −
                  
                    u
                    
                      i
                    
                  
                  (
                  
                    σ
                    
                      i
                    
                    
                      ∗
                    
                  
                  ,
                  
                    σ
                    
                      −
                      i
                    
                    
                      ∗
                    
                  
                  )
                  )
                
              
              
                
                
                  
                  =
                  
                    ∑
                    
                      a
                      ∈
                      
                        A
                        
                          i
                        
                      
                    
                  
                  
                    σ
                    
                      i
                    
                    
                      ∗
                    
                  
                  (
                  a
                  )
                  
                    
                      Gain
                    
                    
                      i
                    
                  
                  (
                  
                    σ
                    
                      ∗
                    
                  
                  ,
                  a
                  )
                
                
                
                  
                     by the previous statements 
                  
                
              
              
                
                
                  
                  =
                  
                    ∑
                    
                      a
                      ∈
                      
                        A
                        
                          i
                        
                      
                    
                  
                  
                    (
                    
                      C
                      −
                      1
                    
                    )
                  
                  
                    σ
                    
                      i
                    
                    
                      ∗
                    
                  
                  (
                  a
                  
                    )
                    
                      2
                    
                  
                  >
                  0
                
              
            
          
        
      
      {\displaystyle {\begin{aligned}0&=u_{i}(\sigma _{i}^{*},\sigma _{-i}^{*})-u_{i}(\sigma _{i}^{*},\sigma _{-i}^{*})\\&=\left(\sum _{a\in A_{i}}\sigma _{i}^{*}(a)u_{i}(a_{i},\sigma _{-i}^{*})\right)-u_{i}(\sigma _{i}^{*},\sigma _{-i}^{*})\\&=\sum _{a\in A_{i}}\sigma _{i}^{*}(a)(u_{i}(a_{i},\sigma _{-i}^{*})-u_{i}(\sigma _{i}^{*},\sigma _{-i}^{*}))\\&=\sum _{a\in A_{i}}\sigma _{i}^{*}(a){\text{Gain}}_{i}(\sigma ^{*},a)&&{\text{ by the previous statements }}\\&=\sum _{a\in A_{i}}\left(C-1\right)\sigma _{i}^{*}(a)^{2}>0\end{aligned}}}
    
  
  where the last inequality follows since 
    
      
        
          
            σ
            
              i
            
            
              ∗
            
          
        
      
      {\displaystyle \sigma _{i}^{*}}
    
   is a non-zero vector. But this is a clear contradiction, so all the gains must indeed be zero. Therefore, 
    
      
        
          
            σ
            
              ∗
            
          
        
      
      {\displaystyle \sigma ^{*}}
    
   is a Nash equilibrium for 
    
      
        
          G
        
      
      {\displaystyle G}
    
   as needed.
  
  Computing Nash equilibria[edit]
  If a player A has a dominant strategy 
    
      
        
          
            s
            
              A
            
          
        
      
      {\displaystyle s_{A}}
    
   then there exists a Nash equilibrium in which A plays 
    
      
        
          
            s
            
              A
            
          
        
      
      {\displaystyle s_{A}}
    
  . In the case of two players A and B, there exists a Nash equilibrium in which A plays 
    
      
        
          
            s
            
              A
            
          
        
      
      {\displaystyle s_{A}}
    
   and B plays a best response to 
    
      
        
          
            s
            
              A
            
          
        
      
      {\displaystyle s_{A}}
    
  . If 
    
      
        
          
            s
            
              A
            
          
        
      
      {\displaystyle s_{A}}
    
   is a strictly dominant strategy, A plays 
    
      
        
          
            s
            
              A
            
          
        
      
      {\displaystyle s_{A}}
    
   in all Nash equilibria. If both A and B have strictly dominant strategies, there exists a unique Nash equilibrium in which each plays their strictly dominant strategy.
  In games with mixed-strategy Nash equilibria, the probability of a player choosing any particular (so pure) strategy can be computed by assigning a variable to each strategy that represents a fixed probability for choosing that strategy. In order for a player to be willing to randomize, their expected payoff for each (pure) strategy should be the same. In addition, the sum of the probabilities for each strategy of a particular player should be 1. This creates a system of equations from which the probabilities of choosing each strategy can be derived.[14]
  
  Examples[edit]
  
  Matching pennies
  
  
  Strategy
  
  Player B plays H
  
  Player B plays T
  
  
  Player A plays H
  
  −1, +1
  
  +1, −1
  
  
  Player A plays T
  
  +1, −1
  
  −1, +1
  
  In the matching pennies game, player A loses a point to B if A and B play the same strategy and wins a point from B if they play different strategies. To compute the mixed-strategy Nash equilibrium, assign A the probability p of playing H and (1−p) of playing T, and assign B the probability q of playing H and (1−q) of playing T.
  
  
    
      
        
          
            
              
                
                
                  
                    E
                  
                  [
                  
                    payoff for A playing H
                  
                  ]
                  =
                  (
                  −
                  1
                  )
                  q
                  +
                  (
                  +
                  1
                  )
                  (
                  1
                  −
                  q
                  )
                  =
                  1
                  −
                  2
                  q
                
              
              
                
                
                  
                    E
                  
                  [
                  
                    payoff for A playing T
                  
                  ]
                  =
                  (
                  +
                  1
                  )
                  q
                  +
                  (
                  −
                  1
                  )
                  (
                  1
                  −
                  q
                  )
                  =
                  2
                  q
                  −
                  1
                
              
              
                
                
                  
                    E
                  
                  [
                  
                    payoff for A playing H
                  
                  ]
                  =
                  
                    E
                  
                  [
                  
                    payoff for A playing T
                  
                  ]
                  
                  ⟹
                  
                  1
                  −
                  2
                  q
                  =
                  2
                  q
                  −
                  1
                  
                  ⟹
                  
                  q
                  =
                  1
                  
                    /
                  
                  2
                
              
              
                
                
                  
                    E
                  
                  [
                  
                    payoff for B playing H
                  
                  ]
                  =
                  (
                  +
                  1
                  )
                  p
                  +
                  (
                  −
                  1
                  )
                  (
                  1
                  −
                  p
                  )
                  =
                  2
                  p
                  −
                  1
                
              
              
                
                
                  
                    E
                  
                  [
                  
                    payoff for B playing T
                  
                  ]
                  =
                  (
                  −
                  1
                  )
                  p
                  +
                  (
                  +
                  1
                  )
                  (
                  1
                  −
                  p
                  )
                  =
                  1
                  −
                  2
                  p
                
              
              
                
                
                  
                    E
                  
                  [
                  
                    payoff for B playing H
                  
                  ]
                  =
                  
                    E
                  
                  [
                  
                    payoff for B playing T
                  
                  ]
                  
                  ⟹
                  
                  2
                  p
                  −
                  1
                  =
                  1
                  −
                  2
                  p
                  
                  ⟹
                  
                  p
                  =
                  1
                  
                    /
                  
                  2
                
              
            
          
        
      
      {\displaystyle {\begin{aligned}&\mathbb {E} [{\text{payoff for A playing H}}]=(-1)q+(+1)(1-q)=1-2q\\&\mathbb {E} [{\text{payoff for A playing T}}]=(+1)q+(-1)(1-q)=2q-1\\&\mathbb {E} [{\text{payoff for A playing H}}]=\mathbb {E} [{\text{payoff for A playing T}}]\implies 1-2q=2q-1\implies q=1/2\\&\mathbb {E} [{\text{payoff for B playing H}}]=(+1)p+(-1)(1-p)=2p-1\\&\mathbb {E} [{\text{payoff for B playing T}}]=(-1)p+(+1)(1-p)=1-2p\\&\mathbb {E} [{\text{payoff for B playing H}}]=\mathbb {E} [{\text{payoff for B playing T}}]\implies 2p-1=1-2p\implies p=1/2\\\end{aligned}}}
    
  
  Thus a mixed-strategy Nash equilibrium, in this game, is for each player to randomly choose H or T with p = 1/2 and q = 1/2.
  
  Oddness of equilibrium points[edit]
  In 1971, Robert Wilson came up with the Oddness Theorem, [23] which says that "almost all" finite games have a finite and odd number of Nash equilibria. In 1993, Harsanyi published an alternative proof of the result.[24] "Almost all" here means that any game with an infinite or even number of equilibria is very special in the sense that if its payoffs were even slightly randomly perturbed, with probability one it would have an odd number of equilibria instead. 
  
  
  Free Money Game
  
  
  Strategy
  
  Player B votes Yes
  
  Player B votes No
  
  
  Player A votes Yes
  
  1, 1
  
  0, 0
  
  
  Player A votes No
  
  0, 0
  
  0, 0
  
  The prisoner's dilemma, for example, has one equilibrium, while the battle of the sexes has three-- two pure and one mixed, and this remains true even if the payoffs change slightly. The free money game is an example of a "special" game with an even number of equilibria. In it, two players have to both vote "yes" rather than "no" to get a reward and the votes are simultaneous. There are two pure-strategy Nash equilibria, (yes, yes) and (no, no), and no mixed strategy equilibria, because the strategy "yes" weakly dominates "no". "Yes" is as good as "no" regardless of the other player's action, but if there is any chance the other player chooses "yes" then "yes" is the best reply. Under a small random perturbation of the payoffs, however, the probability that any two payoffs would remain tied, whether at 0 or some other number, is vanishingly small, and the game would have either one or  three equilibria instead.
  
  See also[edit]
  .mw-parser-output .div-col{margin-top:0.3em;column-width:30em}.mw-parser-output .div-col-small{font-size:90%}.mw-parser-output .div-col-rules{column-rule:1px solid #aaa}.mw-parser-output .div-col dl,.mw-parser-output .div-col ol,.mw-parser-output .div-col ul{margin-top:0}.mw-parser-output .div-col li,.mw-parser-output .div-col dd{page-break-inside:avoid;break-inside:avoid-column}
  Adjusted winner procedure – Method of fairly dividing property
  Complementarity theory
  Conflict resolution research
  Cooperation – Groups working or acting together
  Equilibrium selection
  Evolutionarily stable strategy – Solution concept in game theory
  Glossary of game theory – List of definitions of terms and concepts used in game theory
  Hotelling's law
  Manipulated Nash equilibrium
  Mexican standoff – Type of confrontation
  Minimax theorem – Gives conditions that guarantee the max–min inequality is also an equality
  Mutual assured destruction – Doctrine of military strategy
  Extended Mathematical Programming for Equilibrium Problems
  Optimum contract and par contract – Bridge scoring terms in the card game contract bridge
  Self-confirming equilibrium
  Solution concept
  Stackelberg competition – Economic model
  Wardrop's principle
  
  Notes[edit]
  .mw-parser-output .reflist{font-size:90%;margin-bottom:0.5em;list-style-type:decimal}.mw-parser-output .reflist .references{font-size:100%;margin-bottom:0;list-style-type:inherit}.mw-parser-output .reflist-columns-2{column-width:30em}.mw-parser-output .reflist-columns-3{column-width:25em}.mw-parser-output .reflist-columns{margin-top:0.3em}.mw-parser-output .reflist-columns ol{margin-top:0}.mw-parser-output .reflist-columns li{page-break-inside:avoid;break-inside:avoid-column}.mw-parser-output .reflist-upper-alpha{list-style-type:upper-alpha}.mw-parser-output .reflist-upper-roman{list-style-type:upper-roman}.mw-parser-output .reflist-lower-alpha{list-style-type:lower-alpha}.mw-parser-output .reflist-lower-greek{list-style-type:lower-greek}.mw-parser-output .reflist-lower-roman{list-style-type:lower-roman}
  
  ^ .mw-parser-output cite.citation{font-style:inherit;word-wrap:break-word}.mw-parser-output .citation q{quotes:"\"""\"""'""'"}.mw-parser-output .citation:target{background-color:rgba(0,127,255,0.133)}.mw-parser-output .id-lock-free a,.mw-parser-output .citation .cs1-lock-free a{background:linear-gradient(transparent,transparent),url("//upload.wikimedia.org/wikipedia/commons/6/65/Lock-green.svg")right 0.1em center/9px no-repeat}.mw-parser-output .id-lock-limited a,.mw-parser-output .id-lock-registration a,.mw-parser-output .citation .cs1-lock-limited a,.mw-parser-output .citation .cs1-lock-registration a{background:linear-gradient(transparent,transparent),url("//upload.wikimedia.org/wikipedia/commons/d/d6/Lock-gray-alt-2.svg")right 0.1em center/9px no-repeat}.mw-parser-output .id-lock-subscription a,.mw-parser-output .citation .cs1-lock-subscription a{background:linear-gradient(transparent,transparent),url("//upload.wikimedia.org/wikipedia/commons/a/aa/Lock-red-alt-2.svg")right 0.1em center/9px no-repeat}.mw-parser-output .cs1-ws-icon a{background:linear-gradient(transparent,transparent),url("//upload.wikimedia.org/wikipedia/commons/4/4c/Wikisource-logo.svg")right 0.1em center/12px no-repeat}.mw-parser-output .cs1-code{color:inherit;background:inherit;border:none;padding:inherit}.mw-parser-output .cs1-hidden-error{display:none;color:#d33}.mw-parser-output .cs1-visible-error{color:#d33}.mw-parser-output .cs1-maint{display:none;color:#3a3;margin-left:0.3em}.mw-parser-output .cs1-format{font-size:95%}.mw-parser-output .cs1-kern-left{padding-left:0.2em}.mw-parser-output .cs1-kern-right{padding-right:0.2em}.mw-parser-output .citation .mw-selflink{font-weight:inherit}Osborne, Martin J.; Rubinstein, Ariel (12 Jul 1994). A Course in Game Theory. Cambridge, MA: MIT. p. 14. ISBN 9780262150415.
  
  ^ Kreps D.M. (1987) "Nash Equilibrium." In: Palgrave Macmillan (eds) The New Palgrave Dictionary of Economics. Palgrave Macmillan, London.
  
  ^ Schelling, Thomas, The Strategy of Conflict, copyright 1960, 1980, Harvard University Press, ISBN 0-674-84031-3.
  
  ^ De Fraja, G.; Oliveira, T.; Zanchi, L. (2010). "Must Try Harder: Evaluating the Role of Effort in Educational Attainment". Review of Economics and Statistics. 92 (3): 577. doi:10.1162/REST_a_00013. hdl:2108/55644. S2CID 57072280.
  
  ^ Ward, H. (1996). "Game Theory and the Politics of Global Warming: The State of Play and Beyond". Political Studies. 44 (5): 850–871. doi:10.1111/j.1467-9248.1996.tb00338.x. S2CID 143728467.,
  
  ^ Thorpe, Robert B.; Jennings, Simon; Dolder, Paul J. (2017). "Risks and benefits of catching pretty good yield in multispecies mixed fisheries". ICES Journal of Marine Science. 74 (8): 2097–2106. doi:10.1093/icesjms/fsx062.,
  
  ^ "Marketing Lessons from Dr. Nash - Andrew Frank". 2015-05-25. Retrieved 2015-08-30.
  
  ^ Chiappori, P. -A.; Levitt, S.; Groseclose, T. (2002). "Testing Mixed-Strategy Equilibria when Players Are Heterogeneous: The Case of Penalty Kicks in Soccer" (PDF). American Economic Review. 92 (4): 1138. CiteSeerX 10.1.1.178.1646. doi:10.1257/00028280260344678.
  
  ^ Djehiche, B.; Tcheukam, A.; Tembine, H. (2017). "A Mean-Field Game of Evacuation in Multilevel Building". IEEE Transactions on Automatic Control. 62 (10): 5154–5169. doi:10.1109/TAC.2017.2679487. ISSN 0018-9286. S2CID 21850096.
  
  ^ Djehiche, Boualem; Tcheukam, Alain; Tembine, Hamidou (2017-09-27). "Mean-Field-Type Games in Engineering". AIMS Electronics and Electrical Engineering. 1: 18–73. arXiv:1605.03281. doi:10.3934/ElectrEng.2017.1.18. S2CID 16055840.
  
  ^ Cournot A. (1838) Researches on the Mathematical Principles of the Theory of Wealth
  
  ^ J. Von Neumann, O. Morgenstern, Theory of Games and Economic Behavior, copyright 1944, 1953, Princeton University Press
  
  ^ Carmona, Guilherme; Podczeck, Konrad (2009). "On the Existence of Pure Strategy Nash Equilibria in Large Games" (PDF). Journal of Economic Theory. 144 (3): 1300–1319. doi:10.1016/j.jet.2008.11.009. hdl:10362/11577. SSRN 882466.
  
  ^ Jump up to: a b von Ahn, Luis. "Preliminaries of Game Theory" (PDF). Archived from the original (PDF) on 2011-10-18. Retrieved 2008-11-07.
  
  ^ "Nash Equilibria". hoylab.cornell.edu. Retrieved 2019-12-08.
  
  ^ MIT OpenCourseWare. 6.254: Game Theory with Engineering Applications, Spring 2010. Lecture 6: Continuous and Discontinuous Games.
  
  ^ Jump up to: a b B. D. Bernheim; B. Peleg; M. D. Whinston (1987), "Coalition-Proof Equilibria I. Concepts", Journal of Economic Theory, 42 (1): 1–12, doi:10.1016/0022-0531(87)90099-8.
  
  ^ Aumann, R. (1959). "Acceptable points in general cooperative n-person games". Contributions to the Theory of Games. Vol. IV. Princeton, N.J.: Princeton University Press. ISBN 978-1-4008-8216-8.
  
  ^ D. Moreno; J. Wooders (1996), "Coalition-Proof Equilibrium" (PDF), Games and Economic Behavior, 17 (1): 80–112, doi:10.1006/game.1996.0095, hdl:10016/4408.
  
  ^ T. L. Turocy, B. Von Stengel, Game Theory, copyright 2001, Texas A&M University,  London School of Economics, pages 141-144. Nash proved that a perfect NE exists for this type of finite extensive form game[citation needed] – it can be represented as a strategy complying with his original conditions for a game with a NE. Such games may not have unique NE, but at least one of the many equilibrium strategies would be played by hypothetical players having perfect knowledge of all 10150 game trees[citation needed].
  
  ^ J. C. Cox, M. Walker, Learning to Play Cournot Duoploy Strategies Archived 2013-12-11 at the Wayback Machine, copyright 1997, Texas A&M University,  University of Arizona, pages 141-144
  
  ^ Fudenburg, Drew; Tirole, Jean (1991). Game Theory. MIT Press. ISBN 978-0-262-06141-4.
  
  ^ Wilson, Robert (1971-07-01). "Computing Equilibria of N-Person Games". SIAM Journal on Applied Mathematics. 21 (1): 80–87. doi:10.1137/0121011. ISSN 0036-1399.
  
  ^ Harsanyi, J. C. (1973-12-01). "Oddness of the Number of Equilibrium Points: A New Proof". International Journal of Game Theory. 2 (1): 235–250. doi:10.1007/BF01737572. ISSN 1432-1270. S2CID 122603890.
  
  
  References[edit]
  Game theory textbooks[edit]
  .mw-parser-output .refbegin{font-size:90%;margin-bottom:0.5em}.mw-parser-output .refbegin-hanging-indents>ul{margin-left:0}.mw-parser-output .refbegin-hanging-indents>ul>li{margin-left:0;padding-left:3.2em;text-indent:-3.2em}.mw-parser-output .refbegin-hanging-indents ul,.mw-parser-output .refbegin-hanging-indents ul li{list-style:none}@media(max-width:720px){.mw-parser-output .refbegin-hanging-indents>ul>li{padding-left:1.6em;text-indent:-1.6em}}.mw-parser-output .refbegin-columns{margin-top:0.3em}.mw-parser-output .refbegin-columns ul{margin-top:0}.mw-parser-output .refbegin-columns li{page-break-inside:avoid;break-inside:avoid-column}
  Binmore, Ken (2007), Playing for Real: A Text on Game Theory, Oxford University Press, ISBN 978-0195300574.
  Dixit, Avinash, Susan Skeath and David Reiley. Games of Strategy. W.W. Norton & Company. (Third edition in 2009.) An undergraduate text.
  Dutta, Prajit K. (1999), Strategies and games: theory and practice, MIT Press, ISBN 978-0-262-04169-0. Suitable for undergraduate and business students.
  Fudenberg, Drew and Jean Tirole (1991) Game Theory MIT Press.
  Gibbons, Robert (1992), Game Theory for Applied Economists, Princeton University Press (July 13, 1992), ISBN 978-0-691-00395-5. Lucid and detailed introduction to game theory in an explicitly economic context.
  Morgenstern, Oskar and John von Neumann (1947) The Theory of Games and Economic Behavior Princeton University Press.
  Myerson, Roger B. (1997), Game Theory: Analysis of Conflict, Harvard University Press, ISBN 978-0-674-34116-6
  Osborne, Martin (2004), An Introduction to Game Theory, Oxford University Press, ISBN 978-0-19-512895-6.
  Papayoanou, Paul (2010), Game Theory for Business: A Primer in Strategic Gaming, Probabilistic Publishing, ISBN 978-0964793873
  Rubinstein, Ariel; Osborne, Martin J. (1994), A Course in Game Theory, MIT Press, ISBN 978-0-262-65040-3. A modern introduction at the graduate level.
  Shoham, Yoav; Leyton-Brown, Kevin (2009), Multiagent Systems: Algorithmic, Game-Theoretic, and Logical Foundations, New York: Cambridge University Press, ISBN 978-0-521-89943-7. A comprehensive reference from a computational perspective; see Chapter 3. Downloadable free online.
  
  Original Nash papers[edit]
  
  Nash, John (1950)  "Equilibrium points in n-person games" Proceedings of the National Academy of Sciences 36(1):48-49.
  Nash, John (1951) "Non-Cooperative Games" The Annals of Mathematics 54(2):286-295.
  
  Other references[edit]
  
  Mehlmann, A. (2000) The Game's Afoot! Game Theory in Myth and Paradox, American Mathematical Society.
  Nasar, Sylvia (1998), A Beautiful Mind, Simon & Schuster.
  
  External links[edit]
  "Nash theorem (in game theory)", Encyclopedia of Mathematics, EMS Press, 2001 [1994]
  Complete Proof of Existence of Nash Equilibria
  Simplified Form and Related Results Archived 2021-07-31 at the Wayback Machine
  .mw-parser-output .navbox{box-sizing:border-box;border:1px solid #a2a9b1;width:100%;clear:both;font-size:88%;text-align:center;padding:1px;margin:1em auto 0}.mw-parser-output .navbox .navbox{margin-top:0}.mw-parser-output .navbox+.navbox,.mw-parser-output .navbox+.navbox-styles+.navbox{margin-top:-1px}.mw-parser-output .navbox-inner,.mw-parser-output .navbox-subgroup{width:100%}.mw-parser-output .navbox-group,.mw-parser-output .navbox-title,.mw-parser-output .navbox-abovebelow{padding:0.25em 1em;line-height:1.5em;text-align:center}.mw-parser-output .navbox-group{white-space:nowrap;text-align:right}.mw-parser-output .navbox,.mw-parser-output .navbox-subgroup{background-color:#fdfdfd}.mw-parser-output .navbox-list{line-height:1.5em;border-color:#fdfdfd}.mw-parser-output .navbox-list-with-group{text-align:left;border-left-width:2px;border-left-style:solid}.mw-parser-output tr+tr>.navbox-abovebelow,.mw-parser-output tr+tr>.navbox-group,.mw-parser-output tr+tr>.navbox-image,.mw-parser-output tr+tr>.navbox-list{border-top:2px solid #fdfdfd}.mw-parser-output .navbox-title{background-color:#ccf}.mw-parser-output .navbox-abovebelow,.mw-parser-output .navbox-group,.mw-parser-output .navbox-subgroup .navbox-title{background-color:#ddf}.mw-parser-output .navbox-subgroup .navbox-group,.mw-parser-output .navbox-subgroup .navbox-abovebelow{background-color:#e6e6ff}.mw-parser-output .navbox-even{background-color:#f7f7f7}.mw-parser-output .navbox-odd{background-color:transparent}.mw-parser-output .navbox .hlist td dl,.mw-parser-output .navbox .hlist td ol,.mw-parser-output .navbox .hlist td ul,.mw-parser-output .navbox td.hlist dl,.mw-parser-output .navbox td.hlist ol,.mw-parser-output .navbox td.hlist ul{padding:0.125em 0}.mw-parser-output .navbox .navbar{display:block;font-size:100%}.mw-parser-output .navbox-title .navbar{float:left;text-align:left;margin-right:0.5em}hide.mw-parser-output .navbar{display:inline;font-size:88%;font-weight:normal}.mw-parser-output .navbar-collapse{float:left;text-align:left}.mw-parser-output .navbar-boxtext{word-spacing:0}.mw-parser-output .navbar ul{display:inline-block;white-space:nowrap;line-height:inherit}.mw-parser-output .navbar-brackets::before{margin-right:-0.125em;content:"[ "}.mw-parser-output .navbar-brackets::after{margin-left:-0.125em;content:" ]"}.mw-parser-output .navbar li{word-spacing:-0.125em}.mw-parser-output .navbar a>span,.mw-parser-output .navbar a>abbr{text-decoration:inherit}.mw-parser-output .navbar-mini abbr{font-variant:small-caps;border-bottom:none;text-decoration:none;cursor:inherit}.mw-parser-output .navbar-ct-full{font-size:114%;margin:0 7em}.mw-parser-output .navbar-ct-mini{font-size:114%;margin:0 4em}vteTopics in game theoryDefinitions
  Congestion game
  Cooperative game
  Determinacy
  Escalation of commitment
  Extensive-form game
  First-player and second-player win
  Game complexity
  Game description language
  Graphical game
  Hierarchy of beliefs
  Information set
  Normal-form game
  Preference
  Sequential game
  Simultaneous game
  Simultaneous action selection
  Solved game
  Succinct game
  Equilibriumconcepts
  Bayesian Nash equilibrium
  Berge equilibrium
   Core
  Correlated equilibrium
  Epsilon-equilibrium
  Evolutionarily stable strategy
  Gibbs equilibrium
  Mertens-stable equilibrium
  Markov perfect equilibrium
  Nash equilibrium
  Pareto efficiency
  Perfect Bayesian equilibrium
  Proper equilibrium
  Quantal response equilibrium
  Quasi-perfect equilibrium
  Risk dominance
  Satisfaction equilibrium
  Self-confirming equilibrium
  Sequential equilibrium
  Shapley value
  Strong Nash equilibrium
  Subgame perfection
  Trembling hand
  Strategies
  Backward induction
  Bid shading
  Collusion
  Forward induction
  Grim trigger
  Markov strategy
  Dominant strategies
  Pure strategy
  Mixed strategy
  Strategy-stealing argument
  Tit for tat
  Classesof games
  Bargaining problem
  Cheap talk
  Global game
  Intransitive game
  Mean-field game
  Mechanism design
  n-player game
  Perfect information
  Large Poisson game
  Potential game
  Repeated game
  Screening game
  Signaling game
  Stackelberg competition
  Strictly determined game
  Stochastic game
  Symmetric game
  Zero-sum game
  Games
  Go
  Chess
  Infinite chess
  Checkers
  Tic-tac-toe
  Prisoner's dilemma
  Gift-exchange game
  Optional prisoner's dilemma
  Traveler's dilemma
  Coordination game
  Chicken
  Centipede game
  Lewis signaling game
  Volunteer's dilemma
  Dollar auction
  Battle of the sexes
  Stag hunt
  Matching pennies
  Ultimatum game
  Rock paper scissors
  Pirate game
  Dictator game
  Public goods game
  Blotto game
  War of attrition
  El Farol Bar problem
  Fair division
  Fair cake-cutting
  Cournot game
  Deadlock
  Diner's dilemma
  Guess 2/3 of the average
  Kuhn poker
  Nash bargaining game
  Induction puzzles
  Trust game
  Princess and monster game
  Rendezvous problem
  Theorems
  Arrow's impossibility theorem
  Aumann's agreement theorem
  Folk theorem
  Minimax theorem
  Nash's theorem
  Purification theorem
  Revelation principle
  Zermelo's theorem
  Keyfigures
  Albert W. Tucker
  Amos Tversky
  Antoine Augustin Cournot
  Ariel Rubinstein
  Claude Shannon
  Daniel Kahneman
  David K. Levine
  David M. Kreps
  Donald B. Gillies
  Drew Fudenberg
  Eric Maskin
  Harold W. Kuhn
  Herbert Simon
  Hervé Moulin
  John Conway
  Jean Tirole
  Jean-François Mertens
  Jennifer Tour Chayes
  John Harsanyi
  John Maynard Smith
  John Nash
  John von Neumann
  Kenneth Arrow
  Kenneth Binmore
  Leonid Hurwicz
  Lloyd Shapley
  Melvin Dresher
  Merrill M. Flood
  Olga Bondareva
  Oskar Morgenstern
  Paul Milgrom
  Peyton Young
  Reinhard Selten
  Robert Axelrod
  Robert Aumann
  Robert B. Wilson
  Roger Myerson
   Samuel Bowles
  Suzanne Scotchmer
  Thomas Schelling
  William Vickrey
  Miscellaneous
  All-pay auction
  Alpha–beta pruning
  Bertrand paradox
  Bounded rationality
  Combinatorial game theory
  Confrontation analysis
  Coopetition
  Evolutionary game theory
  First-move advantage in chess
  Game Description Language
  Game mechanics
  Glossary of game theory
  List of game theorists
  List of games in game theory
  No-win situation
  Solving chess
  Topological game
  Tragedy of the commons
  Tyranny of small decisions
  
  Authority control: National libraries  
  Germany
  
  
  
  
  
  <img src="//en.wikipedia.org/wiki/Special:CentralAutoLogin/start?type=1x1" alt="" title="" width="1" height="1" style="border: none; position: absolute;" />
  Retrieved from "https://en.wikipedia.org/w/index.php?title=Nash_equilibrium&oldid=1109707207"