Project Status: Complete

Author: Andrew Mazmanian

Course: CS 3110.01



1. Which problem(s) gave me the most trouble? Did you avoid any problem that is too challenging to finish by deadline? Did you ask questions to AI/instructor?

   The last three problems I found significantly harder than the first two. The first two were straightforward pattern-matching problems. The last two required remembering what happened previously while waiting for future input all while ensuring something will never happen. I did not avoid any problems that were too challenging as I simply just did the first 5 from the range of questions we were allowed to do. I did ask AI how to input an image in a Markdown file asked for some additional points to test if there was an area I feel like the points I came up with were lacking, hopefully I inputted in images correctly and in a format that would suffice the assignment's criteria.
   
2. Which problem(s) surprised you with a "gold-st-ring"? Which next state(s) did you not account for in the subset of next states? why? How to make sure you avoid such errors in your future flight/traffic/compiler state controller tasks, or in the near future, the course projects/exams?

   	I created the NFAs before putting them into JFLAP, making sure I thought of any possible scenarios I wasn't thinking of, so I never really ran into any surprises with a "gold-st-ring", at least I believe I didn't from my understanding. There was instances though, before putting the NFAs into JFLAP, where I encountered some problems. 
   	Initially when making a NFA for {string s| s starts with 01 and ends with  10 }, I lacked a 0 self-loop on q3 so any string with consecutive zeros in the middle (like 010010) would crash, fixing this by adding the self-loop I lacked creating this sort-of waiting room for zeros  till 1 was read again for a possible 0 to be read to complete the requirements. This also had my q3 acting as a Trap state, instead of its intended sort-of waiting room state, which is more of a DFA trait that is not was is being asked of this assignment. Additionally, when making a NFA for {string s| s doesn't contains substring 10 }, I lacked a double-circled Accept state on both states, not just on q0 that I had initially. With this addition, in allowed for any string, even an empty one, to still be accepted as long as it did not contain a substring of 10.
   	I believe errors like this happened because I was instinctively tracing a short, and most likely to be successful string, to purely create these bridges per say to get to the desired accept state, forgetting for evaluating for every possible combination of strings that could be present in every single automaton. To avoid this in the future, I plan on first defining the meaning of every state in an automaton, recognizing why its should be included and what it means when we reach that state. Additionally, I'll try to run each finished diagram under 4 distinct test cases, that I felt to be extremely helpful in the process of creating these NFAs: An empty string, 0 \& 1, consecutive identical inputs (0000 or 1111), and alternating inputs (0101). These 4 test cases became my go to when determining the validity of my diagrams, helping me uncover the issues I mentioned previously.
