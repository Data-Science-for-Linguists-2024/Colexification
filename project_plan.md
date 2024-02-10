# Colexification Across the Globe
- Author: Teresa Davison
- Email: tid30@pitt.edu
- Feb 10, 2024

## 1. BRIEF SUMMARY

- I would like to explore colexification in different languages. Many languages have words that, though the form of the word stays the same, there are multiple concepts associated with that one word. For instance, in Russian there is no distinction between the word for "arm" or for "hand," while there is in English. I would like to explore whether certain colexifications of concepts are common within language families, if they are impacted by proximity geographically, or if there are certain types of concepts that are more common across all languages based on word embeddings or category of meaning.

## 2. DATA

- On the CLICS website, the data is in the form of tables linked together via hyperlinks: [Master Table](https://clics.clld.org/parameters). This can be useful for exploration, but actual calculations will be difficult. The data dowloadable comes in the form of either .gml networks, which I have yet to discover how to interact with outside of the web app since it's not ASCII encoded, and an .sqlite database. 

- The [sqlite database](https://github.com/clics/clics3/blob/master/clics3.sqlite.zip) can be converted into DataFrames fairly easily. I plan to use either the sql database or convert each table from the database into DataFrames and use those directly. After exploring each of the tables in the sql database I think I have a firm grasp on how they are connected, namely I will be looking for "forms" (given in IPA) in sepcific languages that are connected to multiple "parameters" (concepts). I have identified three tables during my exploration as being important for my analyses: FormTable, ParameterTable, and LanguageTable. There are foreign keys to connect information across the different tables. Other tables in the SQL database will likely not be needed.

- Beyond finding which concepts share the same form in a given language, the table containing the "parameters" also has categorizations for the ontological category (Person/Thing, Action/Process, Property, Other,      Number, Classifier) or semantic field (smaller, finer categories like body, agriculture or kinship) for each concept. This will aid in investigating the relationship between colexifications in certain semantic fields with language families or geographical areas. The latter information is housed in the LanguageTable including information like language family, macroarea and lat-/longitude for each language. Additionally, I could play with word embeddings through the GloVe pretained vector embeddings to explore colexification of similar concepts.

- There are 18,954 different concepts (some of which may not have colexifications), 1,462,125 word forms, 3,248 languages, and 201 language families represented in the dataset. From this, it seems like there would be strong power to any findings and the data represents many languages well. 


## 3. ANALYSIS

- During my analyses I would like to explore if there are categories of words with more colexifications or more widely spread colexifications than others. I would also like to see if features like language family, geographical area or category of word can predict the likelihood of colexifications or any correlations between these features. Some colexifications may be more frequent in terms of the number of languages they appear in, but they may also be more frequent in terms of how many concepts are tied to the same word. 

- I would be interested in building a model that could predict geographical region or language family from the colexifications a language has using machine learning models. I would want to compare the performance of various models to choose which one would be most effective. However, there would be many different classes to categorize between so I might explore clustering or some sort of decision tree.

## 4. PRESENTATION

- I would present my data much like anyone else, with the presentation of any classifiers I am able to make, any limitations I encountered, any anamolies and visualizations of the data in the form of plots or maps. The Lexibank data format seems to have plugins to create world maps and show the prevalence of features in different geographical areas, which I would be interested in using for my presentation.

