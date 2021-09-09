
# Make attractive AD transcripts for your product
It takes a lot of time to think of appealing advertisement transcripts. To save your time, I made a NLP model that writes advertisement transcripts about your product. I used [Teachable NLP](https://ainize.ai/teachable-nlp) to make my own NLP model. 

### Try Ad transcript generator model: [link](https://kubecon-tabtab-ainize-team.endpoint.ainize.ai/?modelUrl=https://train-m7vw4m8hinqgzra7s7wr-gpt2-train-teachable-ainize.endpoint.ainize.ai/predictions/gpt-2-en-small-finetune&text=Type%20a%20category%20of%20your%20product)

# Data perparation 

To prepare the advertisement transcripts dataset, I looked up the word, 'Advertisement', at the data section in Kaggle. Thankfully, I found the data that I need.: ' **Advertisement Transcripts from Various Industries.** ' ([link](https://www.kaggle.com/kevinhartman0/advertisement-transcripts-from-various-industries?select=Advertisement_Transcripts_deduped_edited.xlsx))

The advertisement transcripts are consist of 2,000 advertisement scripts from various industries including automotive, food & beverage, home & personal care, healthcare, media & entertainment, advocacy, and more.
Then I checked the license of the data. The data license is CC0: Public Domain, one of several public copyright licenses that enable free distribution.
![image](https://user-images.githubusercontent.com/89971178/131820535-30fab027-f882-4749-afdf-a826502cd664.png)

# Data Pre-processing
After I downloaded the dataset, I check the dataset to find parts that do not need to be trained.
Since I only need the advertisement transcripts, I removed all columns except the 'Ad copy' column and also removed 'Ad copy' row, which is the name of the data. 
![image](https://user-images.githubusercontent.com/89971178/131820599-138754b6-ba97-4e42-89f4-666d0c07f08a.png)

*Be aware of the file format of your dataset! Teachable NLP accepts only TXT files so I converted the CSV file into TXT file format by using [csv. → txt. file converter](https://products.groupdocs.app/conversion/csv-to-txt).

After converting the file format, I checked inappropriate empty spaces that do not need to be trained. There was no inappropriate empty space that needed to be removed. 
When the data cleaning was done, I checked whether the data size is enough to train the model or not. The data size is 733 KB, which is somewhat enough to train the model.


# Result of NLP Model

Since the dataset includes the food & beverage category, I typed '**Ice cream**' and clicked '**Run autocomplete**' button. I chose one of the suggestions that are perfect for my ice cream advertisement transcripts. 

See my first result below. The sentence suggested by my NLP model is mind-blowing! I wouldn't even have thought about it. Isn't this amazing? 
* Bolded words were written by myself. :

> **Icecream** and chocolate chips, it's a meal that will make you forget all about work, deadlines, schedules

![image](https://user-images.githubusercontent.com/89971178/131820730-a7b429eb-597b-4a29-9df6-01db5699f714.png)
![image](https://user-images.githubusercontent.com/89971178/131820740-ba93a6a3-7df9-45ee-8a54-b1780445ccf6.png)


After few more iterations, I made a compelling advertisement transcript for my product with a help of my NLP model. 
* **Bolded words** were written by myself. 
* *Italics words* were originally suggested by my NLP model but I replaced them to words that were more related to my product.

> **Ice cream** and chocolate chips, it's a *dessert* that will make you forget all about work, deadlines, schedules, budgets, and all the worries. Ice cream will satisfy your soul, your body and your spirit with this savory. **Our ice cream has three flavors: Vanilla, Strawberry, and Chocolate.** Try this out and see how they differ from one another. Visit our website [icecream.com](http://icecream.com) for a taste of your favorite.

:shushing_face:**A small tip to make your advertisement transcripts better:**
Don't hesitate to edit the sentences suggested by your NLP model! Your direction will make your NLP model write better advertisement transcripts that are more related to your product!

### Try Ad transcript generator model: [link](https://kubecon-tabtab-ainize-team.endpoint.ainize.ai/?modelUrl=https://train-m7vw4m8hinqgzra7s7wr-gpt2-train-teachable-ainize.endpoint.ainize.ai/predictions/gpt-2-en-small-finetune&text=Type%20a%20category%20of%20your%20product)
