# Blog Post Generator

This project is a Python-based workflow for generating high-quality blog posts on a given topic. It uses the phidata library & Agentic AI to search for relevant articles and generate a blog post based on those articles.

## Features
* Search for Articles: Uses DuckDuckGo to search for articles on a given topic.
* Generate Blog Post: Creates a well-structured blog post based on the top articles found.
* Caching: Option to use cached blog posts to avoid redundant searches and generation.
## Requirements
* Python 3.8+
* pydantic
* phidata
* dotenv
## Installation
1. Clone the repository:
```
git clone <repo-url>
cd <repo-dir>
```

2. Install the required packages:
```
pip install -r requirements.txt
```

3. Set up environment variables:
* Create a .env file in the root directory.
* Add your API key for the Gemini model:
```
MODEL_API_KEY=your_api_key_here
```
## Usage
1. Run the script:
```
python blog_post_generator.py
```

2. Enter the topic when prompted:
```
Enter Topic: <your_topic_here>
```
3. The script will search for articles and generate a blog post. The response will be printed in markdown format.

## Code Overview

### NewsArticle Model
Defines the structure of a news article with fields for the title, URL, and an optional summary.

### SearchResults Model
Contains a list of NewsArticle objects.

### BlogPostGenerator Workflow
* Searcher: An agent that uses the Gemini model and DuckDuckGo to find relevant articles.
* Writer: An agent that generates a blog post based on the articles found.
* Run Method: Executes the workflow, searches for articles, and generates the blog post. It also handles caching of blog posts.
  
## License
The project is licensed under MIT License,
