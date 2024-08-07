# FS-Classifiction-CF
1.Match_to_cats_across_years (rmd file)
Download the Financial Statement and Notes Datasets from SEC with XBRL
read broad_cat_with_aggregation_v2.csv 
export pre_20xx.csv and sub_20xx.csv files
export df_year.csv (in data/df.zip)
export cognate_search_year.csv (in data zip folder)

2. Data joining.ipynb
read df_year.csv(in data/df.zip), export data_master.csv(in data/data_master.csv.zip) , df.sav(in data/df.sav.zip)
read cognate_search_year.csv(in data zip folder), export cognate_search.csv(in data)

3. Initial exploration.ipynb
Read data_master.csv(in data/data_master.csv.zip)
Show head and description
Explore report, line, stmt, inpth, tag, prole, plabel, negating, name, form, broad_cat
Display correlations

4. Modeling_with_loc_broad_cat_part1_V3_oversampling.ipynb (simple model for broad cats)
Read df.sav(in data/df.sav.zip)
Export labels_to_ids_1.sav, ids_to_labels_1.sav(in data zip folder)
Export model_disagg_broad_cat.sav(in data zip folder)

5. Modeling_with_loc_broad_cat_part2_V3_oversampling.ipynb
Select column (plabel, broad_cat, contain “interact”, contain “presence”//plabel, broad_cat, plabel_proc ) and clean duplicates.
Data preprocessing for plabel, which is originally text data, oversampling for splitting train and text data
(remove stopwords, remove punctuation, create bigrams(try) and trigram(not try), stemming, Create sentence again)
Set current disagg and use TF-IDF to extract features and export vectorizer
Cross-validation

7. Modeling_with_loc_lvl_step_part1_v4_all_disagg
