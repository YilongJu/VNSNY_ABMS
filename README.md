# VNSNY_ABMS
# Plans

## Phase I: Markov Model for patients' states
### 1. Build Patients Archetypes
1. **NHATS data** – Use Brooke’s 3 patient archetypes – what factors distinguish them (beyond just older and sicker)? Can we find those other factors in Claims or Census Datasets (eg, poverty, educ level, male, single, race)? 
1. **Claims Data** - Sort High utilizers by good/bad habits.(Times to visit doctors from Claim – see Miriam’s email. Also aside from routine visits, do we know if Carrier is ER or ED?). 
1. **Census Data** - Build high utilizer area data from census.(hot spotting)
### 2. Model State Transition
> Need some literature research

* 5 states: S L D H N (ask Miriam if there is a state for Home w/care)
* Plot claims data to see if it supports continuous probabilities
* **Build top-down model both ways** (constant rate vs. continuous  time Markov models) 
* Using R to calculate probability again. (probability, rate)
### 3. Construct Agent Population
* Consider Dual Eligible/Ineligible, and number of Comorbidities (1-3,4-7,8+) 
* Other factors to be confirmed
* Add consideration of more variables: low/medium/high utilizers. 
Check correlation among utilizers, dual eligibility and number of comorbidities. 
Conjoin probabilities into a population model with  AnyLogic)

## Phase II: Model Transits / Accessibilities
Provider Side, End-to-end hospital model, mobile service models.
### 1. Research Provider Side
Research Provider Side, End-to-end hospital model, mobile service models
* Primary Care Service Area (PCSA) data
* Area Health Resource File (AHRF)
* MPI numbers (individuals vs. facilities) – how to show on map? In model? (model all nodes? 1 of each type? 1 in each tract? Or how?)
* Highest goal is to substitute lesser cost providers
### 2. Create Bottom Up Agent Goals
* Regard the state transitions as the ground truth about the actual population (Need for short-term stay, Nursing, long-term stay, house or go home).
* Try to use Theory of Reasoned Action (or similar theory) for agents to make bottom up decisions about their healthcare. Agents make daily healthcare micro-decisions and macro-behavior of the population emerges over time.
* Compare emergent macro-behavior to state transitions. Possibly re-tune the agent parameters to get the macro-behavior to more closely mimic real life transition rates.
### 3. Model Agent Causation and Effects
> Need some literature research (what causes disease to grow worse? Just old age vs. poor behavior in ADLs?)

Create models (using GSP trees, accessibility indices and etc.) for population to determine their actions when they have a need:
*Model the Activities of Daily Living (ADLs)*
* See UN model of ADLs
* Take meds, get refills
* Exercise
* Eat right
* Keep routine Dr. appointments
* Go to hospital / clinics
* Get wrap around services (home care) - Call for visiting nurses, case workers, caregivers
* Stay at home doing nothing
### 4. Calculate Costs
> Need some literature research

Including expense of service call, transportation expense and some quantification of negative personal feelings
### 5. GUI Policy Sliders
* Change range of input variables
* Alter policy considerations
* Add more vs less urgicare/retail med clinics in hot spots
* Add some ADL sliders
* Slider for top down vs. bottom up? (top down better for predicting a given individual’s future, while bottom up is better for testing policy effects)
### 6. Optimize the resource allocation to minimize the cost.
* This can be done with Anylogic builtin optimizer. If our license does not permit using that, we need to write our own experiment designer, model controller, and comparator across runs. 
* Possibly do this in AnyLogic, but possibly do this in R. Which is best?

## Phase III: Connecting Shiny App with R
Show the results in shiny map.
