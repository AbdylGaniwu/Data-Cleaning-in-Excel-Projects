#Data Cleaning: Movies Dataset

##Project Overview:
This project focuses on cleaning and organizing movie data to enhance its usability and analysis potential.

##Data Cleaning Steps:
Combined Data Separation:
=CONCAT("Written by: ", RIGHT(B2, LEN(B2)-FIND(":", B2)))

Separates and formats author names within "Written by:" format.
=CONCAT("Narrated by: ", RIGHT(B2, LEN(B2)-FIND(":", B2)))
Separates and formats narrator names within "Narrated by:" format (similar to author names).

##Date Formatting:
Converted release date to a long date format.

Movie Age Calculation:
=YEAR(TODAY()) - YEAR(E2) & "Years"
Calculates the current age of each movie in current year.

Rating Extraction:
Flash fill was used to extract ratings from a combined "Rate out of 5" field. This separates the rating and out-of-5 information.

Price Formatting:
Converted numerical price values to an accounting format.
Cedis (Ghana, West Africa)

Time Lapse Conversion:
=IF(ISNUMBER(SEARCH("hrs",D2)),LEFT(D2,2),0)
Extracts hours from the time lapse string (e.g., "2hrs").

=IF(ISNUMBER(SEARCH("mins",D2)),LEFT(RIGHT(D2,7),2),0)
Extracts minutes from the time lapse string (e.g., "20mins")

These formulas combine to convert the time lapse from a text format (e.g., "2hrs 20mins") to total minutes for easier calculations.
Total calculate Total minutes:
= (Hours * 60) + Minutes

Feel free to adjust or expand upon these steps based on the specific details of your dataset and cleaning requirements.
Provide examples of the original and cleaned data (anonymized if necessary) to illustrate the transformations.
