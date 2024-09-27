# NLP-Mini-Project-Ni-Jin
## link to your GIT code repository
https://git.arts.ac.uk/21033182/NLP-Mini-Project-Ni-Jin

## Background
This project is a mini project of the course IU000131: Natural Language Processing for the Creative Industries.

Using different models and methods based on NLP techniques, this project uses joke text to machine learn and generate short jokes and matches the generated joke text with the description text of memes to eventually match the most relevant meme images. As a follow-up task, I will use Tracery to develop a self-hosted Twitter bot @meirl_meme_bot to tweet the generated joke text together with the meme image.

### Project process:
 
### The goals for this repository are:
1. a runtime file for crawling the knowyourmemes.com website and saving the data locally
2. a file for data cleaning.
3. three files for text generation (using LSTM, TEXTGENRNN, and GPT-2 respectively)
4. two-run files for memes matching (using TF/IDF, SVD respectively)
5. a Readme.pdf file
6. some text-generated result files

## Install
The project needs to be opened using Jypyter in anaconda. To run it you need to ensure that you have downloaded python3 and the supported python libraries (I am using python version python3.10.7). 

If you do not have them installed locally, check them.

Please do not delete the data and textgenrnn folders and their contents, otherwise, you may get a runtime error.

## Usage
1. Open the Scraping_meme_description.ipynb file and run it. This is used to crawl meme information on knowyourmemes.com.

You can change the page =10 line of code to determine how many pages of memes to crawl, please note: when the parameter is too large, it will take a long time!

2. Open the clean_dataset.ipynb file and run it. This is used for dirty data cleaning

3. Open the LSTM_generate.ipynb file and run it locally for text generation.
You can modify maxlen,step,num_neurons,epoch,batch_size,temperature and other parameters to change the effect of text generation.
Note: LSTM_generate_colab.ipynb is used to run in colab.
You can also use the files LSTM_genrnn.ipynb and GPT_2_generate.ipynb for this step. They use textgenrnn and GPT-2 for text generation respectively.
Note: Before GPT-2 can be run you will need to download the GPT-2 support package locally on huggingface and change the path

4. open the similarity_match_TFIDF. ipynb file and run it. This is used to match the joke text to the meme image. You can modify the joke file for testing.
You can also run it using similarity_match_LDA_SVD. ipynb, but the results of matching in this way are not very good.

### Other.
Genrnn_output_jokes.txt is a collection of 20 jokes generated using genrnn.
Knowyourmemes.txt is the address of the meme that was grabbed, and when the code is run, its original content is overwritten.
Bad_words.csv is the data used to clean up the dirty data
clean_shortjokes.txt is the result of the cleaning and is an important file for the machine learning part of my project
joketest.txt and joketest.csv are used to test the text against meme matching AI generated jokes
LSTM_Generate_XX.csv is the joke generated using different parameters
LSTM_Generate_dirty.csv is a joke generated using the original dataset (with dirty data)
memesinfos.csv is a dataset of memes messages grabbed using beautifulsoup
shortjokes.csv is the original dataset
The data in the LSTM_colab_output file is the jokes generated by running LSTM_generate_colab.ipynb with colab (using different parameters)

## Maintainers
Ni Jin @https://git.arts.ac.uk/21033182

## Contributing
Credit for the references used and the existence of the project goes to all those who contributed to it.

Request: https://pypi.org/project/requests/
Bs4: https://www.crummy.com/software/BeautifulSoup/bs4/doc/
Pandas: https://pandas.pydata.org/
Numpy: https://numpy.org/
Ixml: https://lxml.de/
Keras: https://keras.io/api/layers/recurrent_layers/lstm/
Gpt-2 recourse in huggingface: https://huggingface.co/gpt2/tree/main
Genrnn: github.com/minimaxir/textgenrnn.git
Pytorch_transformers1.0: https://pypi.org/project/pytorch-transformers/
NLTK: https://www.nltk.org/
scikit-learn : https://scikit-learn.org/stable/index.html

## License
Berkeley Software Distribution @Ni Jin
