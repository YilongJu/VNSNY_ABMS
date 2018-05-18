# VNSNY_ABMS
# Plans

## Phase I: Markov Model for patients' states
### 1. Build Patients Archetypes
Using NHATS to build patients' archetypes. Sort High utilizers by good/bad habits.(Times to visit doctors from Claim?). Build high utilizer area data from census.
### 2. Model State Transition
> Need some literature research
5 states: S L D H N
Consider Dual Eligible/Ineligible, and number of Comorbidities (1-3,4-7,8+)
Other factors to be confirmed
Using R to calculate probability again. (probability, rate)(model by AnyLogic)
* Add consideration of more variables: low/medium/high utilizers.
* Check correlation among utilizers, dual eligibility and number of comorbidities.

## Phase II: Model Transits / Accessibilities
Provider Side, End-to-end hospital model, mobile service models.
### 1. Create Agent Goals
Regard the moment when a state transition happens as the moment when a goal generates (Need for short-term stay, Nursing, long-term stay, house or go home).
### 2. Model Agent Decisions
Create models (using GSP trees, accessibility indices and etc.) for population to determine their actions when they have a need:
* Go to hospital / clinics
* Call for visiting nurses, case workers, caregivers
* Stay at home doing nothing
### 3. Calculate Costs
Including expense of service call, transportation expense and some quantification of negative personal feelings
### 4. Optimize the resource allocation to minimize the cost.
This can be done with Anylogic builtin optimizer.
## Phase III: Connecting Shiny App with R
Show the results in shiny map.
