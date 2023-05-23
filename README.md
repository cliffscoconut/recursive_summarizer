# PDF Summarizer
Using a GPT API key and a PDF file, get a summary of the text in the PDF file by prompting the GPT model. 

The summarizer, if necessary, first breaks the PDF text into smaller chunks for the GPT API to process due to the 4096 token limit on GPT-3.5-Turbo model. After each section is summarized, the summaries will be recursively summarized. When only one section remains, it will be returned as the output. 

## Parameters
The main parameters to play with are the following:
 (1) temperature - control the tightness or looseness of the summarization. A tighter temperature has a lower value and will generate more reproducible results.
 (2) max tokens - the number of max tokens the summary will contain. If the task is not finished, it will cut off at the max token limit. 
 (3) section_size - the number of tokens to submit to GPT API per request. 