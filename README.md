🧠 Abstractive Summarization & Named Entity Recognition (NER) on Twitter Data
This project performs Named Entity Recognition (NER) and abstractive summarization on tweets using transformer-based models like BERTweet for NER and Pegasus for summarization. The goal is to analyze and condense large volumes of tweets into concise summaries while identifying key entities.

🚀 Features
🏷️ Named Entity Recognition using fine-tuned BERTweet model

📝 Abstractive Summarization using Pegasus (google/pegasus-xsum)

🧹 Robust tweet cleaning and preprocessing (removes links, emojis, usernames, etc.)

📅 Filter tweets by date and summarize daily tweet content

📤 Exports processed results to CSV

📁 Project Structure
bash
Copy
Edit
Abstractive-summarization-and-NER-of-Twitter-dataset/
├── notebook.ipynb          # Main notebook with complete pipeline
├── dataset.csv             # Input dataset (Twitter data)
└── latest_download.csv     # Output CSV after NER tagging
🛠️ Requirements
Install dependencies:

bash
Copy
Edit
pip install transformers==4.6.0
pip install torch==1.8.2+cu111 torchvision==0.9.2+cu111 torchaudio===0.8.2 -f https://download.pytorch.org/whl/lts/1.8/torch_lts.html
pip install emoji sentencepiece pandas matplotlib seaborn scikit-learn
▶️ How to Run
Clone the repository:

bash
Copy
Edit
git clone https://github.com/moaaz12-web/Abstractive-summarization-and-NER-of-Twitter-dataset.git
cd Abstractive-summarization-and-NER-of-Twitter-dataset
Open notebook.ipynb in Jupyter Notebook or Google Colab.

Upload dataset.csv if not already present.

Run all cells to:

Clean and preprocess the tweet text

Run NER with BERTweet

Generate summaries with Pegasus

Export results to latest_download.csv

💡 How It Works
Named Entity Recognition (NER)
Uses TweebankNLP/bertweet-tb2_wnut17-ner

Extracts entities like Person, Organization, Location, etc. from each tweet

Stores results in a column named Entities

Summarization
Uses google/pegasus-xsum

Summarizes all tweets of a specific day into 1-2 lines

Designed for highly abstractive summarization

📥 Input
CSV file with columns: tweet_text and tweet_date

Example:

csv
Copy
Edit
tweet_text,tweet_date
"@user Amazing update! 😍 Check this out: https://t.co/xyz",2022-09-24
📤 Output
Cleaned tweet text

Named entities extracted

Final summary of tweets for selected dates

CSV export: latest_download.csv

📌 Sample Output
json
Copy
Edit
{
  "Text": "Amazing update! Check this out",
  "Entities": [{"word": "update", "entity": "O"}],
  "Date": "2022-09-24"
}
Daily Summary:

"Exciting new developments were shared and discussed."
