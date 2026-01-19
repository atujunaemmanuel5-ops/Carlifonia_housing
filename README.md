# Carlifonia_housing
I'm working through chapter 2 of "Hands on Machine Learning with Scikit Learn,Keras & Tensor Flow by O'Reily" and 
am encountering an error when creating a custom pipeline with ColumnTransformer
Error message:  A given column is not a column of the dataframe

# Code causing the issue
full_pipeline = ColumnTransformer([
("num",num_pipeline,num_attribs),
("cat",OneHotEncoder(),cat_attribs),
])
df_prepared = full_pipeline.fit_transform(df)
# Objective 
create a complete machine learning pipeline for predicting Carlifornia housing prices that includes
1.Data preprocessing
2.Custom feature engineering(CombinedAttributesAdder)
3.Handling numerical and categorical features

# Specific issues 
The columnTransformer is failing with error above likely because num_attribs or cat_attribs incorectly defined or might
be dataframes instead of lists
