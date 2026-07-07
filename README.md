# 🧩 Tokenizer Comparison using Hugging Face

A Natural Language Processing (NLP) project that demonstrates the implementation, training, and comparison of three popular subword tokenization algorithms:

- 🔹 Byte Pair Encoding (BPE)
- 🔹 WordPiece
- 🔹 Unigram

All three tokenizers are trained using the **same corpus** to provide a fair comparison of their vocabulary generation and tokenization behavior.

---

## 📌 Project Overview

Tokenization is one of the most important preprocessing steps in NLP. Different tokenization algorithms break text into subword units in different ways, directly impacting downstream language models.

This project trains and compares:

- **BPE (Byte Pair Encoding)** using Hugging Face Tokenizers
- **WordPiece** using Hugging Face Tokenizers
- **Unigram** using SentencePiece

The tokenizers are trained on the same cleaned text corpus extracted from **Pride and Prejudice** by Jane Austen (Project Gutenberg).

---

## 🚀 Features

- Train a BPE tokenizer
- Train a WordPiece tokenizer
- Train a Unigram tokenizer
- Preprocess and clean raw text
- Build a common training corpus
- Compare tokenization outputs
- Compare vocabulary sizes
- Display token IDs
- Save trained tokenizer models

---

## 📂 Dataset

**Source:** Project Gutenberg

**Book Used:** *Pride and Prejudice* by Jane Austen

The text corpus is:
- converted to lowercase
- cleaned by removing punctuation and special characters
- whitespace normalized
- used as the common training corpus for all tokenizers

---

## 🛠 Technologies Used

- Python 3
- Google Colab
- Hugging Face Tokenizers
- SentencePiece
- Regular Expressions (re)

---

## 📦 Libraries

```bash
pip install tokenizers
pip install sentencepiece
```

---

## 📁 Project Structure

```
Tokenizer-Comparison/
│
├── Tokenizer_Comparison.ipynb
├── corpus5000.txt
├── bpe_tokenizer.json
├── wordpiece_tokenizer.json
├── unigram.model
├── unigram.vocab
├── README.md
```

---

## ⚙️ Workflow

### 1. Load Dataset

- Read text from Project Gutenberg
- Remove Project Gutenberg header/footer

### 2. Text Preprocessing

- Convert text to lowercase
- Remove punctuation
- Remove numbers
- Normalize whitespace

### 3. Create Training Corpus

- Generate a cleaned corpus
- Use the same corpus for all three tokenizers

### 4. Train Tokenizers

- BPE
- WordPiece
- Unigram

### 5. Test Tokenizers

Tokenize sample sentences and compare:

- Tokens
- Token IDs
- Vocabulary size

---

## 📊 Example Output

### Input Sentence

```
Elizabeth Bennet loves reading books.
```

### BPE

```
['elizabeth', 'bennet', 'love', 's', 'read', 'ing', 'book', 's']
```

### WordPiece

```
['elizabeth', 'bennet', 'love', '##s', 'read', '##ing', 'book', '##s']
```

### Unigram

```
['▁elizabeth', '▁bennet', '▁love', 's', '▁read', 'ing', '▁book', 's']
```

*Note: Actual output depends on the trained vocabulary size and corpus.*

---

## 📈 Comparison

The project compares:

- Vocabulary Size
- Tokenization Strategy
- Token IDs
- Unknown Tokens (`[UNK]`)
- Subword Segmentation

---

## 📚 Learning Outcomes

Through this project, you will understand:

- Why subword tokenization is used
- Differences between BPE, WordPiece, and Unigram
- How Hugging Face Tokenizers work
- How SentencePiece implements Unigram
- The impact of vocabulary size on tokenization
- The effect of corpus size and preprocessing on tokenizer performance

---

## 📖 References

- Hugging Face Tokenizers Documentation  
  https://huggingface.co/docs/tokenizers

- SentencePiece Documentation  
  https://github.com/google/sentencepiece

- Project Gutenberg  
  https://www.gutenberg.org/

---

## 👩‍💻 Author

**Nishitha Sathish**

Computer Science Engineering Student

GitHub: https://github.com/<your-username>

---

## ⭐ Future Improvements

- Train on larger corpora
- Compare tokenizer training time
- Measure compression efficiency
- Visualize vocabulary growth
- Evaluate tokenizers on unseen text
- Benchmark against pretrained BERT and GPT tokenizers

---

## 📜 License

This project is intended for educational and research purposes.
