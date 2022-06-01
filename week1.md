Welcome to Math v Gerrymandering 2022 in the Computational Math at Tarleton REU!!  I'm Dr. Scott Cook.  Sadly, I have to be at a family funeral until Tuesday, so you'll need to get started without me :(

In this repo, you should see workshops part 1 & 2 and "make_animations".  The workshop was delivered 3/31 at the MAA TX conference (link to video inside).  Even if you attended that workshop, we went really fast.  I created make_animations in mid-April.

I want you all to use these 3 notebooks to learn about BOTH the data wrangling AND the MCMC analysis processes.  This is also some fairly hefty Python code that you can learn a lot from.

We have several projects this summer, but I'd like to wait to dive into them until I get back.  I have a non-trivial warm up task to try to complete before I get back.  I don't think it is too hard once you understand the code.  But, of course, understanding the code is point :)

TASK
In "make_animations", there are functions called "no_defect_cap" and "with_defect_cap" which run recomb under different constraints.  For this task, you can ignore the latter.

Look at line 56:
pop_constraint = gc.constraints.within_percent_of_ideal_population(initial_partition, 0.1)
