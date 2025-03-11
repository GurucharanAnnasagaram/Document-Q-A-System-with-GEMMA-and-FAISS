PDF Document Processing & Vector Search

Uses PyPDFDirectoryLoader to load PDFs from a directory.
Splits text into 1000-character chunks with 200-character overlap using RecursiveCharacterTextSplitter.
Embeds text using Google Generative AI Embeddings (models/embedding-001).
Stores vector embeddings in FAISS, allowing fast similarity searches.
Question Answering with GEMMA-2 (Groq API)

Accepts user queries via Streamlit UI.
Retrieves relevant document chunks from FAISS.
Passes retrieved text and query to GEMMA-2 9B IT (Groq API) for generating an accurate response.
Interactive UI with Streamlit

Users can initialize the vector store and ask document-related questions.
Displays retrieved document snippets for reference.
Technologies Used:
Groq API (GEMMA-2 9B IT) – LLM for answering questions.
FAISS – Vector search for document retrieval.
Google Generative AI Embeddings – Converts text into numerical embeddings.
LangChain – Manages retrieval and response generation.
PyPDFDirectoryLoader – Loads and processes PDFs.
Streamlit – Interactive web UI.
Workflow:
User uploads PDFs → System loads & splits text.
Vector embeddings are created using Google Generative AI Embeddings.
FAISS indexes and stores document vectors.
User enters a question → System retrieves relevant document snippets.
Groq (GEMMA-2 9B IT) processes the question & retrieved text.
Answer is displayed, along with relevant document excerpts.
