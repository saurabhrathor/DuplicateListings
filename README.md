# DuplicateListings
Finding duplicate listings in Online Retailer Dataset

Features of Dataset observed from review -
1. The dataset is unlabeled, supervised learning can't be implemented
2. in Unsupervised learning, clustering can be used, but can't estimate the No. of Clusters as there can be many.
3. Dataset is mix of Numeric and Textual Data
4. Most of the Textual entries are unique so converted them to Unique Numeric Integer.


Other Techniques to find Duplicate Entries - 
1. Calculating Hash Value -- That is ot ok here as any small change will lead to huge variation.
2. Using Word2vec model -- It will be better. However, as every entry is unique, it will lead to more complexity. Converting Text to Vector will create multi-vector data.

Final Implementation -
This implementation is basically using Auto-encoders for dimmensionality reduction of available Dataset and then find Euclidean distance among each other. It involves following steps - 
1. Converting Textual data into numeric by giving them Unique Numeric identity.
2. Merging this transformed data with Numeric fields.
3. Transformed input is processed using Auto-encoders to perform Dimmensionality reduction and extract features.
4. These extracted features are used to find similarity among products by calculating euclidian distance.
