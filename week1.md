Welcome to Math v Gerrymandering 2022 in the Computational Math at Tarleton REU!!  I'm Dr. Scott Cook.  Sadly, I have to be at a family funeral until Tuesday, so you'll need to get started without me :(

In this repo, you should see workshops part 1 & 2 and "make_animations".  The workshop was delivered 3/31 at the MAA TX conference (link to video inside).  Even if you attended that workshop, we went really fast.  I created make_animations in mid-April.

I want you all to use these 3 notebooks to learn about BOTH the data wrangling AND the MCMC analysis processes.  This is also some fairly hefty Python code that you can learn a lot from.

We have several projects this summer, but I'd like to wait to dive into them until I get back.  I have a non-trivial warm up task to try to complete before I get back.  I don't think it is too hard once you understand the code.  But, of course, understanding the code is point :)

TASK

Background
In "make_animations", there are functions called "no_defect_cap" and "with_defect_cap" which run recomb under different constraints.  For this task, you can ignore the latter.

Look at line 56:
pop_constraint = gc.constraints.within_percent_of_ideal_population(initial_partition, 0.1)

This forces the chain to reject any proposal that would cause population deviation (pop dev) to exceed 10%.  This works with no problem.  But, suppose we want a tighter pop dev cap of 5%.  If you replace 0.1 with 0.05, you should get an error:

ValueError: The given initial_state is not valid according is_valid. The failed constraints were: Bounds(population,(670108.5483870967, 740646.2903225806))

That's because the map STARTS with pop dev above 5%.

Goal
Implement a "push and hold" strategy which allows pop dev to start above 5% (avoiding the error) and gradually "pushes" it down to 5% rejecting any proposal that increases pop dev.  Once it drops below 5%, the chain switches to "hold" it below 5%.

Good luck!!
