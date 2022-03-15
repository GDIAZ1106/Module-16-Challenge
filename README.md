# Amazon_Vine_Analysis

## Analysis Overview
This project analyzes Amazon Vine program and determines if there is a bias toward favorable reviews from Vine members.\
The analysis uses PySpark to perform the ETL process to extract the dataset, transform the data, connect to an AWS RDS instance, load the transformed data into pgAdmin and calculate different metrics.\
We focused on the US reviews music instruments.

## Resources
- Data Source: [Amazon Review datasets](https://s3.amazonaws.com/amazon-reviews-pds/tsv/index.txt), [Musical  Instruments](https://s3.amazonaws.com/amazon-reviews-pds/tsv/amazon_reviews_us_Musical_Instruments_v1_00.tsv.gz)
- Software: Google Colab Notebook, PostgreSQL 13.4, pgAdmin 4, AWS

## Results
### Figures resulting from the analysis
Once the database have been filtered to show only articles with more than 20 reviews and with more than 50% of helpful votes we have a total of 14,537 rows in the database. The overall figure show that 56.72% of those articles have a 5-star rating. 

When filtering this to separate the reviews that are paid from those unpaid, we have only 60 articles that form part of the vine program and 14,477 that do not form part of such a program. 

5-star rating on articles that form part of the vine program account for 56.67% of the total, while the non paid reviewed articules have a 5-star percentage of 56.72%

## Conclusion

According to the analysis perform we cannot conclude that any bias exist on the paid reviewers, since the percentage of 5-star articles on paid and unpaid reviewers are almost the same. Having said this, we are not in the position of saying that the bias do not exist since the amount of articles that form part of the vine program is fairly reduce and therefore any minor change in the rating could change the percentage of the vine program on a material way.

In order to finally determine the bias on the vine program a similar analysis but on a bigger vine database is recommended. 