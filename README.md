# TEXT-SUMMARIZATION-TOOL
COMPANY : CODTECH IT SOLUTIONS NAME : PAIDIPELLI BHEEMRAJ ID : CT06DF373 DOMAIN : ARTIFICIAL INTELLIGENCE DURATION : 6 WEEKS MENTOR : NEELA SANTHOSH KUMAR
 Text Summarization Tool
------------------------

Overview:
---------
This project implements a command-line text summarizer using the BART (Bidirectional and Auto-Regressive Transformers) model 
from Facebook AI. It leverages the 'facebook/bart-large-cnn' pretrained model from Hugging Face Transformers to generate 
coherent, concise summaries from long text input.

Key Features:
-------------
- Uses BART transformer for high-quality abstractive summarization
- Accepts multi-line input directly in the terminal
- Dynamically adjusts summary length based on input size
- Adds slight randomness to output length for variation
- Supports summarizing large blocks of text (up to 1024 tokens)

Technologies Used:
------------------
- Python 3.7+
- Hugging Face Transformers
- PyTorch

Installation Instructions:
--------------------------
1. Make sure Python 3 is installed.

2. Install the required libraries:
   pip install transformers torch

3. Run the script:
   python bart_summarizer.py

Usage:
------
- When prompted, paste or type the content you want summarized.
- Press Enter twice (a blank line) to end input.
- The tool will analyze the input length and generate a summary.

Example:
--------
Input:
-------
  Enter the text to summarize (end input with a blank line):
  Artificial intelligence is transforming industries by automating tasks, analyzing data,
  and enabling smarter decision-making processes. Many companies use AI-powered systems
  to improve customer service, enhance supply chain logistics, and develop innovative products.

  [Press Enter again]

Output:
--------
  Summary:

  Artificial intelligence is revolutionizing industries by automating tasks, analyzing data,
  and enabling smarter decisions. Companies use AI to improve customer service,
  logistics, and innovation.

Input Guidelines:
-----------------
- Minimum input: 10 words
- Maximum length: Approx. 1024 tokens (truncated if exceeded)
- Longer input = more informative summaries

Advanced Notes:
---------------
- The summarizer uses beam search (num_beams=4) for better quality.
- Summary length is adjusted based on input size with small random variation:
    - Short text: 15–30 words
    - Medium text: 30–100 words
    - Long text: up to 130–150 words
- You can modify parameters like min_length, max_length, num_beams in the source code.

Limitations:
------------
- Requires internet to download the model the first time.
- May be slow on CPU — GPU is recommended for large inputs.
- Input longer than 1024 tokens will be truncated.

Author:
Bheemrajpaidipelli
