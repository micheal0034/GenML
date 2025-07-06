- [x] Create project folder + Git repo
- [ ] Download and inspect sample chunk JSON
- [ ] Create and fill out the time estimation CSV (first commit)
- [ ] Set up virtual environment and dependencies (fastapi, uvicorn, weaviate-client, sentence-transformers, etc.)
- [ ] Define high-level file structure (api/, ingestion/, db/, models/, etc.)

📥 1. Ingestion Pipeline (Design + Code)
- [ ] Implement file detection (simulate or hard-code for now)
- [ ] Write chunking logic (split by heading/token size)
- [ ] Add metadata to each chunk
- [ ] Generate embeddings
- [ ] Write to vector DB (e.g., Weaviate or FAISS)
- [ ] Write pseudocode version for submission
- [ ] Document vector DB choice in markdown

🌐 2. API Development
- [ ] /api/upload → Ingest chunks, embed, store
- [ ] /api/similarity_search → Search vector DB with semantic query
- [ ] /api/<journal_id> → Return all chunks & metadata for a document
- [ ] Add OpenAPI docs via FastAPI

🧪 3. Testing and Validation
- [ ] Use Postman or curl to test all 3 endpoints
- [ ] Load sample JSON and perform a search query
- [ ] Log or print matched chunks with citation info

🎥 4. Deliverables
- [ ] Record Loom video:
- [ ] Upload JSON
- [ ] Run /similarity_search
- [ ] Show chatbot-style output (manual or scripted)
- [ ] Write README.md with:
- [ ] Setup instructions
- [ ] Vector DB explanation
- [ ] Optional features list
- [ ] Zip the repo or push to GitHub

🌟 5. Optional Stretch Features (Choose 1–2 if time permits)
- [ ] Basic frontend: React + fetch to backend
- [ ] Update usage_count on each chunk access
- [ ] Add a /summarize or /compare endpoint
- [ ] Add unit tests for ingestion or search logic






genai-research-assistant/
│
├── api/                  # FastAPI route handlers
│   ├── upload.py
│   ├── search.py
│   └── journal.py
│
├── ingestion/            # File polling, chunking, embedding
│   ├── file_watcher.py
│   ├── chunker.py
│   ├── embedder.py
│   └── vector_store.py
│
├── db/                   # DB setup, usage tracking
│   └── weaviate_client.py
│
├── models/               # Pydantic models
│   └── chunk.py
│
├── tests/                # Unit and integration tests
│
├── sample_data/          # Pre-chunked JSON samples
│   └── mucuna_sample.json
│
├── main.py               # FastAPI app entrypoint
├── requirements.txt      # Python dependencies
├── README.md
└── time_estimates.csv    # Estimation vs actual tracker
