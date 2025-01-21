# FEC Political Contributions Analysis

## Overview
This project analyzes individual contributions to Federal Committees, including presidential, senate, and house committees, for the period from June 20, 2024, to July 24, 2024. The analysis involves data collection, processing, and analysis using Apache Spark. The goal is to uncover patterns and trends in political contributions during this period.

## Technologies Used
- **AWS**: The project was hosted on Amazon Web Services for scalable computing resources.
- **EC2 Instance**: An EC2 instance was used to run the Jupyter Notebook and process the data.
- **Jupyter Notebook**: The analysis was conducted using Jupyter Notebook, which provides an interactive environment for data exploration and visualization.
- **SQL**: SQL queries were used to analyze the data and extract insights.
- **Bash**: Bash scripting was used for data preprocessing tasks such as unzipping files and converting file formats.
- **PostgreSQL**: PostgreSQL was used for database management and querying.
- **Apache Spark**: Apache Spark was used for distributed data processing and analysis.

## Dataset
The dataset was officially obtained from the Federal Election Commission (FEC) website. You can access the dataset [here](https://www.fec.gov/data/browse-data/?tab=bulk-data).

## Project Steps

### Data Collection
1. **Uploading and Unzipping Data**: The data was downloaded from the FEC website and uploaded to the EC2 instance. The files were unzipped using Bash commands.
2. **Removing Zip Files**: To save space, the zip files were removed after extraction.

### Data Processing
1. **Converting .txt to .csv**: The unzipped .txt files were converted to .csv format using the `csvformat` utility.
2. **Word Count Verification**: The number of lines in the original .txt files and the converted .csv files were compared to ensure successful conversion.
3. **Combining Header and Data Files**: The header file and the data files were concatenated to create a single dataset.
4. **Understanding the Data**: The schema and the first few rows of the data were printed to understand the structure.

### Key Insights from FEC Political Contributions Analysis

1. **Top 10 States by Total Count of Contributions**  
   - **Insight**: California (CA), Texas (TX), and Florida (FL) dominated in both the number of contributions and total amounts, reflecting their political and economic influence.

2. **Top 10 States by Total Amount of Contributions**  
   - **Insight**: California led with **$64.8 billion**, followed by Texas (**$55.4 billion**) and Illinois (**$34.1 billion**), highlighting the concentration of contributions in wealthier states.

3. **Contributions Above $5000**  
   - **Insight**: High-value donors like **Timothy Mellon ($50 million)** and organizations like **One Nation ($18.4 million)** were among the top contributors, showcasing the influence of wealthy individuals and PACs.

4. **Total Contributions by Individual**  
   - **Insight**: **Timothy Mellon** contributed a total of **$55 million**, followed by **One Nation ($18.4 million)**, emphasizing the significant role of ultra-wealthy donors in campaign financing.

5. **Contributor’s Name, Occupation, and Transaction Amount**  
   - **Insight**: High-value contributors predominantly came from sectors like **Investments** and **Entrepreneurship**, indicating the financial industry's strong influence in political funding.

6. **Top 10 Committees by Total Contributions on a Given Date**  
   - **Insight**: Committee **C00825851** received a record **$50 million** on **07/15/2024**, demonstrating the pivotal role of PACs in campaign financing and their ability to mobilize large sums quickly.

---

### **Summary of Insights**
- **Geographic Concentration**: Contributions are heavily concentrated in states like California, Texas, and Florida, reflecting their economic and political clout.
- **Wealthy Donors and PACs**: Individuals like Timothy Mellon and organizations like One Nation dominate contributions, raising concerns about the influence of money in politics.
- **Sectoral Influence**: Contributors from the financial and entrepreneurial sectors play a significant role in campaign financing.
- **PACs' Role**: Committees like C00825851 highlight the growing reliance on PACs to fund campaigns, often tied to specific political events or milestones.

This analysis underscores the importance of transparency and regulation in campaign finance to ensure a fair democratic process.

## Conclusion
The analysis reveals significant insights into political contributions, emphasizing the influence of wealthy individuals and PACs. The findings underscore the importance of transparency and regulation in maintaining a fair democratic process.

## References
- [FEC Dataset](https://www.fec.gov/data/browse-data/?tab=bulk-data)
- [Politico Article on Timothy Mellon](https://www.politico.com/news/2024/08/20/timothy-mellon-maga-inc-00175249)
- [FEC Records for One Nation](https://www.fec.gov/data/committee/C00468447)
