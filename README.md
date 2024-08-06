# Usecase-3-Project-2 (University Rank)


## 1- PROCESS 
    1. Loading The Data
    2. Data Profiling
        2.1 Clean Data: 
            2.1.1 Cleaning the 'World Rank' Column:
                df['World Rank'] = df['World Rank'].map(lambda x: int(x.split('T')[0])) 
                "This line removes any characters after 'T' in the 'World Rank' column and converts the result to an integer. It assumes 'World Rank' values might have a 'T' followed by other characters."
            
            2.1.2 Handling Missing Values:
                df['Educational Rank'] = df['Educational Rank'].map(lambda x : 0 if x == '-' else x)
                df['Employability Rank'] = df['Employability Rank'].map(lambda x : 0 if x == '-' else x)
                df['Faculty Rank'] = df['Faculty Rank'].map(lambda x : 0 if x == '-' else x)
                df['Research Rank'] = df['Research Rank'].map(lambda x : 0 if x == '-' else x)
                "Replaces any '-' values in the ranking columns with 0, indicating that missing values or non-numeric data should be treated as zero."

            2.1.3 Converting Columns to Integer Type:
                df['Educational Rank'] = df['Educational Rank'].astype(int)
                df['Employability Rank'] = df['Employability Rank'].astype(int)
                df['Faculty Rank'] = df['Faculty Rank'].astype(int)
                df['Research Rank'] = df['Research Rank'].astype(int)
                "Converts the ranking columns to integers. This step ensures that numerical operations can be performed on these columns."
    3. Univariate analysis
    4. Multivariate Analysis

## 2- RESULT
    1. Which universities are ranked in the top 10 globally?

    2. Which universities are ranked in the top 10 for employment outcomes?

    3. What positions do universities in Saudi Arabia hold within the global rankings?

    4. Considering various factors such as employment rankings, research rankings, and others, which has the most significant impact on a university's overall ranking?

    5. Is there a correlation between national and global university rankings, and based on this information, can you recommend a country that appears to
    have a high concentration of top-ranked universities?

    6. Develop two additional questions

## 3- Team members:-  
1. علي الفارس
2. سامر غربي 
3. احمد الصبحي
4. عبدالعزيز الكثيري
