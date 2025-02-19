# AI Search Assistant 

## Hello Human 👋🤖

This project is an **AI-powered search assistant** that determines whether a query requires a web search, generates an optimized search query, retrieves and validates results from **DuckDuckGo**, and provides a final AI-generated response based on the best available information.  

The assistant uses **Ollama** for AI-powered chat capabilities, **BeautifulSoup & Trafilatura** for web scraping, and **Colorama** for terminal color formatting.



## Features  

- **Intelligent Search Decision**: Determines if a web search is necessary for the user's query.  
- **Automated Query Generation**: Converts user input into an optimized search query.  
- **DuckDuckGo Integration**: Searches the web for relevant results.  
- **Best Result Selection**: AI picks the most relevant search result for scraping.  
- **Web Scraping & Validation**: Extracts and verifies useful data from web pages.  
- **AI-Powered Response**: Generates a conversational response using retrieved data (if available).  
- **Context Handling**: If no valid data is found, the assistant asks the user how to proceed.



## Dependencies  

Ensure you have the following Python libraries installed:  

```bash
pip install -r requirements.txt

```

---

## How It Works  

### **1. User Input Handling**  
- The assistant starts by taking user input.  

### **2. Search Decision**  
- Determines if the input requires a web search using `search_or_not()`.  

### **3. Query Generation**  
- If needed, the AI generates an optimized search query using `query_generator()`.  

### **4. Web Search Execution**  
- DuckDuckGo is queried for search results via `duckduckgo_search()`.  

### **5. Best Search Result Selection**  
- AI selects the most relevant result using `best_search_results()`.  

### **6. Web Scraping & Data Validation**  
- The selected webpage is scraped using `scrape_webpage()`.  
- AI determines if the extracted data is relevant using `contains_data_needed()`.  

### **7. AI Response Generation**  
- If valid data is found, it is used to generate a final response.  
- If no relevant data is found, the assistant asks the user how to proceed.  

### **8. Streaming AI Response**  
- The assistant provides a streamed response using `stream_assistant_reponse()`.  

---

## How to Run  

To start the assistant, run the following command in your terminal:  

```bash
python search_agent.py
```

The assistant will prompt you for input and generate responses in real-time.

---

## Example Usage  

```bash
Human USER:
What is the latest AI breakthrough in 2025?
```

**Assistant Response (Scenario 1 - Search Required & Data Found):**  

```bash
AI assistant:
I found recent information on AI breakthroughs in 2025. 
Here’s a summary: …
```

**Assistant Response (Scenario 2 - Search Required & No Data Found):**  

```bash
AI assistant:
I couldn't find relevant information. Would you like me to search again or respond without web context?
```

---

## Customization  

You can modify:  

- **sys_msgs.py**: To adjust AI system prompts.  
- **Search engine**: Replace DuckDuckGo with another provider if needed.  
- **Query logic**: Improve the query generation logic for better search results.  

---


## License  

This project is open-source. Feel free to modify and distribute it as needed.

---

## Author  

Developed by ***Khouloud Ben Cheikh***. Contributions welcome! 🚀
