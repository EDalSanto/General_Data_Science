#Chipotle Command Line Homework

##Questions

1. Look at the head and the tail of chipotle.tsv in the data subdirectory of this repo. 
Think for a minute about how the data is structured. What do you think each column means? 
What do you think each row means? Tell me! (If you're unsure, look at more of the file contents.)

	* Answer: Order #, Quantity of Item_Name ordered, Item_Name, Description of Item 
	
2. How many orders do there appear to be?
	
	* Answer: **1,834**

3. How many lines are in this file?

	* Answer: **4,623**
		* wc -l

4. Which burrito is more popular, steak or chicken?

	* Answer: **Chicken**
		*compare 'grep -i "chicken burrito" | wc -l' to 'grep -i "steak burrito" | wc -l  

5. Do chicken burritos more often have black beans or pinto beans?
	
	*Answer: **Black Beans**
		*compare "chicken burrito" DAT8/data/chipotle.tsv | grep -i "black beans" | wc -l
		and grep -i "chicken burrito" DAT8/data/chipotle.tsv | grep -i "pinto beans" | wc -l
	

6. Make a list of all of the CSV or TSV files in the DAT8 repo 
(using a single command). Think about how wildcard characters can help you with this task.

	*Answer: DAT8/data/airlines.csv
			 DAT8/data/bank-additional.csv
			 DAT8/data/bikeshare.csv
			 DAT8/data/chipotle.tsv
			 DAT8/data/drinks.csv
			 DAT8/data/hitters.csv
			 DAT8/data/imdb_1000.csv
			 DAT8/data/sms.tsv
			 DAT8/data/titanic.csv
			 DAT8/data/ufo.csv
			 DAT8/data/vehicles_test.csv
			 DAT8/data/vehicles_train.csv
			 DAT8/data/yelp.csv
		* find DAT8 -name *".?sv"

7. Count the approximate number of occurrences of the word "dictionary" 
(regardless of case) across all files in the DAT8 repo.

	*Answer: 1,353
		* grep -r "dictionary" DAT8 | wc -w
	
8. Optional: Use the the command line to discover something "interesting" about
the Chipotle data. Try using the commands from the "advanced" section!
	
	*Answer: They sold 122% more items with chicken than with steak
		*grep -i "chicken" chipotle.tsv | wc -l and grep -i "steak" chipotle.tsv | wc -l