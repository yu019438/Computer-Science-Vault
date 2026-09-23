#CS2PP 
- Data science reveals patterns/trends from data in order to produce insights that business/scientists may use to inform decisions. 
- Data science combines the following fields:
	- Statistics
	- Scientific methods
	- AI
	- Data analysis
## Machine Learning 
- We can use machine learning in data science in order to reverse the typical expert system into a data-driven approach:
![[Pasted image 20260923154628.png]]
- In the above image, classical programming shows that the programmer writes the rules themselves.  
	- E.g. `if temperature > 30: return "hot"` -> the rule is pre-decided
- Machine learning inverts this process by allowing a computer to study countless examples of data paired with answers, in order for it to determine the rules itself. 
	- E.g. scanning labelled photos through a machine, allowing it to learn what order of pixels/pixel values determine the photo's label
- **CORE CONCEPT**: In classical programming, humans supply the logic, whereas in a machine learning approach logic is *derived from the data*
### Supervised vs unsupervised learning
- **Supervised Learning**: Machine learning is defined as being supervised when the training data is labelled -> This allows the machine to predict labels for new, unseen data:
	- **Regression**: when the prediction is continuous *(price of an item)*
	- **Classification**: When the answer is a categorical label *(cat vs dog)*
- **Unsupervised learning**: Machine learning is defined as being unsupervised when the training data contains no label (raw data), and the machine is left to determine its own data structure
	- **Clustering**: When a machine groups similar data points together without being given input as to what the groups should be 
---
## The Data Science Process
This is the workflow for turning raw data into usable insight:
1. **Frame the problem**: Clearly define what you're trying to solve
2. **Collect data**: Find a source, plan access, understand its basic characteristics
3. **Exploratory Data Analysis**: Examine the data in detail, look for abnormalities/ notable statistical properties
4. **Data Pre-Processing**: Select, clean, and transform the data to prepare it for analysis
5. **In-Depth Analysis**: Feed data into modelling frameworks, test the model, evaluate results iteratively
6. **Communicate Results**: Create reports/presentations, ready the model for deployment
### Python Tools
- **Data Collection** *(Used in stage 2)*:
	- `Scrapy` (web crawling/APIs), `BeautifulSoup` (web scraping without APIs)
- **Numerical Computation** *(Used in stages 3 and 5)*:
	- `NumPy` (numerical computation, underlies other libraries), `SciPy` (scientific/technical computation)
- **Data Manipulation, Analysis and Visualisation** *(Used in stages 3, 4, and 6)*:
	- `Pandas` (analysis/cleaning), `Matplotlib` (visualisation, underlies other viz libraries)
- **Machine Learning and Deep Learning** *(Used in stage 5)*:
	- `Scikit-learn` (ML: clustering, classification, regression), `TensorFlow`/`Keras` (deep learning)
---
## Related

## Covered in
- [[CS2PP_week_01_lecture.pdf]]
