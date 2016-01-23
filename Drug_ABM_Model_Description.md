#Agent Based Model of Drug Markets and Crime

###Purpose:
The purpose of this model is to explore the dynamics of illegal drug markets. It focuses in particular on the effect of policing, legalizations, and other interventions on shaping the social, economic and spatial patterns of drug use.

###Questions: 
- How much policing and money would be required to stop the trade?
- What is the effect of a ‘rational drug use policy’ focusing on mid-level versus street level dealers

###Agents:
- Dealers: street level dealers, mid-level distributors, importers
- Users: casual users (90% of the population), heavy users
- Non-users
- Police

###Space:
- Neighborhood Census Area (probably Toronto or San Francisco)


###Interventions:
- Increase policing level at street level (more police on the street)
- Increase police focus on high level dealers and distributors
- Decrease discretion granted by police when activity is caught
- Increase chance of charge

###Parameters:
- Number of police hours, spatial distribution of policing

###Measures:
- Number of arrests 
- Number of stories (?) 
- Number of dealers
- Quantity of drugs sold ($ and volume)

###Network structure:
- The line from user, dealer, mid-level, dealer to importer in the network typically has very few branches. One occasionally two or three. Casual users will often only know one dealer. Some will have one or two people as a backup in case the primary trusted dealer does not come through. Street-level and mid-level deals have an interest in preventing their customers from learning about the source of the drugs, so they won’t get access to cheaper drugs.  Dealers are also inclined towards having one supplier (i.e. mid-level dealer or importer) that they know and trust, though they may also have backups (there are risks of cost/low quality/safety with going to new suppliers)
- We need data on the number of users per dealer, dealers per mid-level dealer, and dealers per importer (could model as one importer)
- We also need data on the social structure of the network between users and non-users, what social contagion effects exist, how much of the network is known by police, and how much police knowledge is common knowledge vs individual in one police officer.

###Risk:
- Different relationships in the network have different degrees of trust, so each relationship is weighted with a trust co-efficient. 
- Dealers and users also have a general variable for perceived risk.
    - Increase visibility of uniformed police on the streets acts as a deterrent, reducing the amount of drug activity. This may cause a change in user and dealer behaviour. Light users might become less likely to buy drugs. Dealers might change to safer locations, hold the drugs for shorter times, sell to only trusted customers, or increase prices.
    - Perceived risk increases with the number of recent seizures
    - Perceived risk can increase when there is an investigation
- Different locations are perceived as involving different levels of risk
- When risks is high users and dealers avoid low trust relationships and locations, and the price of transactions increases.
- Despite increased police presence, upper level dealers will continue distributing. They are unlikely to change their interactions with lower level dealers, except perhaps by increasing the price and reducing the purity of the drugs to reduce the need to import more drugs.
- The size of drug shipments by importers will increase with potential gain (supply demand curve)
- Charges leveraged are almost always possession of drugs (using drugs is not actually an illegal act)
- Physical and relationship distance can lead to an individual being caught for possessing drugs
- Police are less likely to exercise discretion when an individual possess larger amounts of drugs, particularly in a crackdown situation
- Crackdowns can lead police to trace more relationships in the network of possessing and selling drugs

###Spatial structure:
- Particular spaces are known as places where dealers congregate
- There may be more policing in particular neighborhoods, increased speed of response etc.
- There may be more policing where there is more known drug activity

###New Users and Dealers:
- If a particular dealer or distributor is removed, by police arrest etc., a new one will take it’s place. There may be a small delay as they ramp up and build up a network.
-  It is more challenging to replace mid-level distributors. There are larger lags as they ramp up.
-  If consumers get removed from the market for whatever reason, they are naturally going to be replaced by the demand
-  There are transitions with people moving between being non-users, causal users, and heavy users. All people might have a degree of use parameter so we don’t have to model users and non-users separately. 
    -  New users transition from being non-users if there are more well connected users in their network, near them spatially, if there are lower cost drugs, and if using drugs is perceived as low risk.
    -  There may also be a way for users to transition to non-users. 
    -  What factors affect users becoming heavy users? Is it just a chance.
    -  Do health problems lead to removal of some heavy users? E,g. by hospitalization?

