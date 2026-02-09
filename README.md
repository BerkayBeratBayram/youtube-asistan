# YouTube Asistan

Ben bu projede bir YouTube videosunun transcriptini alip parcalayarak ChromaDB'ye kaydeden ve sonra Ollama ile soru-cevap yapan bir asistan kurdum. Tum is akisi notebook icinde, hucreleri sirasiyla calistirarak ilerliyorum.

## Kullandiklarim

- youtube_transcript_api: YouTube altyazisini cekmek icin
- chromadb: vektor veritabani
- sentence-transformers (Chroma embedding fonksiyonu icin)
- langchain_text_splitters: metni parcalamak icin
- ollama: lokal LLM ile yanit uretmek icin
- re ve datetime: kucuk yardimci isler

## Kurulum

```bash
python -m venv venv
venv\Scripts\Activate.ps1
pip install youtube-transcript-api chromadb sentence-transformers langchain-text-splitters ollama
```

## Calistirma

1. Jupyter ile youtube_asistan.ipynb dosyasini aciyorum.
2. Hucreleri yukaridan asagi dogru tek tek calistiriyorum.
3. Ornek soru ile arama yapip Ollama cevabini aliyorum.

## Notlar

- Video altyazisi yoksa transcript cekilemez.
- Ollama icin lokal sunucu calisir durumda olmali.

---

# English

I built this project as a YouTube assistant that pulls a video transcript, splits it into chunks, stores them in ChromaDB, and answers questions with a local Ollama model. The whole flow lives in the notebook, so I run the cells top to bottom.

## What I Use

- youtube_transcript_api: fetches YouTube subtitles
- chromadb: vector database
- sentence-transformers (for Chroma embeddings)
- langchain_text_splitters: text chunking
- ollama: local LLM responses
- re and datetime: small helpers

## Setup

```bash
python -m venv venv
venv\Scripts\Activate.ps1
pip install youtube-transcript-api chromadb sentence-transformers langchain-text-splitters ollama
```

## Run

1. Open youtube_asistan.ipynb in Jupyter.
2. Run cells from top to bottom.
3. Ask a test question and get an Ollama answer.

## Notes

- If a video has no subtitles, the transcript step fails.
- Ollama needs to be running locally.
