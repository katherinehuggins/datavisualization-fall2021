# Padilla's Funding Mainly Comes From Small-Time Donors

Sen. Alex Padilla, D-Calif., who was appointed by California Gov. Gavin Newsom (D) to fill now-Vice President Kamala Harris' seat, appears financially prepared to take on his first Senate election, with the vast majority of his funding coming from small donations from individuals in California.
According to data from the FEC, nearly two-thirds of donations (63%) to Padilla since early 2021 came from individuals — and over half (55%) of all his donations came from entities in California, highlighting a strong base both locally and financially, with which the senator can launch his re-election bid.

Original data set link: https://www.fec.gov/data/receipts/?data_type=efiling&committee_id=C00765164

### Steps to Clean Data

1. change column (load timestamp) to short date format
2. Delete column A and B — line number (A) is not useful information and committee name (B) is unnecessary since it specifies that the donations are going to Alex Padilla, which is already clear from the dataset (all rows the same)
3. Delete column C and D — transaction ID and image number are not useful reference points and do not include usable data
4. Delete back reference and back schedule columns, since they don't include pertinent data or info (G and H)
5. Delete column M donor prefix (all blank), delete AI and J irrelevant
6. Delete columns Z-AF because committee info is already mentioned in earlier columns, including location
7. Insert Column D "contributor full name"
8. =CONCATENATE(E2," ",F2," ",G2) to merge Columns of first name, middle and lat name into one
9. New sheet and delete columns first/middle/last (the copying and pasting clears the formula too and makes it only values) 
10. Change columns J and K into currency 

Now my data is as clean as I want it to be and it's time to analyze...

Command A and insert pivot table in a new sheet, drag contributor state into row and sum of contributions into value, then sort from highest to lowest
Using that same pivot table, I also sorted by entity type (and eliminated the state filter), as well "contributor full name" under entity type. My questions and subsequent findings are below.

1. Where did the largest sum of money come from during 2021-2022, state-wise?
A: California by a massive margin ($4.3 million), followed by Massachusetts ($1.9 million) and Washington, D.C. (about $520k). 

2. Conversely, what states offered the least amount of funding to Padilla?
A: Arkansas ($250), West Virginia ($375) and Kentucky ($500)

3. What percentage of the donations were coming from individuals versus PACs/committees/etc?
A: The vast majority (62.5%) of donations during the 2021-2022 cycle came from individuals (about $5 million), followed by ~$2 million from organizations (25%) and about $980,000 from PACS (~12%). 

4. Who were the top aggregate donors over the 1-year-period among those top three groupings (individual, organization and PAC)?
A: The biggest aggregate donor was the organization ActBlue with an aggregate of $1.4 million over the year, followed by Padilla's PAC, Padilla Harder Victory Fund, with about $22,000 in total donations. This shows that while his campaign received most of its funding through individual donors, as shown above, most donors did not contribute large sums. 
The individual donor with the biggest donation aggegrate sum from the year is David Lizarraga, at just $7800.




