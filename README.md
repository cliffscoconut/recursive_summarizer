# PDF Summarizer
This program automatically extracts text from PDF files and summarizes the content using OpenAI's GPT-4 model. It's designed to handle large documents by breaking them into sections, summarizing each section, and then recursively summarizing the results to generate a concise summary.

The summarizer, if necessary, first breaks the PDF text into smaller chunks for the GPT API to process due to the 4096 token limit on GPT-3.5-Turbo model. After each section is summarized, the summaries will be recursively summarized. When only one section remains, it will be returned as the output. 

## Parameters
The main parameters to play with are the following:
 (1) temperature - control the tightness or looseness of the summarization. A tighter temperature has a lower value and will generate more reproducible results.
 (2) max tokens - the number of max tokens the summary will contain. If the task is not finished, it will cut off at the max token limit. 
 (3) section_size - the number of tokens to submit to GPT API per request. 


## Features

- Extracts text from PDF files using PyPDF2.
- Summarizes text using OpenAI's GPT-4.
- Handles large documents by recursive summarization.
- Tokenization and detokenization of text using NLTK and sacremoses.

## Installation

Clone the repository and navigate to the project directory:

In terminal: 

git clone https://github.com/your-github-username/pdf-summarizer.git
cd pdf-summarizer

## Set up a virtual environment
python3 -m venv venv
source venv/bin/activate  # On Windows use `venv\Scripts\activate`

## Install required packages
pip install -r requirements.txt

## Load GPT API Key
Create .env file and add: 
OPENAI_API_KEY="your_secret_key_here"

## Add filepath to your pdf file
pdf_path = "path to your pdf file"

## Usage:
Run the program
python3 gpt_summarizer.py
