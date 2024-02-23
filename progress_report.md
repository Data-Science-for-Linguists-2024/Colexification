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