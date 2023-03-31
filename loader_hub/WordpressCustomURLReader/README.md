# Wordpress Custom URL Loader

This loader fetches the text from the given Wordpress Custom URL using the Wordpress API. It also uses the BeautifulSoup library to parse the HTML and extract the text from the articles.

## Usage

To use this loader, you need to pass full Custom URL of the Wordpress installation (e.g. `https://www.mysite.com/wp-json/wp/v2/custom`), a username, and an application password for the user (more about application passwords [here](https://www.paidmembershipspro.com/create-application-password-wordpress/))

```python
from llama_index import download_loader

WordpressCustomURLReader = download_loader("WordpressCustomURLReader")

loader = WordpressCustomURLReader(url="https://www.mysite.com/wp-json/wp/v2/custom", username="my_username", password="my_password")
documents = loader.load_data()
```

This loader is designed to be used as a way to load data into [LlamaIndex](https://github.com/jerryjliu/gpt_index/tree/main/gpt_index) and/or subsequently used as a Tool in a [LangChain](https://github.com/hwchase17/langchain) Agent. See [here](https://github.com/emptycrown/llama-hub/tree/main) for examples.
