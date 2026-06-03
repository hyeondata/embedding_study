# 🚀 임베딩 모델 기초 학습 가이드 (Embedding Models Study Guide)

이 저장소는 **임베딩(Embedding)**의 기초 개념부터 실무 활용, 그리고 최신 모델까지 체계적으로 학습하기 위한 공간입니다.

## 📌 1. 임베딩(Embedding)이란?

임베딩은 텍스트, 이미지, 오디오 등의 비정형 데이터를 컴퓨터가 이해할 수 있는 **숫자의 배열(벡터, Vector)**로 변환하는 기술입니다.
유사한 의미를 가진 데이터(예: 비슷한 뜻의 단어나 문장)는 다차원 벡터 공간 상에서 서로 가까운 거리에 위치하게 됩니다.

- **핵심 목적**: 컴퓨터가 인간의 언어(의미와 문맥)를 수학적으로 계산하고 비교할 수 있게 만드는 것.

---

## 🎯 2. 학습 로드맵 (Study Roadmap)

### 🟢 1단계: 전통적인 텍스트 표현 방식 (NLP 기초)

- [ ] One-hot Encoding
- [ ] Bag of Words (BoW)
- [ ] TF-IDF (Term Frequency-Inverse Document Frequency)
- *학습 포인트: 단어 빈도수 기반 모델의 한계점 (의미/문맥 반영 불가, 차원의 저주, 희소 벡터 문제)*

### 🟡 2단계: 단어 임베딩 (Static Word Embeddings)

- [ ] **Word2Vec** (CBOW, Skip-gram)
- [ ] **GloVe** (Global Vectors for Word Representation)
- [ ] **FastText** (Subword 기반 임베딩 - OOV(Out-Of-Vocabulary) 문제 해결)
- *학습 포인트: 밀집 벡터(Dense Vector)의 도입. 단, 동음이의어(다의어)를 문맥에 따라 구분하지 못한다는 한계점.*

### 🟠 3단계: 문맥을 이해하는 임베딩 (Contextualized Embeddings)

- [ ] **Transformer** 아키텍처 기초 (Self-Attention Mechanism)
- [ ] **BERT** (Bidirectional Encoder Representations from Transformers)
- *학습 포인트: 같은 "배(Ship, Pear, Stomach)"라는 단어도 문맥에 따라 다른 벡터 값을 가지게 됨.*

### 🔴 4단계: 문장/문서 임베딩 및 최신 모델 (Sentence/Document Embeddings)

- [ ] **Sentence-BERT (SBERT)**: 문장 단위 임베딩과 의미론적 검색(Semantic Search) 모델
- [ ] 최신 임베딩 모델 트렌드 파악
  - 상용 API: OpenAI (`text-embedding-3`), Cohere, Google Vertex AI
  - 오픈소스(Local): BGE(BAAI), E5(Microsoft), Nomic-Embed 등
- [ ] **MTEB (Massive Text Embedding Benchmark)** 리더보드 보는 법

### 🟣 5단계: 벡터 검색과 실무 응용 (Vector Search & Applications)

- [ ] 벡터 유사도 측정 방법 (Cosine Similarity, Dot Product, L2 Distance)
- [ ] **Vector Database (VDB)** 기초 (FAISS, ChromaDB, Milvus, Qdrant 등)
- [ ] **RAG (Retrieval-Augmented Generation)** 시스템 구축 기초 (LLM과 임베딩 결합)

---

## 💻 3. 실습 환경 세팅

Python 기반의 실습을 위해 가상환경을 구성하고 필요한 라이브러리를 설치합니다.

```bash
# 가상환경 생성 및 활성화
python -m venv venv
source venv/bin/activate  # Mac/Linux

# 필수 라이브러리 설치 (예시)
pip install numpy pandas scikit-learn
pip install torch transformers sentence-transformers
pip install chromadb
```

## 📚 4. 추천 참고 자료 (References)

- [Hugging Face NLP Course](https://huggingface.co/course/chapter1/1)
- [Sentence-Transformers 공식 문서](https://www.sbert.net/)
- [MTEB Leaderboard (Hugging Face)](https://huggingface.co/spaces/mteb/leaderboard)
- [Pinecone Vector Embeddings Guide](https://www.pinecone.io/learn/vector-embeddings/)

---
> 💡 **Tip:** 학습을 진행하면서 각 단계별 개념 정리(Markdown)와 실습 코드(Jupyter Notebook `.ipynb` 또는 Python `.py`)를 이 디렉토리에 추가하며 나만의 지식 저장소를 만들어 보세요!
