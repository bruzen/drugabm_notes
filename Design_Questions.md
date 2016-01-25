# Crime and Drug ABM Design Questions: Model Details and Parameter Values

This is rough first pass at listing what we will need to define in order to build the model.

The questions are general. Answering these will let us write individual level equations and algorithms. These will define a set of parameter and state variables.

These questions assume the basic structure described in my previous set of model notes. As that document evolves so will this list.


## Questions

- **Agents:** How many of each type?

- **Movement:** How do agents move? Do police police particular regions more than others? Do do agents congregate? Why? E.g. do they have a tendency to clump where there is existing drug activity?

- **Networks:** How many of each agent type is in each agent's network? How do agents interact with their networks? And how do networks affect agents (some contagion effects)?

- **Police activity:** How/when do police make discoveries? How does a police discovery affect the portion of the network they know? How does acting on a discovery affect it?  

- **Drug use causes:** When do agents do drugs? E.g. are there location/network/addiction/random effects? 

- **Drug use effects:** What are the effects of drug use? E.g. are there health risks? Is there a chance of a problem with each use? Is there a danger in crossing a threshold?

- **Drug market:** What is the supply/demand curve/relationship for drugs? If we start with system level data, how do we relate the global supply/demand relationship with individual choices (the ecological interfaces problem)? Is it okay to change all individuals' demand probabilistically based on a global number from the curve (e.g. they get a fraction of the total depending on their details/addiction/etc.)?  Alternatively, we may only define individual level preferences and see what happens globally.

- **Drug market risk:** Can we treat risk, e.g. from increased policing after a raid, as a shift in the price demanded by high level dealers using standard economics for risk? 

- **Legalization:** What do prices go to after legalization? What is demand? What social/other factors affect it? 

- **Advertising:** Do we want to take a shot at modelling the effect of things like allowing advertising? E.g. we could model it as a change in either the typical demand or in the demand curve? Can we approximate how big the effect is?


## Next Steps
 
- We could either **talk** through the questions when we meet, **or** we could each go through and **answer independently** before our conversation, then we could get a sense of where our intuition differs. 

- We can start modelling with just back of the envelope **approximations** and look at what the model is sensitive to, too decide where we need greater accuracy/precision.

- I've done this very quickly. It might be good also if we each tried to **add** at least one or two **questions** before we talked.


# Notes on Language

- In addition to general questions about model design, there are two kind of things to define, **parameters** which we program into the model and **state variables** which are the values variables in the model. These values are produced by the model. We can validate the model by checking that these values are reasonable. For instance we set a parameter for the number of agents, define their preferences, and let them trade. The quantity of drugs those agents buy and sell are state variables.

- For parameter values we will eventually want not just the **average** number, but what is the **range** of values, is there **randomness**, and what is the **distribution**?

- In each case we should identify parameters  and/or state variables we want to **experiment** with changing. Some to validate the robustness of an effect, others to answer a question.

- As an aside, I'm treating interventions as a special kind of **parameter** value that is an arbitrary algorithmic change to the model. While the normal parameter space has a fixed dimension, the space of **interventions** is arbitrarily large, since you could code any change in rules or practices. While we can sweep over a range of parameters systematically, we can only look at a tiny subset of types interventions.
