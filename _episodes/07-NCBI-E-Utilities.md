---
title: "Excercise: NCBI E-utilities"
teaching: 
- "5"
exercises: 
- "20"
questions:
- "How can we use the Entrez Programming Utilities (E-utilities) to search across the Entrez Molecular Sequence Database System?"
objectives:
- "Introduce the Entrez Molecular Sequence Database System (Entrez) and the databases it includes."
- "Provide sources for documentation and more information about using the E-utilities."
- "Develop API calls answer research questions using data pulled from Entrez through the E-utilities." 
keypoints:
- "By linking to the NCBI Entrez system through the E-utilities, you can make complicated data requests across a huge dataset."
---

## Entrez Molecular Sequence Database System (Entrez)

Entrez is a molecular biology database system that provides integrated access to nucleotide and protein sequence data, genomic mapping informaiton, 3D structure data, PubMed MEDLINE, and more. This system is produced by the National Center for Biotechnology Information (NCBI). 

Entrez is NCBI's primary text search and retreival system that integrates the PubMed database of biomedical literature with 38 other literature and molecular databases

The web based search interface for these NCBI databases is avaiable to the public [here, through the U.S. National Library of Medicine](http://www.ncbi.nlm.nih.gov/Entrez/).

#### Databases included in Entrez
[You can find a full list of Entrez databases listed here](https://www.ncbi.nlm.nih.gov/books/NBK3837/).

## Entrez Programming Utilities (E-utilities)
The E-utilities are made up of 9 programs that provide access to Entrez. You can find a list of these 9 programs in the table below. The information shown in this table was taken from [Eric Sayers A General Introduction to the E-utilities](https://www.ncbi.nlm.nih.gov/books/NBK25497/).

| E-utilities | Query string | Use |
| ------ | ------ | ------ |
| EInfo | eutils.ncbi.nlm.nih.gov/entrez/eutils/einfo.fcgi | Provides the number of records indexed in each field of a given database, the date of the last update of the database, and the available links from the database to other Entrez databases. |
| ESearch | eutils.ncbi.nlm.nih.gov/entrez/eutils/esearch.fcgi | Responds to a text query with the list of matching UIDs in a given database (for later use in ESummary, EFetch or ELink), along with the term translations of the query. |
| EPost | eutils.ncbi.nlm.nih.gov/entrez/eutils/epost.fcgi | Accepts a list of UIDs from a given database, stores the set on the History Server, and responds with a query key and web environment for the uploaded dataset. |
| ESummary | eutils.ncbi.nlm.nih.gov/entrez/eutils/esummary.fcgi | Responds to a list of UIDs from a given database with the corresponding document summaries. |
| EFetch | eutils.ncbi.nlm.nih.gov/entrez/eutils/efetch.fcgi | Responds to a list of UIDs in a given database with the corresponding data records in a specified format. |
| ELink | eutils.ncbi.nlm.nih.gov/entrez/eutils/elink.fcgi | Responds to a list of UIDs in a given database with either a list of related UIDs (and relevancy scores) in the same database or a list of linked UIDs in another Entrez database; checks for the existence of a specified link from a list of one or more UIDs; creates a hyperlink to the primary LinkOut provider for a specific UID and database, or lists LinkOut URLs and attributes for multiple UIDs. |
| EGQuery | eutils.ncbi.nlm.nih.gov/entrez/eutils/egquery.fcgi | Responds to a text query with the number of records matching the query in each Entrez database. |
| ESpell | eutils.ncbi.nlm.nih.gov/entrez/eutils/espell.fcgi | Retrieves spelling suggestions for a text query in a given database. | 
| ECitMatch | eutils.ncbi.nlm.nih.gov/entrez/eutils/ecitmatch.cgi | Retrieves PubMed IDs (PMIDs) corresponding to a set of input citation strings. |

#### E-utilities Documentation
- [Entrez Programming Utilities Help](https://www.ncbi.nlm.nih.gov/books/NBK25501/) 


>## Title
> Description
> - instruction
> - instruction
> 1. consideration
> 2. consideration
>
>>## Solution
>>1. Step 1
>>2. Step 2
>{: .solution}
{: .challenge}


>## Perform a search across all Entrez databases
> Perform a global Entrez search to determine racial/ethnic representation across database contents. 
> 1. Identify which E-utility to use for this task.
> 2. Identify how you will conceptualize and categorize racial/ethnic groupings for this task.
> - NIH racial and ethnic categories include American Indian or Alaska Native, Asian, Black or African American, Hispanic or Latino, Native Hawaiian or Other Pacific Islander, and White. (See NOT-OD-15-089)[https://grants.nih.gov/grants/guide/notice-files/not-od-15-089.html] for more details.
> 3. Write and run the API strings that would enable you to uncover these representations. 
>
>>## Solution
>> Here is an example of API calls that could provide you with summary data based on NIH racial and ethnic categories. (There are many potential solutions to this exercise!) 
>>1. https://eutils.ncbi.nlm.nih.gov/gquery?term=african+AND+black&retmode=xml
>>2. https://eutils.ncbi.nlm.nih.gov/gquery?term=white&retmode=xml
>>3. https://eutils.ncbi.nlm.nih.gov/gquery?term=hispanic+OR+latino&retmode=xml
>>4. https://eutils.ncbi.nlm.nih.gov/gquery?term=native+hawaiian+OR+pacific+islander&retmode=xml
>{: .solution}
{: .challenge}

>## Design your own research question
> Develop a research question about databases included in Entrez, or about the data held within the databases.
> Review the table of E-utilities, their query strings, and use cases above.
> - Please share your research question in the class etherpad in the designated section. 
> 1. Which E-utilitiy would provide you with the type of data you could use to answer your question?
> 2. Which databases would you need to query with your choses E-utility in order to answer your research question?
> 3. Try writing the APIs that would provide you with the data that would answer your research question!
>
>>## Solution
>>- Did it work?
>>1. If it worked, please share your API calls in the etherpad by your research question.
>>2. If it did not work, consider if the problem is conceptual or technical and share your thoughts in the eatherpad near your research question.  
>{: .solution}
{: .challenge}
