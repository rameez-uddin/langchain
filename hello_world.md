# download the packages above:

```python

# Ensure 'langchain_google_genai' is correctly installed:
!pip install langchain-google-genai --quiet
```
# import the module:

```python
# Import the module:
import langchain_google_genai as genai
```
## also import this:

```python
from langchain_google_genai import ChatGoogleGenerativeAI
```
# configure the api key:

```python
from google.colab import userdata
GEMINI_API_KEY = userdata.get('GEMINI_API_KEY')
```
# create an instance of the chat model:

```python
model : ChatGoogleGenerativeAI = ChatGoogleGenerativeAI(
    model = "gemini-1.5-flash",
    api_key = "AIzaSyDEumTmPqtrGYO2pgCLWrQFmIMQUa6rAig"
)
```
# now fetch the response:
```python
response1 = model.invoke("What is the capital of France?")
print(response1.content)
```