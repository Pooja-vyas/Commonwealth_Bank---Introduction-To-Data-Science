```python
!pip install ntscraper
```

    Collecting ntscraper
      Obtaining dependency information for ntscraper from https://files.pythonhosted.org/packages/7d/3f/026f5c95eff8761f4f0dd8e6cce80ea034351cf4886cebbbb546d9456f4e/ntscraper-0.3.13-py3-none-any.whl.metadata
      Downloading ntscraper-0.3.13-py3-none-any.whl.metadata (6.7 kB)
    Requirement already satisfied: requests in c:\users\sompurapooja32\anaconda3\lib\site-packages (from ntscraper) (2.31.0)
    Requirement already satisfied: beautifulsoup4 in c:\users\sompurapooja32\anaconda3\lib\site-packages (from ntscraper) (4.12.2)
    Requirement already satisfied: lxml in c:\users\sompurapooja32\anaconda3\lib\site-packages (from ntscraper) (4.9.3)
    Requirement already satisfied: soupsieve>1.2 in c:\users\sompurapooja32\anaconda3\lib\site-packages (from beautifulsoup4->ntscraper) (2.4)
    Requirement already satisfied: charset-normalizer<4,>=2 in c:\users\sompurapooja32\anaconda3\lib\site-packages (from requests->ntscraper) (2.0.4)
    Requirement already satisfied: idna<4,>=2.5 in c:\users\sompurapooja32\anaconda3\lib\site-packages (from requests->ntscraper) (3.4)
    Requirement already satisfied: urllib3<3,>=1.21.1 in c:\users\sompurapooja32\anaconda3\lib\site-packages (from requests->ntscraper) (1.26.16)
    Requirement already satisfied: certifi>=2017.4.17 in c:\users\sompurapooja32\anaconda3\lib\site-packages (from requests->ntscraper) (2023.7.22)
    Downloading ntscraper-0.3.13-py3-none-any.whl (11 kB)
    Installing collected packages: ntscraper
    Successfully installed ntscraper-0.3.13
    


```python
pip install textblob
```

    Collecting textblob
      Obtaining dependency information for textblob from https://files.pythonhosted.org/packages/02/07/5fd2945356dd839974d3a25de8a142dc37293c21315729a41e775b5f3569/textblob-0.18.0.post0-py3-none-any.whl.metadata
      Downloading textblob-0.18.0.post0-py3-none-any.whl.metadata (4.5 kB)
    Requirement already satisfied: nltk>=3.8 in c:\users\sompurapooja32\anaconda3\lib\site-packages (from textblob) (3.8.1)
    Requirement already satisfied: click in c:\users\sompurapooja32\anaconda3\lib\site-packages (from nltk>=3.8->textblob) (8.0.4)
    Requirement already satisfied: joblib in c:\users\sompurapooja32\anaconda3\lib\site-packages (from nltk>=3.8->textblob) (1.2.0)
    Requirement already satisfied: regex>=2021.8.3 in c:\users\sompurapooja32\anaconda3\lib\site-packages (from nltk>=3.8->textblob) (2022.7.9)
    Requirement already satisfied: tqdm in c:\users\sompurapooja32\anaconda3\lib\site-packages (from nltk>=3.8->textblob) (4.65.0)
    Requirement already satisfied: colorama in c:\users\sompurapooja32\anaconda3\lib\site-packages (from click->nltk>=3.8->textblob) (0.4.6)
    Downloading textblob-0.18.0.post0-py3-none-any.whl (626 kB)
       ---------------------------------------- 0.0/626.3 kB ? eta -:--:--
       ---------------------------------------- 0.0/626.3 kB ? eta -:--:--
        --------------------------------------- 10.2/626.3 kB ? eta -:--:--
       -- ------------------------------------ 41.0/626.3 kB 495.5 kB/s eta 0:00:02
       ---- ---------------------------------- 71.7/626.3 kB 491.5 kB/s eta 0:00:02
       -------- ----------------------------- 143.4/626.3 kB 853.3 kB/s eta 0:00:01
       ------------ ------------------------- 204.8/626.3 kB 888.4 kB/s eta 0:00:01
       --------------- ---------------------- 256.0/626.3 kB 983.0 kB/s eta 0:00:01
       --------------- ---------------------- 256.0/626.3 kB 983.0 kB/s eta 0:00:01
       --------------- ---------------------- 256.0/626.3 kB 983.0 kB/s eta 0:00:01
       --------------------- ---------------- 348.2/626.3 kB 864.2 kB/s eta 0:00:01
       --------------------- ---------------- 348.2/626.3 kB 864.2 kB/s eta 0:00:01
       --------------------- ---------------- 348.2/626.3 kB 864.2 kB/s eta 0:00:01
       --------------------- ---------------- 348.2/626.3 kB 864.2 kB/s eta 0:00:01
       --------------------- ---------------- 348.2/626.3 kB 864.2 kB/s eta 0:00:01
       --------------------- ---------------- 348.2/626.3 kB 864.2 kB/s eta 0:00:01
       ----------------------- -------------- 389.1/626.3 kB 622.1 kB/s eta 0:00:01
       ------------------------- ------------ 419.8/626.3 kB 624.4 kB/s eta 0:00:01
       --------------------------- ---------- 450.6/626.3 kB 626.3 kB/s eta 0:00:01
       ----------------------------- -------- 481.3/626.3 kB 641.7 kB/s eta 0:00:01
       --------------------------------- ---- 553.0/626.3 kB 694.9 kB/s eta 0:00:01
       -------------------------------------- 626.3/626.3 kB 744.1 kB/s eta 0:00:00
    Installing collected packages: textblob
    Successfully installed textblob-0.18.0.post0
    Note: you may need to restart the kernel to use updated packages.
    


```python
from ntscraper import Nitter
import json
from textblob import TextBlob
```


```python
tweets = Nitter().get_tweets("CommBank",mode="user", number=100)
```

    Testing instances:  71%|█████████████████████████████████████████████                  | 55/77 [02:44<01:13,  3.36s/it]

    04-Jun-24 11:10:05 - Certificate did not match expected hostname: nitter.no-logs.com. Certificate: {'subject': ((('commonName', 'no-logs.com'),),), 'issuer': ((('countryName', 'US'),), (('organizationName', "Let's Encrypt"),), (('commonName', 'R3'),)), 'version': 3, 'serialNumber': '03D031100DF5685B02FBBE1577956863687F', 'notBefore': 'May 14 21:29:50 2024 GMT', 'notAfter': 'Aug 12 21:29:49 2024 GMT', 'subjectAltName': (('DNS', 'no-logs.com'),), 'OCSP': ('http://r3.o.lencr.org',), 'caIssuers': ('http://r3.i.lencr.org/',)}
    

    Testing instances:  92%|██████████████████████████████████████████████████████████     | 71/77 [09:45<00:43,  7.26s/it]

    04-Jun-24 11:17:06 - Certificate did not match expected hostname: nt.ggtyler.dev. Certificate: {'subject': ((('commonName', '4g.ggtyler.dev'),),), 'issuer': ((('countryName', 'US'),), (('organizationName', "Let's Encrypt"),), (('commonName', 'R3'),)), 'version': 3, 'serialNumber': '03A4459CE6DA31CFF555DB78FF3F35BFEA88', 'notBefore': 'May 14 10:55:44 2024 GMT', 'notAfter': 'Aug 12 10:55:43 2024 GMT', 'subjectAltName': (('DNS', '4g.ggtyler.dev'),), 'OCSP': ('http://r3.o.lencr.org',), 'caIssuers': ('http://r3.i.lencr.org/',)}
    

    Testing instances:  95%|███████████████████████████████████████████████████████████▋   | 73/77 [09:48<00:16,  4.19s/it]

    04-Jun-24 11:17:09 - Certificate did not match expected hostname: nitter.uni-sonia.com. Certificate: {'subject': ((('commonName', '*.xserver.jp'),),), 'issuer': ((('countryName', 'JP'),), (('organizationName', 'CloudSecure Corporation'),), (('commonName', 'CloudSecure RSA Domain Validation Secure Server CA 2'),)), 'version': 3, 'serialNumber': 'ACA67AD2030638EE2DCE8E845B8299A6', 'notBefore': 'Mar 11 00:00:00 2024 GMT', 'notAfter': 'Apr 11 23:59:59 2025 GMT', 'subjectAltName': (('DNS', '*.xserver.jp'), ('DNS', 'xserver.jp')), 'OCSP': ('http://ocsp.sectigo.com',), 'caIssuers': ('http://crt.sectigo.com/CloudSecureRSADomainValidationSecureServerCA2.crt',)}
    

    Testing instances:  99%|██████████████████████████████████████████████████████████████▏| 76/77 [10:00<00:04,  4.38s/it]

    04-Jun-24 11:17:22 - Certificate did not match expected hostname: nitter.tinfoil-hat.net. Certificate: {'subject': ((('commonName', 'jelly.tinfoil-hat.de'),),), 'issuer': ((('countryName', 'US'),), (('organizationName', "Let's Encrypt"),), (('commonName', 'R3'),)), 'version': 3, 'serialNumber': '044FDE3E7089FB997C3D8AFDE2412CE51554', 'notBefore': 'May 15 09:29:23 2024 GMT', 'notAfter': 'Aug 13 09:29:22 2024 GMT', 'subjectAltName': (('DNS', 'jelly.tinfoil-hat.de'),), 'OCSP': ('http://r3.o.lencr.org',), 'caIssuers': ('http://r3.i.lencr.org/',)}
    

    Testing instances: 100%|███████████████████████████████████████████████████████████████| 77/77 [10:03<00:00,  7.83s/it]

    04-Jun-24 11:17:22 - No instance specified, using random instance https://nitter.privacydev.net
    

    
    

    04-Jun-24 11:17:31 - Current stats for CommBank: 21 tweets, 0 threads...
    04-Jun-24 11:17:35 - Current stats for CommBank: 41 tweets, 0 threads...
    04-Jun-24 11:17:40 - Current stats for CommBank: 61 tweets, 0 threads...
    04-Jun-24 11:17:42 - Empty page on https://nitter.privacydev.net
    

### Step 1: Load and Explore the Data


```python
import json

# Load the JSON file
with open('CommBank.json', 'r') as file:
    data = json.load(file)

# Explore the data structure
data.keys()
```




    dict_keys(['tweets', 'threads'])



### Step 2: Extract Relevant Fields python


```python
import pandas as pd

# Extract tweet text, date, and user information
tweets = []
for tweet in data['tweets']:
    tweet_info = {
        'text': tweet['text'],
        'date': tweet['date'],
        'user': tweet['user']['name'],
        'username': tweet['user']['username'],
        'comments': tweet['stats']['comments'],
        'retweets': tweet['stats']['retweets'],
        'likes': tweet['stats']['likes'],
        'quotes':tweet['stats']['quotes'],
        'is-retweet':tweet['is-retweet'],
        'is-pinned':tweet['is-pinned']
    }
    tweets.append(tweet_info)

# Convert to DataFrame
df = pd.DataFrame(tweets)
df.to_csv("CommBank_tweet_data.csv")
```


```python
df
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>text</th>
      <th>date</th>
      <th>user</th>
      <th>username</th>
      <th>comments</th>
      <th>retweets</th>
      <th>likes</th>
      <th>quotes</th>
      <th>is-retweet</th>
      <th>is-pinned</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>When shopping online, do you look for discount...</td>
      <td>Dec 18, 2023 · 1:13 AM UTC</td>
      <td>CommBank</td>
      <td>@CommBank</td>
      <td>79</td>
      <td>1</td>
      <td>10</td>
      <td>0</td>
      <td>False</td>
      <td>True</td>
    </tr>
    <tr>
      <th>1</th>
      <td>These lucky girls will have the chance to see ...</td>
      <td>May 31, 2024 · 11:51 PM UTC</td>
      <td>CommBank</td>
      <td>@CommBank</td>
      <td>1</td>
      <td>0</td>
      <td>2</td>
      <td>0</td>
      <td>False</td>
      <td>False</td>
    </tr>
    <tr>
      <th>2</th>
      <td>Meet the girls from Pagewood Botany FC, one of...</td>
      <td>May 31, 2024 · 11:51 PM UTC</td>
      <td>CommBank</td>
      <td>@CommBank</td>
      <td>2</td>
      <td>1</td>
      <td>3</td>
      <td>0</td>
      <td>False</td>
      <td>False</td>
    </tr>
    <tr>
      <th>3</th>
      <td>These lucky girls will have the chance to see ...</td>
      <td>May 31, 2024 · 11:46 PM UTC</td>
      <td>CommBank</td>
      <td>@CommBank</td>
      <td>2</td>
      <td>0</td>
      <td>2</td>
      <td>0</td>
      <td>False</td>
      <td>False</td>
    </tr>
    <tr>
      <th>4</th>
      <td>We’ve read the Federal #Budget2024 so you don’...</td>
      <td>May 15, 2024 · 1:26 AM UTC</td>
      <td>CommBank</td>
      <td>@CommBank</td>
      <td>13</td>
      <td>0</td>
      <td>7</td>
      <td>2</td>
      <td>False</td>
      <td>False</td>
    </tr>
    <tr>
      <th>...</th>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
    </tr>
    <tr>
      <th>56</th>
      <td>TL;DR - Watch out for online shopping scams th...</td>
      <td>Dec 18, 2023 · 11:05 PM UTC</td>
      <td>CommBank</td>
      <td>@CommBank</td>
      <td>3</td>
      <td>3</td>
      <td>7</td>
      <td>1</td>
      <td>False</td>
      <td>False</td>
    </tr>
    <tr>
      <th>57</th>
      <td>For emergency help in storms, call the @QldFES...</td>
      <td>Dec 18, 2023 · 6:25 AM UTC</td>
      <td>CommBank</td>
      <td>@CommBank</td>
      <td>0</td>
      <td>0</td>
      <td>1</td>
      <td>0</td>
      <td>False</td>
      <td>False</td>
    </tr>
    <tr>
      <th>58</th>
      <td>We understand everyone will have different nee...</td>
      <td>Dec 18, 2023 · 6:25 AM UTC</td>
      <td>CommBank</td>
      <td>@CommBank</td>
      <td>1</td>
      <td>0</td>
      <td>1</td>
      <td>1</td>
      <td>False</td>
      <td>False</td>
    </tr>
    <tr>
      <th>59</th>
      <td>We have activated our Emergency Assistance to ...</td>
      <td>Dec 18, 2023 · 6:25 AM UTC</td>
      <td>CommBank</td>
      <td>@CommBank</td>
      <td>2</td>
      <td>0</td>
      <td>4</td>
      <td>0</td>
      <td>False</td>
      <td>False</td>
    </tr>
    <tr>
      <th>60</th>
      <td>The best part is, eligibility starts with hold...</td>
      <td>Dec 18, 2023 · 1:13 AM UTC</td>
      <td>CommBank</td>
      <td>@CommBank</td>
      <td>5</td>
      <td>0</td>
      <td>2</td>
      <td>0</td>
      <td>False</td>
      <td>False</td>
    </tr>
  </tbody>
</table>
<p>61 rows × 10 columns</p>
</div>



### Step 3: Clean the Data


```python
import re

def clean_tweet(text):
    text = re.sub(r'http\S+', '', text)  # Remove URLs
    text = re.sub(r'@\w+', '', text)     # Remove mentions
    text = re.sub(r'#\w+', '', text)     # Remove hashtags
    text = re.sub(r'\W+', ' ', text)     # Remove special characters
    text = text.lower()                  # Convert to lowercase
    return text

df['cleaned_text'] = df['text'].apply(clean_tweet)
df.to_csv("CommBank_tweet_data.csv")
```

### Step 4: Sentiment Analysis


```python
from vaderSentiment.vaderSentiment import SentimentIntensityAnalyzer

analyzer = SentimentIntensityAnalyzer()

def get_sentiment(text):
    sentiment = analyzer.polarity_scores(text)
    return sentiment

# Apply sentiment analysis
df['sentiment'] = df['cleaned_text'].apply(get_sentiment)

# Extract sentiment scores into separate columns
df['neg'] = df['sentiment'].apply(lambda x: x['neg'])
df['neu'] = df['sentiment'].apply(lambda x: x['neu'])
df['pos'] = df['sentiment'].apply(lambda x: x['pos'])
df['compound'] = df['sentiment'].apply(lambda x: x['compound'])

# Drop the intermediate sentiment column
df.drop(columns=['sentiment'], inplace=True)
```


```python
def get_textblob_sentiment(text):
    analysis = TextBlob(text)
    return analysis.sentiment.polarity, analysis.sentiment.subjectivity

df['textblob_polarity'], df['textblob_subjectivity'] = zip(*df['cleaned_text'].apply(get_textblob_sentiment))
```


```python
df
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>text</th>
      <th>date</th>
      <th>user</th>
      <th>username</th>
      <th>comments</th>
      <th>retweets</th>
      <th>likes</th>
      <th>quotes</th>
      <th>is-retweet</th>
      <th>is-pinned</th>
      <th>cleaned_text</th>
      <th>neg</th>
      <th>neu</th>
      <th>pos</th>
      <th>compound</th>
      <th>textblob_polarity</th>
      <th>textblob_subjectivity</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>When shopping online, do you look for discount...</td>
      <td>Dec 18, 2023 · 1:13 AM UTC</td>
      <td>CommBank</td>
      <td>@CommBank</td>
      <td>79</td>
      <td>1</td>
      <td>10</td>
      <td>0</td>
      <td>False</td>
      <td>True</td>
      <td>when shopping online do you look for discounts...</td>
      <td>0.000</td>
      <td>1.000</td>
      <td>0.000</td>
      <td>0.0000</td>
      <td>0.100000</td>
      <td>0.000000</td>
    </tr>
    <tr>
      <th>1</th>
      <td>These lucky girls will have the chance to see ...</td>
      <td>May 31, 2024 · 11:51 PM UTC</td>
      <td>CommBank</td>
      <td>@CommBank</td>
      <td>1</td>
      <td>0</td>
      <td>2</td>
      <td>0</td>
      <td>False</td>
      <td>False</td>
      <td>these lucky girls will have the chance to see ...</td>
      <td>0.000</td>
      <td>0.782</td>
      <td>0.218</td>
      <td>0.7964</td>
      <td>-0.016667</td>
      <td>0.383333</td>
    </tr>
    <tr>
      <th>2</th>
      <td>Meet the girls from Pagewood Botany FC, one of...</td>
      <td>May 31, 2024 · 11:51 PM UTC</td>
      <td>CommBank</td>
      <td>@CommBank</td>
      <td>2</td>
      <td>1</td>
      <td>3</td>
      <td>0</td>
      <td>False</td>
      <td>False</td>
      <td>meet the girls from pagewood botany fc one of ...</td>
      <td>0.000</td>
      <td>0.823</td>
      <td>0.177</td>
      <td>0.7096</td>
      <td>0.000000</td>
      <td>0.250000</td>
    </tr>
    <tr>
      <th>3</th>
      <td>These lucky girls will have the chance to see ...</td>
      <td>May 31, 2024 · 11:46 PM UTC</td>
      <td>CommBank</td>
      <td>@CommBank</td>
      <td>2</td>
      <td>0</td>
      <td>2</td>
      <td>0</td>
      <td>False</td>
      <td>False</td>
      <td>these lucky girls will have the chance to see ...</td>
      <td>0.000</td>
      <td>0.782</td>
      <td>0.218</td>
      <td>0.7964</td>
      <td>-0.016667</td>
      <td>0.383333</td>
    </tr>
    <tr>
      <th>4</th>
      <td>We’ve read the Federal #Budget2024 so you don’...</td>
      <td>May 15, 2024 · 1:26 AM UTC</td>
      <td>CommBank</td>
      <td>@CommBank</td>
      <td>13</td>
      <td>0</td>
      <td>7</td>
      <td>2</td>
      <td>False</td>
      <td>False</td>
      <td>we ve read the federal so you don t have to he...</td>
      <td>0.000</td>
      <td>1.000</td>
      <td>0.000</td>
      <td>0.0000</td>
      <td>0.000000</td>
      <td>0.000000</td>
    </tr>
    <tr>
      <th>...</th>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
    </tr>
    <tr>
      <th>56</th>
      <td>TL;DR - Watch out for online shopping scams th...</td>
      <td>Dec 18, 2023 · 11:05 PM UTC</td>
      <td>CommBank</td>
      <td>@CommBank</td>
      <td>3</td>
      <td>3</td>
      <td>7</td>
      <td>1</td>
      <td>False</td>
      <td>False</td>
      <td>tl dr watch out for online shopping scams this...</td>
      <td>0.297</td>
      <td>0.703</td>
      <td>0.000</td>
      <td>-0.5859</td>
      <td>0.000000</td>
      <td>0.000000</td>
    </tr>
    <tr>
      <th>57</th>
      <td>For emergency help in storms, call the @QldFES...</td>
      <td>Dec 18, 2023 · 6:25 AM UTC</td>
      <td>CommBank</td>
      <td>@CommBank</td>
      <td>0</td>
      <td>0</td>
      <td>1</td>
      <td>0</td>
      <td>False</td>
      <td>False</td>
      <td>for emergency help in storms call the on 132 5...</td>
      <td>0.315</td>
      <td>0.586</td>
      <td>0.099</td>
      <td>-0.7096</td>
      <td>0.000000</td>
      <td>0.000000</td>
    </tr>
    <tr>
      <th>58</th>
      <td>We understand everyone will have different nee...</td>
      <td>Dec 18, 2023 · 6:25 AM UTC</td>
      <td>CommBank</td>
      <td>@CommBank</td>
      <td>1</td>
      <td>0</td>
      <td>1</td>
      <td>1</td>
      <td>False</td>
      <td>False</td>
      <td>we understand everyone will have different nee...</td>
      <td>0.093</td>
      <td>0.771</td>
      <td>0.137</td>
      <td>0.4588</td>
      <td>0.250000</td>
      <td>0.550000</td>
    </tr>
    <tr>
      <th>59</th>
      <td>We have activated our Emergency Assistance to ...</td>
      <td>Dec 18, 2023 · 6:25 AM UTC</td>
      <td>CommBank</td>
      <td>@CommBank</td>
      <td>2</td>
      <td>0</td>
      <td>4</td>
      <td>0</td>
      <td>False</td>
      <td>False</td>
      <td>we have activated our emergency assistance to ...</td>
      <td>0.072</td>
      <td>0.854</td>
      <td>0.074</td>
      <td>0.0258</td>
      <td>0.500000</td>
      <td>0.500000</td>
    </tr>
    <tr>
      <th>60</th>
      <td>The best part is, eligibility starts with hold...</td>
      <td>Dec 18, 2023 · 1:13 AM UTC</td>
      <td>CommBank</td>
      <td>@CommBank</td>
      <td>5</td>
      <td>0</td>
      <td>2</td>
      <td>0</td>
      <td>False</td>
      <td>False</td>
      <td>the best part is eligibility starts with holdi...</td>
      <td>0.000</td>
      <td>0.837</td>
      <td>0.163</td>
      <td>0.7783</td>
      <td>0.387500</td>
      <td>0.450000</td>
    </tr>
  </tbody>
</table>
<p>61 rows × 17 columns</p>
</div>




```python
df.info()
```

    <class 'pandas.core.frame.DataFrame'>
    RangeIndex: 61 entries, 0 to 60
    Data columns (total 17 columns):
     #   Column                 Non-Null Count  Dtype  
    ---  ------                 --------------  -----  
     0   text                   61 non-null     object 
     1   date                   61 non-null     object 
     2   user                   61 non-null     object 
     3   username               61 non-null     object 
     4   comments               61 non-null     int64  
     5   retweets               61 non-null     int64  
     6   likes                  61 non-null     int64  
     7   quotes                 61 non-null     int64  
     8   is-retweet             61 non-null     bool   
     9   is-pinned              61 non-null     bool   
     10  cleaned_text           61 non-null     object 
     11  neg                    61 non-null     float64
     12  neu                    61 non-null     float64
     13  pos                    61 non-null     float64
     14  compound               61 non-null     float64
     15  textblob_polarity      61 non-null     float64
     16  textblob_subjectivity  61 non-null     float64
    dtypes: bool(2), float64(6), int64(4), object(5)
    memory usage: 7.4+ KB
    

## Step-by-Step Guide After Structuring Twitter Data
### 1. Exploratory Data Analysis (EDA)


```python
import matplotlib.pyplot as plt
import seaborn as sns

# Summary statistics
print(df.describe())

# Distribution of sentiments
df[['neg', 'neu', 'pos']].hist(bins=20, figsize=(10, 5))
plt.show()

# Distribution of compound scores
sns.histplot(df['compound'], bins=20, kde=True)
plt.show()
```

            comments   retweets      likes     quotes        neg        neu  \
    count  61.000000  61.000000  61.000000  61.000000  61.000000  61.000000   
    mean    9.868852   1.540984   9.360656   0.704918   0.070246   0.804623   
    std    15.800291   3.074485  13.351695   1.801335   0.112762   0.145909   
    min     0.000000   0.000000   0.000000   0.000000   0.000000   0.340000   
    25%     2.000000   0.000000   2.000000   0.000000   0.000000   0.739000   
    50%     5.000000   0.000000   4.000000   0.000000   0.000000   0.801000   
    75%    10.000000   2.000000  11.000000   1.000000   0.101000   0.899000   
    max    79.000000  18.000000  57.000000  12.000000   0.425000   1.000000   
    
                 pos   compound  textblob_polarity  textblob_subjectivity  
    count  61.000000  61.000000          61.000000              61.000000  
    mean    0.125115   0.214969           0.136724               0.331942  
    std     0.119566   0.504126           0.215892               0.253867  
    min     0.000000  -0.783000          -0.500000               0.000000  
    25%     0.000000   0.000000           0.000000               0.000000  
    50%     0.119000   0.226300           0.068182               0.383333  
    75%     0.199000   0.700300           0.285714               0.500000  
    max     0.643000   0.872000           0.500000               0.900000  
    


    
![png](./Visualizations/Distribution%20of%20sentiments.png)
    



    
![png](./Visualizations/Distribution%20of%20compound%20scores.png)
    


### 2. Data Visualization


```python
import pandas as pd
from datetime import datetime
import matplotlib.pyplot as plt
import seaborn as sns

# Sample data
date_strings = df['date']

# Convert to pandas Series
date_series = pd.Series(date_strings)

# Custom date parser
def custom_date_parser(date_str):
    return datetime.strptime(date_str, '%b %d, %Y · %I:%M %p %Z')

# Parse dates
parsed_dates = date_series.apply(custom_date_parser)

# Create DataFrame
df['date'] = pd.DataFrame(parsed_dates, columns=['date'])

# Assuming you have sentiment scores in the DataFrame
#df['sentiment'] = [0.5] * len(df)  # Replace with your actual sentiment data
```


```python
# Bar plot of average sentiment scores
avg_sentiments = df[['neg', 'neu', 'pos']].mean()
avg_sentiments.plot(kind='bar', figsize=(10, 5))
plt.ylabel('Average Sentiment Score')
plt.title('Average Sentiment Scores')
plt.show()

# Time series analysis of sentiments over time
# Plotting sentiment over time
plt.figure(figsize=(15, 10))
plt.subplot(2,2,2)
plt.plot(df['date'],df['neg'],"g--o")
plt.title("negetive sentiment over time")
plt.xlabel('Date')
plt.ylabel('Sentiment Score')

plt.subplot(2,2,3)
plt.plot(df['date'],df['neu'],"b--o")
plt.title("neural sentiment over time")
plt.xlabel('Date')
plt.ylabel('Sentiment Score')

plt.subplot(2,2,1)
plt.plot(df['date'],df['pos'],"r--o")
plt.title("positive sentiment over time")
plt.xlabel('Date')
plt.ylabel('Sentiment Score')

#sns.pairplot(data=df,hue="date")
#plt.title('Sentiment Over Time')

plt.show()
```


    
![png](./Visualizations/Bar%20plot%20of%20average%20sentiment%20scores.png)
    



    
![png](./Visualizations/Time%20series%20analysis%20of%20sentiments%20over%20time.png)
    


### Trend Analysis
####  Visualize Sentiment Over Time


```python
import seaborn as sns
plt.figure(figsize=(30, 10))

# Plot VADER Compound Sentiment over time
sns.lineplot(x='date', y='compound', data=df, label='VADER Compound Sentiment')
# Plot TextBlob Polarity over time
sns.lineplot(x='date', y='textblob_polarity', data=df, label='TextBlob Polarity')

plt.title('Sentiment Analysis Over Time')
plt.xlabel('Date')
plt.ylabel('Sentiment Score')
plt.legend()
plt.show()

```


    
![png](./Visualizations/Trend%20Analysis%20between%20VADER%20Compound%20Sentiment%20%26%20TextBlob%20Polarity%20over%20time.png)
    


#### Word Clouds for Trending Topics


```python
pip install wordcloud
```

    Collecting wordcloud
      Obtaining dependency information for wordcloud from https://files.pythonhosted.org/packages/f5/b0/247159f61c5d5d6647171bef84430b7efad4db504f0229674024f3a4f7f2/wordcloud-1.9.3-cp311-cp311-win_amd64.whl.metadata
      Downloading wordcloud-1.9.3-cp311-cp311-win_amd64.whl.metadata (3.5 kB)
    Requirement already satisfied: numpy>=1.6.1 in c:\users\sompurapooja32\anaconda3\lib\site-packages (from wordcloud) (1.24.3)
    Requirement already satisfied: pillow in c:\users\sompurapooja32\anaconda3\lib\site-packages (from wordcloud) (9.4.0)
    Requirement already satisfied: matplotlib in c:\users\sompurapooja32\anaconda3\lib\site-packages (from wordcloud) (3.7.2)
    Requirement already satisfied: contourpy>=1.0.1 in c:\users\sompurapooja32\anaconda3\lib\site-packages (from matplotlib->wordcloud) (1.0.5)
    Requirement already satisfied: cycler>=0.10 in c:\users\sompurapooja32\anaconda3\lib\site-packages (from matplotlib->wordcloud) (0.11.0)
    Requirement already satisfied: fonttools>=4.22.0 in c:\users\sompurapooja32\anaconda3\lib\site-packages (from matplotlib->wordcloud) (4.25.0)
    Requirement already satisfied: kiwisolver>=1.0.1 in c:\users\sompurapooja32\anaconda3\lib\site-packages (from matplotlib->wordcloud) (1.4.4)
    Requirement already satisfied: packaging>=20.0 in c:\users\sompurapooja32\anaconda3\lib\site-packages (from matplotlib->wordcloud) (23.1)
    Requirement already satisfied: pyparsing<3.1,>=2.3.1 in c:\users\sompurapooja32\anaconda3\lib\site-packages (from matplotlib->wordcloud) (3.0.9)
    Requirement already satisfied: python-dateutil>=2.7 in c:\users\sompurapooja32\anaconda3\lib\site-packages (from matplotlib->wordcloud) (2.8.2)
    Requirement already satisfied: six>=1.5 in c:\users\sompurapooja32\anaconda3\lib\site-packages (from python-dateutil>=2.7->matplotlib->wordcloud) (1.16.0)
    Downloading wordcloud-1.9.3-cp311-cp311-win_amd64.whl (300 kB)
       ---------------------------------------- 0.0/300.2 kB ? eta -:--:--
       - -------------------------------------- 10.2/300.2 kB ? eta -:--:--
       - -------------------------------------- 10.2/300.2 kB ? eta -:--:--
       --- ----------------------------------- 30.7/300.2 kB 217.9 kB/s eta 0:00:02
       ----- --------------------------------- 41.0/300.2 kB 245.8 kB/s eta 0:00:02
       ------- ------------------------------- 61.4/300.2 kB 297.7 kB/s eta 0:00:01
       ----------- --------------------------- 92.2/300.2 kB 403.5 kB/s eta 0:00:01
       --------------- ---------------------- 122.9/300.2 kB 450.6 kB/s eta 0:00:01
       ------------------- ------------------ 153.6/300.2 kB 510.2 kB/s eta 0:00:01
       ------------------------- ------------ 204.8/300.2 kB 541.9 kB/s eta 0:00:01
       ---------------------------- --------- 225.3/300.2 kB 529.7 kB/s eta 0:00:01
       -------------------------------- ----- 256.0/300.2 kB 542.5 kB/s eta 0:00:01
       -------------------------------- ----- 256.0/300.2 kB 542.5 kB/s eta 0:00:01
       -------------------------------- ----- 256.0/300.2 kB 542.5 kB/s eta 0:00:01
       -------------------------------- ----- 256.0/300.2 kB 542.5 kB/s eta 0:00:01
       -------------------------------- ----- 256.0/300.2 kB 542.5 kB/s eta 0:00:01
       -------------------------------- ----- 256.0/300.2 kB 542.5 kB/s eta 0:00:01
       -------------------------------------- 300.2/300.2 kB 395.0 kB/s eta 0:00:00
    Installing collected packages: wordcloud
    Successfully installed wordcloud-1.9.3
    Note: you may need to restart the kernel to use updated packages.
    


```python
from wordcloud import WordCloud

# Generate a word cloud
all_words = ' '.join([text for text in df['cleaned_text']])
wordcloud = WordCloud(width=800, height=400, random_state=21, max_font_size=110).generate(all_words)

plt.figure(figsize=(10, 7))
plt.imshow(wordcloud, interpolation="bilinear")
plt.axis('off')
plt.show()
```


    
![png](./Visualizations/Word%20Clouds%20for%20Trending%20Topics.png)
    


### Extracting Insights
#### Analyzing Sentiment Distribution


```python
plt.figure(figsize=(12, 6))

# Distribution of VADER Compound Sentiment
sns.histplot(df['compound'], kde=True, bins=30)
plt.title('Distribution of VADER Compound Sentiment')
plt.xlabel('Sentiment Score')
plt.ylabel('Frequency')
plt.show()
```


    
![png](./Visualizations/Distribution%20of%20VADER%20Compound%20Sentiment.png)
    


#### Analyzing Sentiment by Tweet Categories


```python
df
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>text</th>
      <th>date</th>
      <th>user</th>
      <th>username</th>
      <th>comments</th>
      <th>retweets</th>
      <th>likes</th>
      <th>quotes</th>
      <th>is-retweet</th>
      <th>is-pinned</th>
      <th>cleaned_text</th>
      <th>neg</th>
      <th>neu</th>
      <th>pos</th>
      <th>compound</th>
      <th>textblob_polarity</th>
      <th>textblob_subjectivity</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>When shopping online, do you look for discount...</td>
      <td>2023-12-18 01:13:00</td>
      <td>CommBank</td>
      <td>@CommBank</td>
      <td>79</td>
      <td>1</td>
      <td>10</td>
      <td>0</td>
      <td>False</td>
      <td>True</td>
      <td>when shopping online do you look for discounts...</td>
      <td>0.000</td>
      <td>1.000</td>
      <td>0.000</td>
      <td>0.0000</td>
      <td>0.100000</td>
      <td>0.000000</td>
    </tr>
    <tr>
      <th>1</th>
      <td>These lucky girls will have the chance to see ...</td>
      <td>2024-05-31 23:51:00</td>
      <td>CommBank</td>
      <td>@CommBank</td>
      <td>1</td>
      <td>0</td>
      <td>2</td>
      <td>0</td>
      <td>False</td>
      <td>False</td>
      <td>these lucky girls will have the chance to see ...</td>
      <td>0.000</td>
      <td>0.782</td>
      <td>0.218</td>
      <td>0.7964</td>
      <td>-0.016667</td>
      <td>0.383333</td>
    </tr>
    <tr>
      <th>2</th>
      <td>Meet the girls from Pagewood Botany FC, one of...</td>
      <td>2024-05-31 23:51:00</td>
      <td>CommBank</td>
      <td>@CommBank</td>
      <td>2</td>
      <td>1</td>
      <td>3</td>
      <td>0</td>
      <td>False</td>
      <td>False</td>
      <td>meet the girls from pagewood botany fc one of ...</td>
      <td>0.000</td>
      <td>0.823</td>
      <td>0.177</td>
      <td>0.7096</td>
      <td>0.000000</td>
      <td>0.250000</td>
    </tr>
    <tr>
      <th>3</th>
      <td>These lucky girls will have the chance to see ...</td>
      <td>2024-05-31 23:46:00</td>
      <td>CommBank</td>
      <td>@CommBank</td>
      <td>2</td>
      <td>0</td>
      <td>2</td>
      <td>0</td>
      <td>False</td>
      <td>False</td>
      <td>these lucky girls will have the chance to see ...</td>
      <td>0.000</td>
      <td>0.782</td>
      <td>0.218</td>
      <td>0.7964</td>
      <td>-0.016667</td>
      <td>0.383333</td>
    </tr>
    <tr>
      <th>4</th>
      <td>We’ve read the Federal #Budget2024 so you don’...</td>
      <td>2024-05-15 01:26:00</td>
      <td>CommBank</td>
      <td>@CommBank</td>
      <td>13</td>
      <td>0</td>
      <td>7</td>
      <td>2</td>
      <td>False</td>
      <td>False</td>
      <td>we ve read the federal so you don t have to he...</td>
      <td>0.000</td>
      <td>1.000</td>
      <td>0.000</td>
      <td>0.0000</td>
      <td>0.000000</td>
      <td>0.000000</td>
    </tr>
    <tr>
      <th>...</th>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
    </tr>
    <tr>
      <th>56</th>
      <td>TL;DR - Watch out for online shopping scams th...</td>
      <td>2023-12-18 23:05:00</td>
      <td>CommBank</td>
      <td>@CommBank</td>
      <td>3</td>
      <td>3</td>
      <td>7</td>
      <td>1</td>
      <td>False</td>
      <td>False</td>
      <td>tl dr watch out for online shopping scams this...</td>
      <td>0.297</td>
      <td>0.703</td>
      <td>0.000</td>
      <td>-0.5859</td>
      <td>0.000000</td>
      <td>0.000000</td>
    </tr>
    <tr>
      <th>57</th>
      <td>For emergency help in storms, call the @QldFES...</td>
      <td>2023-12-18 06:25:00</td>
      <td>CommBank</td>
      <td>@CommBank</td>
      <td>0</td>
      <td>0</td>
      <td>1</td>
      <td>0</td>
      <td>False</td>
      <td>False</td>
      <td>for emergency help in storms call the on 132 5...</td>
      <td>0.315</td>
      <td>0.586</td>
      <td>0.099</td>
      <td>-0.7096</td>
      <td>0.000000</td>
      <td>0.000000</td>
    </tr>
    <tr>
      <th>58</th>
      <td>We understand everyone will have different nee...</td>
      <td>2023-12-18 06:25:00</td>
      <td>CommBank</td>
      <td>@CommBank</td>
      <td>1</td>
      <td>0</td>
      <td>1</td>
      <td>1</td>
      <td>False</td>
      <td>False</td>
      <td>we understand everyone will have different nee...</td>
      <td>0.093</td>
      <td>0.771</td>
      <td>0.137</td>
      <td>0.4588</td>
      <td>0.250000</td>
      <td>0.550000</td>
    </tr>
    <tr>
      <th>59</th>
      <td>We have activated our Emergency Assistance to ...</td>
      <td>2023-12-18 06:25:00</td>
      <td>CommBank</td>
      <td>@CommBank</td>
      <td>2</td>
      <td>0</td>
      <td>4</td>
      <td>0</td>
      <td>False</td>
      <td>False</td>
      <td>we have activated our emergency assistance to ...</td>
      <td>0.072</td>
      <td>0.854</td>
      <td>0.074</td>
      <td>0.0258</td>
      <td>0.500000</td>
      <td>0.500000</td>
    </tr>
    <tr>
      <th>60</th>
      <td>The best part is, eligibility starts with hold...</td>
      <td>2023-12-18 01:13:00</td>
      <td>CommBank</td>
      <td>@CommBank</td>
      <td>5</td>
      <td>0</td>
      <td>2</td>
      <td>0</td>
      <td>False</td>
      <td>False</td>
      <td>the best part is eligibility starts with holdi...</td>
      <td>0.000</td>
      <td>0.837</td>
      <td>0.163</td>
      <td>0.7783</td>
      <td>0.387500</td>
      <td>0.450000</td>
    </tr>
  </tbody>
</table>
<p>61 rows × 17 columns</p>
</div>




```python
plt.figure(figsize=(20, 6))

# Example: Assuming you have a column 'category'
sns.boxplot(x='retweets', y='compound', data=df)
plt.title('Sentiment by Category')
plt.xlabel('Category')
plt.ylabel('VADER Compound Sentiment')
plt.xticks(rotation=45)
plt.show()

```


    
![png](./Visualizations/Analyzing%20Sentiment%20by%20Tweet%20Categories.png)
    


### 3. Model Selection and training


```python
from sklearn.model_selection import train_test_split
from sklearn.feature_extraction.text import CountVectorizer,TfidfVectorizer
from sklearn.naive_bayes import MultinomialNB
from sklearn.metrics import classification_report

# Prepare the data
X = df['cleaned_text']
y = df['compound'].apply(lambda x: 'positive' if x >= 0 else 'negative')

# Split the data
X_train, X_test, y_train, y_test = train_test_split(X, y, test_size=0.2, random_state=42)

# Vectorize the text data
vectorizer = CountVectorizer()
X_train_vec = vectorizer.fit_transform(X_train)
X_test_vec = vectorizer.transform(X_test)

# Train a Naive Bayes classifier
nb = MultinomialNB()
nb.fit(X_train_vec, y_train)

# Predict and evaluate
y_pred = nb.predict(X_test_vec)
print(classification_report(y_test, y_pred))
print('Confusion Matrix:')
print(confusion_matrix(y_test, y_pred))
```

                  precision    recall  f1-score   support
    
        negative       1.00      1.00      1.00         2
        positive       1.00      1.00      1.00        11
    
        accuracy                           1.00        13
       macro avg       1.00      1.00      1.00        13
    weighted avg       1.00      1.00      1.00        13
    
    Confusion Matrix:
    [[ 2  0]
     [ 0 11]]
    

### 4. Hyperparameter Tuning


```python
from sklearn.model_selection import GridSearchCV

# Define the parameter grid
param_grid = {
    'C': [0.1, 1, 10, 100]
}

# Grid search for Logistic Regression
grid_search = GridSearchCV(LogisticRegression(), param_grid, cv=5)
grid_search.fit(X_train_vec, y_train)

# Best parameters
print(f'Best Parameters: {grid_search.best_params_}')
```

    Best Parameters: {'C': 1}
    

### 5. Prediction and Analysis


```python
# Predict sentiments for new tweets
new_tweets = ['Say hello to the first recipients of the Growing Football Fund 👋 In partnership with @FootballAUS, we recently announced the 121 amazing clubs and associations who would receive funding to help drive participation and remove financial barriers to help more girls into the game', 'Not really service with a smile. @Commbank, pretty hopeless. Telling me things I cannot check because I cant access settings.']
new_tweets_cleaned = [clean_tweet(tweet) for tweet in new_tweets]
new_tweets_vec = vectorizer.transform(new_tweets_cleaned)
new_sentiments = nb.predict(new_tweets_vec)

print('New Sentiments:', new_sentiments)
```

    New Sentiments: ['positive' 'positive']
    

### Trend Analysis
#### Analyze Tweet Volume Over Time


```python
import matplotlib.pyplot as plt

# Resample data to daily frequency and count the number of tweets per day
df['date'] = pd.to_datetime(df['date'])
df.set_index('date', inplace=True)
daily_tweet_count = df['text'].resample('D').count()

plt.figure(figsize=(12, 6))
plt.plot(daily_tweet_count, marker='o')
plt.title('Number of Tweets Over Time')
plt.xlabel('Date')
plt.ylabel('Number of Tweets')
plt.grid(True)
plt.show()
```


    
![png](./Visualizations/Analyze%20Tweet%20Volume%20Over%20Time.png)
    


### Sentiment Trend Over Time


```python
# Resample data to daily frequency and calculate the mean sentiment score per day
daily_sentiment = df['compound'].resample('D').mean()

plt.figure(figsize=(12, 6))
plt.plot(daily_sentiment, marker='o', color='green')
plt.title('Daily Average Sentiment Over Time')
plt.xlabel('Date')
plt.ylabel('Average Sentiment Score')
plt.grid(True)
plt.show()
```


    
![png](./Visualizations/Sentiment%20Trend%20Over%20Time.png)
    


### Analyze Specific Keywords or Hashtags


```python
# Example: Analyzing the trend of the keyword 'banking'
keyword = df['text'].
df['contains_keyword'] = df['cleaned_text'].apply(lambda x: keyword in x)

# Resample data to daily frequency and count occurrences of the keyword
daily_keyword_count = df['contains_keyword'].resample('D').sum()

plt.figure(figsize=(12, 6))
plt.plot(daily_keyword_count, marker='o', color='red')
plt.title(f'Occurrences of Keyword "{keyword}" Over Time')
plt.xlabel('Date')
plt.ylabel(f'Number of Tweets Containing "{keyword}"')
plt.grid(True)
plt.show()

```


    
![png](./Visualizations/Analyze%20Specific%20Keywords%20or%20Hashtags.png)
    

