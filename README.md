# School_District_Analysis

## Overview of this project

This project provides a high-level on a dataset (district) of schools and students that were graded for a mathematics and reading test.

Maria is thrilled that there is no missing data in the CSV files. By doing an exploratory analysis and testing to determine how to "clean" a student's name. We found and remplace the following words that some student have by running the code below.

```
# Add each prefix and suffix to remove to a list.
prefixes_suffixes = ["Dr. ", "Mr. ","Ms. ", "Mrs. ", "Miss ", " MD", " DDS", " DVM", " PhD"]

# Iterate through the words in the "prefixes_suffixes" list and replace them with an empty space, "".
for word in prefixes_suffixes:
    student_data_df["student_name"] = student_data_df["student_name"].str.replace(word,"")

# Check names.
student_data_df.head(10)
```

## Size and district results and analysis

#### Figure 1: District before adjustment

<img src="https://github.com/poboisvert/School_District_Analysis/blob/main/Resources/images/district_mod.png?raw=true" width="750" />

#### Figure 2: District after removing 9th grade from Thomas High School
<img src="https://github.com/poboisvert/School_District_Analysis/blob/main/Resources/images/district_ori.png?raw=true" width="750" />

The figure 1 and 2 illustrate the effect of removing the 461 students in 9th grade from Thomas Student School. This shows a significant variation for the reading, mathematic and overall result and seem to confirm an alteration of the dataset. Removing 461 students improved all the passing statistics.

#### Figure 3: District before adjustment
<img src="https://github.com/poboisvert/School_District_Analysis/blob/main/Resources/images/school_ori.png?raw=true" width="750" />

#### Figure 4: District after adjustment
<img src="https://github.com/poboisvert/School_District_Analysis/blob/main/Resources/images/school_mod.png?raw=true" width="750" />

The Figure 3 and 4 show by comparing the size of Thomas High School with 1,635 students against all the school in this dataset. Again, the removing the 9th grade only the size “Medium (1000-2000)” is improving since the 9th grades seems to be a group below the average. The modification showed that the 9th grade is above the average result and all metrics higher.

## Test results and analysis 

#### Figure 5: Reading score before modification
<img src="https://github.com/poboisvert/School_District_Analysis/blob/main/Resources/images/read_ori.png?raw=true" width="750" />

#### Figure 6: Reading score before modification
<img src="https://github.com/poboisvert/School_District_Analysis/blob/main/Resources/images/read_mod.png?raw=true" width="750" />

The figure 6 seems to confirm that almost all students in the 9th grade got a passing grade, but we can not confirm it since we do not have any metrics like IQR, median or minimum. The figure 5 and 6 show the before (figure 5) and after the manipulation (figure 6) that the 9th grade wasn’t the worst or the best performer for the reading test. This analysis to not confirm a signigicant variation.

#### Figure 7: Mathematics score before modification
<img src="https://github.com/poboisvert/School_District_Analysis/blob/main/Resources/images/math_ori.png?raw=true" width="750" />

#### Figure 8: Mathematics score before modification
<img src="https://github.com/poboisvert/School_District_Analysis/blob/main/Resources/images/math_mod.png?raw=true" width="750" />

The figure 7 and 8 illustrate the mathematics grade for Thomas High School. The only conclusion is the 9th was the best performing class across all.

## Sending analysis & conclusion

#### Figure 9: Spending before modification
<img src="https://github.com/poboisvert/School_District_Analysis/blob/main/Resources/images/spend_ori.png" width="750" />

#### Figure 10: Spending after modification
<img src="https://github.com/poboisvert/School_District_Analysis/blob/main/Resources/images/spend_mod.png?raw=true" width="750" />

Figure 9 & 10 show a slight improvement for the overall passing grade and the total % for the $630-644 group which include Thomas High School. In conclusion, the 9th group seems in the average, but slighly lower and by removing it, the school is improving and maintain his second rank.

#### Figure 11: Top 5 after modification
<img src="https://github.com/poboisvert/School_District_Analysis/blob/main/Resources/images/top5_mod.png?raw=true" width="750" />

