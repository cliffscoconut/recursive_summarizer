# Recursive Summarizer

The Recursive Summarizer is an advanced tool designed to automatically extract text from PDF files and summarize the content using OpenAI's GPT-4 model. Tailored for handling large documents, it breaks the document into smaller sections for manageable processing and utilizes a recursive approach to summarize these sections, ensuring a concise and comprehensive summary.

## Features

- **Text Extraction**: Leverages PyPDF2 for efficient text extraction from PDF files.
- **GPT-4 Summarization**: Utilizes the cutting-edge capabilities of OpenAI's GPT-4 for accurate and context-aware summarization.
- **Recursive Approach**: Implements a novel recursive summarization strategy, breaking the document into sections and summarizing these sections step-by-step to produce a final summary.
- **Customizable Parameters**: Allows users to fine-tune the summarization process through adjustable parameters like section size and overlap.
- **NLTK and Sacremoses Integration**: Employs NLTK for tokenization and Sacremoses for detokenization, maintaining high linguistic quality.

## Parameters

Key parameters for customization include:
- `section_tokens`: The size of text sections (in tokens) for processing, with a default of 3000 tokens.
- `overlap_size`: The token overlap between sections to maintain context continuity, set to 150 tokens by default.

## Installation

1. **Clone the Repository:**

    ```bash
    git clone https://github.com/cliffscoconut/recursive_summarizer.git
    cd recursive_summarizer
    ```

2. **Set Up a Virtual Environment:**

    ```bash
    python3 -m venv venv
    source venv/bin/activate  # On Windows use `venv\Scripts\activate`
    ```

3. **Install Required Packages:**

    ```bash
    pip install -r requirements.txt
    ```

4. **Configure OpenAI API Key:**

    - Create a `.env` file at the project root.
    - Add your OpenAI API key:
        ```
        OPENAI_API_KEY="your_secret_key_here"
        ```

5. **Specify Your PDF Path:**

    - Update the `pdf_path` variable in the script to point to your target PDF file.

## Usage

To run the program and summarize your PDF document:

```bash
python3 gpt_summarizer.py
