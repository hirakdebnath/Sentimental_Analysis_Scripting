from textblob import TextBlob
import pandas as pd

df = pd.read_excel('C:\\Users\\hirak.deb.nath\\Downloads\\Ind_Processed_may.xlsx', sheet_name='indTaxo_Ind_updated') 
df.set_index('Sno', inplace=True)
result2 = []
for index, row in df.iterrows():
    y = row["Sentences"]    
    edu = TextBlob(str(y))
    x = edu.sentiment.polarity
    z = edu.sentiment.subjectivity
    print(x)
    if x<0:
        result = -1 
    elif x ==0:
        result =  0 
    elif x>0 or x==1:
        result =  1 
    print(result)   
    result2.append(result)
df['Manual'] = result2
df.to_excel('C:\\Users\\hirak.deb.nath\\Downloads\\Ind_Processed_may_new.xlsx', index=False)
