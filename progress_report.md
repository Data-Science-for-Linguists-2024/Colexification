# Progress Report
Teresa Davison

### Log 1
Explored the data by turning the sqldatabase into DataFrames in Project_exploration notebook. Concluded that I will be using LanguageTable, FormTable, and ParameterTable for analyses. Updated project plan.

### 1st Progress Report

1. Data Sharing Plan
After cursorally exploring the data, I decided to use three of the tables: LanguageTable (l_df), FormTable (f_df), and ParameterTable (p_df) for my analysis. Since these data are licensed under CC BY 4.0 by [these contributors](https://github.com/clics/clics/blob/master/CONTRIBUTORS.md), I will make smaller versions of these dfs and pickle them to share in a folder named ['data_samples'](https://github.com/Data-Science-for-Linguists-2024/Colexification-Across-the-Globe/tree/main/data_samples).

2. What I accomplished
Working in [progress_report1.ipynb](https://github.com/Data-Science-for-Linguists-2024/Colexification-Across-the-Globe/blob/main/progress_report1.ipynb) I explored each of the three tables more thouroughly, investigating things like how many languages were included, their language families and physical locations, number of concepts represented, and most importantly the links between the tables that can help me do analysis later.

I then did a little test attempt to come up with colexifications for the concept named 'dust'. During this test, I found out that the use of parameter IDs for the concepts in the form df was troubling. There are multiple different PIDs for the same concept because they come from different databases. I found a temporary fix where I added the corresponding concepticon IDs to the form df. The process I used to create the dataframe of colexifications took a while to run, so I will have to be careful to come up with the most efficient way to create data structures to house the colexifications and then analyze them.

### 2nd Progress Report

1. Summary of what I accomplished
In this phase, I worked in [progress_report2.ipynb](https://github.com/Data-Science-for-Linguists-2024/Colexification-Across-the-Globe/blob/main/progress_report2.ipynb) and decided to make a data frame for a specific language with each row corresponding to a different form in the language. Then I made a column with a list of different concepts colexified for each form. I did this first with German, since I'm familiar with the language. I then added the semantic field and ontological category corresponding to each concept per form and made dictionaries to show the number of occurences of colexification between centain semantic categories or ontological fields to see if there would be differences between languages and if those differences would be more stark for languages less closely related or further geographically.

Then I made a function to streamline the process and repeated the process for Russian and Tamil to have a language semi similar to German and one not related to either German or Russian. Just looking at the dictionaries for each, it seemed like there were bigger differences in terms of frequency of semantic field bieng colexified for lless similar languages, but that could easily be chance.

- Data sharing: I will be sharing the dfs for German, Russian and Tamil as csvs in the [data_sample](https://github.com/Data-Science-for-Linguists-2024/Colexification-Across-the-Globe/tree/main/data_samples) folder, along with the other samples. Additionally, people could use the function I used for other languages easily.
- License: I have decided to use the GNU GENERAL PUBLIC LICENSE v 3.0 because I would like my work to be accesible but stay as I made it.
