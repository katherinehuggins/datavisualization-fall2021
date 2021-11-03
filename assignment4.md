# Padilla Does Not Rely on PACs for Fundraising, Individuals Remain Primary Source

Sen. Alex Padilla, D-Calif., who was appointed by California Gov. Gavin Newsom (D) to fill now-Vice President Kamala Harris' seat, appears financially prepared to take on his first Senate election, with the vast majority of his funding coming from small donations from individuals in California.
According to data from the FEC, nearly two-thirds of donations (63%) to Padilla since early 2021 came from individuals — and over half (55%) of all his donations came from entities in California, highlighting a strong base both locally and financially, with which the senator can launch his re-election bid.

Original data set link: https://www.fec.gov/data/receipts/?data_type=efiling&committee_id=C00765164

Working data set to see the steps I took in Excel: https://github.com/katherinehuggins/datavisualization-fall2021/blob/main/Alex%20Padilla%20Data_KHuggins.xls

### Steps to Clean Data

1. Change column (load timestamp) to short date format
2. Delete column A and B — line number (A) is not useful information and committee name (B) is unnecessary since it specifies that the donations are going to Alex Padilla, which is already clear from the dataset (all rows the same)
3. Delete column C and D — transaction ID and image number are not useful reference points and do not include usable data
4. Delete back reference and back schedule columns, since they don't include pertinent data or info (G and H)
5. Delete column M donor prefix (all blank), delete AI and J irrelevant
6. Delete columns Z-AF because committee info is already mentioned in earlier columns, including location
7. Insert Column D "contributor full name"
8. =CONCATENATE(E2," ",F2," ",G2) to merge Columns of first name, middle and lat name into one
9. New sheet and delete columns first/middle/last (the copying and pasting clears the formula too and makes it only values) 
10. Change columns J and K into currency 

### Now my data is as clean as I want it to be and it's time to analyze...

Command A and insert pivot table in a new sheet, drag contributor state into row and sum of contributions into value, then sort from highest to lowest
Using that same pivot table, I also sorted by entity type (and eliminated the state filter), as well "contributor full name" under entity type. My questions and subsequent findings are below.

*1. Where did the largest sum of money come from during 2021-2022, state-wise?*

A: California by a massive margin ($4.3 million), followed by Massachusetts ($1.9 million) and Washington, D.C. (about $520k). 

*2. Conversely, what states offered the least amount of funding to Padilla?*

A: Alaska ($250), West Virginia ($375) and Kentucky ($500). However, he had no donations from Iowa, Hawaii, Louisiana, Mississippi, North Dakota, Ohio or South Carolina.

*3. What percentage of the donations were coming from individuals versus PACs/committees/etc?*

A: The vast majority (62.5%) of donations during the 2021-2022 cycle came from individuals (about $5 million), followed by ~$2 million from organizations (25%) and about $980,000 from PACS (~12%). 

*4. Who were the top aggregate donors over the 1-year-period among those top three groupings (individual, organization and PAC)?*

A: The biggest aggregate donor was the organization ActBlue with an aggregate of $1.4 million over the year (which of course is crowd-sourced funds), followed by Padilla's PAC, Padilla Harder Victory Fund, with about $22,000 in total donations. This shows that while his campaign received most of its funding through individual donors, as shown above, most donors did not contribute large sums. 
The individual donor with the biggest donation aggegrate sum from the year is David Lizarraga, at just $7800.

## Adding belatedly out of sheer curiosity...

I wanted to learn more about those donations in AK, WV and KY. The sums of $250, $375 and $500 come from three donors, one in each state: Marilyn  Romano, an Alaska Airlines employee in Alaska, Ramon Alvarez in West Virginia who says he is not employed, and Emily Da Silva in Kentucky, a principal for CJ Lake LLC (law firm).

I was curious what other donations these three had made, since they seemed to be the odd ones out, so I checked the FEC database through their donor lookup.

Aside from her ActBlue contributions, I was curious to see that the only campaigns Romano donated directly toward were Alaska's Republican Sens. Lisa Murkowski and Dan Sullivan, as well as former Democratic Sen. Mark Begich in 2014. It seems unusual that she would contribute to a Democrat in California's campaign, as she is by no means a serial out-of-state donor.

I then looked up Ramon Alvarez and limited the results to West Virginia. Also a big ActBlue donor, Alvarez has contributed solely to Democrats' campaigns — and was in particular, a prolific donor during Joe Biden's and Speaker Nancy Pelosi's campaigns.

Lastly, Emily Da Silva from Kentucky: It appears Emily does not actually live in Kentucky. Only one of her many Democratic donations was listed from there; donations made around the same time were listed in Washington, D.C. — also where her office is based. So I think it's safe to say that Padilla did not actually receive any funds from Kentucky, making it a total of eight states from which Padilla has received zero funding.
