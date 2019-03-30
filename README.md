# Complete-Cigarette-Smokers-Solution

I implemeted my own Semaphores you can see the code files in semaphore library file uploaded in this github
for Expalnation for those implemtation please see readme files of github files https://github.com/lokeshreddy1999/producer_consumer_solution

Now I am going to explain solution of Complete(deadlock free and starvation free )-Cigarette-Smokers-Solution

problem statement:Assume a cigarette requires three ingredients to make and smoke: tobacco, paper, and matches. 
There are three smokers around a table, each of whom has an infinite supply of one of the three ingredients — one smoker has an infinite supply of tobacco, another has paper, and the third has matches.
There is also a non-smoking agent who enables the smokers to make their cigarettes by arbitrarily (non-deterministically) selecting two of the supplies to place on the table.
The smoker who has the third supply should remove the two items from the table, using them (along with their own supply) to make a cigarette, which they smoke for a while. Once the smoker has finished his cigarette, the agent places two new random items on the table. 
This process continues forever.

solutions :Here I inculded three pushers which will  able to select the right smokers to take the ingredients that has been placed by agent on the table
the main aim i included the pushers is to reduce the "DEADLOCK".for suppose pushers puts ingredients tabbaco(A) and mathes(C) .then pushersA or pushers c invvokes one after other and invokes the thired smokers(here person with paper ) to make cigeratte.

you can read this pdf to get complete understading 
https://cse.yeditepe.edu.tr/~kserdaroglu/spring2014/cse331/labnotes/WEEK%205%20-%20SEMAPHORES/mysemaphoreexamplesMOE.pdf

fast explanantion:

we uses 7 semaphores

1)semaphore agentsem:this is initilazed with 1 and when anyone makes thier cigerartte the this used to invoke agent;

2)semaphore Tobacco:this is initilazed with 0 and when this will become invoked  when agent puts tabacco on the table; 

3)semaphore Paper;this is initilazed with 0 and when this will become invoked  when agent puts Paper on the table;

4)semaphore Match;this is initilazed with 0 and when this will become invoked  when agent puts Match on the table;

5)semaphore mutex;this is used for mutuall excusions

6)Tobaccosem:this invokes the person with tabbaco to take remaning ingrdients on the table// simmilarly other papersem and Matchsem


To get to know the full algo see the code using this hints 



