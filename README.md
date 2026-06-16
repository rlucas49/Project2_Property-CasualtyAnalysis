# Project2_Property-CasualtyAnalysis

This project uses LangGraph to create a multi-agent AI assistant that runs a preliminary EDA on a given dataset. A manual EDA .ipynb file is included for comparison. The EDA AI agent code should generalize to other datasets if in the same format.

I'm starting with an property and casualty dataset.

The architecture here is a plan-evaluate ReAct loop.

Architecture: Plan → Code-Write → Execute → Evaluate (ReAct loop)

Specialist Agents
Basic_Summary – shape, dtypes, nulls, descriptive stats, unique counts, duplicates
Grapher – distributions, frequency bars, numeric correlation heatmap



### Explaination of the Columns
There are a lot of abbreviations and terms. Operationalizing for convenience of the reader (and myself while working on this project).

-	AGENCY_ID Unique	 ID of the insurance agency
-	PRIMARY_AGENCY_ID	 ID of the main or parent agency (if applicable)
-	PROD_ABBR	 Product abbreviation (short code for insurance product type)
-	PROD_LINE	 Product line (e.g., auto, home, life)
-	STATE_ABBR	 U.S. state abbreviation (e.g., NY, CA)
-	STAT_PROFILE_DATE_YEAR	 Year of the statistical profile or reporting snapshot
-	RETENTION_POLY_QTY	 Quantity of retained policies
-	POLY_INFORCE_QTY	 Number of in-force (active) policies
-	PREV_POLY_INFORCE_QTY	 In-force policy count in the previous period
-	NB_WRTN_PREM_AMT	 New Business Written Premium Amount
-	WRTN_PREM_AMT	 Total Written Premium Amount
-	PREV_WRTN_PREM_AMT	 Written Premium Amount from the previous period
-	PRD_ERND_PREM_AMT	 Period Earned Premium Amount
-	PRD_INCRD_LOSSES_AMT	 Period Incurred Losses Amount
-	MONTHS	 Number of months in the time period covered
-	RETENTION_RATIO	 Percentage of policies renewed
-	LOSS_RATIO	 Incurred losses ÷ earned premium (this is the formula I am aware of)
-	LOSS_RATIO_3YR	 3-year average loss ratio
-	GROWTH_RATE_3YR	 3-year growth rate
-	AGENCY_APPOINTMENT_YEAR	 Year the agency was appointed or contracted
-	ACTIVE_PRODUCERS	 Count of active insurance producers (agents)
-	MAX_AGE, MIN_AGE	 Maximum and minimum age of something
-	VENDOR_IND	 Vendor indicator
-	VENDOR	 Name or ID of vendor
-	CL_BOUND_CT_MDS	 Count of Commercial Lines policies bound via MDS platform
-	CL_QUO_CT_MDS	 Count of quotes for CL via MDS
-	CL_BOUND_CT_SBZ	 Bound count via SBZ platform
-	CL_QUO_CT_SBZ	 Quotes via SBZ
-	CL_BOUND_CT_eQT	 Bound via eQT
-	CL_QUO_CT_eQT	 Quotes via eQT
-	PL_BOUND_CT_ELINKS	 Personal Lines bound via eLinks
-	PL_QUO_CT_ELINKS	 Quotes via eLinks
-	PL_BOUND_CT_PLRANK	 Bound via PLRank platform or program
-	PL_QUO_CT_PLRANK	 Quotes via PLRank
-	PL_BOUND_CT_eQTte	 Bound via eQTte
-	PL_QUO_CT_eQTte	 Quotes via eQTte
-	PL_BOUND_CT_APPLIED	 Bound via Applied (Applied Systems)
-	PL_QUO_CT_APPLIED	 Quotes via Applied
-	PL_BOUND_CT_TRANSACTNOW	 Bound via TransactNow (a quoting/bridging tool)
-	PL_QUO_CT_TRANSACTNOW	 Quotes via TransactNow

