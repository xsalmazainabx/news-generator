# news-generator
import requests
import json
query= input("what type of news are you intrested in?")
url=f"https://newsapi.org/v2/everything?q={query}&from=2023-12-27&sortBy=publishedAt&apiKey=8035f6613df448a598f29e6b9c65dd2d"
r=requests.get(url)
news=json.loads(r.text)
print(news)
for article in news["articles"]:
  print(article["title"])
  print(article["description"])
  print("--------------------------------------")
