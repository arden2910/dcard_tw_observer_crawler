# Observer Crawler

This is a Python web crawler for the 暗卡 (Dark Card) website, specifically designed to scrape data from the website's beauty section. 
The crawler uses the Jupyter Notebook format and outputs the crawled data in JSON format.



### Website Information

Name: 暗卡

暗卡Last Updated: 2011-12-16

URL: https://tw.observer/

### Getting Started

Clone this repository to your local machine.

Open the observer.ipynb file in Jupyter Notebook.

Make sure to have Python 3.x and the necessary libraries installed (e.g., pymongo).

Adjust the db_config settings, query, and date range as needed.

Run the notebook and wait for the data to be crawled.

Example of Crawled Data

The output of the crawled data will look like this:

```json
{
'id': 232054152,
'title': 'romand 唇釉',
'content': '...',
'excerpt': '...',
'createdAt': '2019-09-10T15:38:36.888000Z',
'updatedAt': '2019-09-10T15:38:36.888000',
'commentCount': 1,
'likeCount': 4,
'forumName': '美妝',
'forumAlias': 'makeup',
'school': '仁德醫護管理專科學校',
'gender': 'F',
'hidden': False,
'media': [{'url': 'https://i.imgur.com/9XqGxFc.jpg'},
{'url': 'https://i.imgur.com/I5znzV8.jpg'}],
'score': '2019-09-10T22:52:05.879000Z',
'order': '2019-09-10T15:38:36.888000Z',
'comments': [{'_id': '5d77c733f380bc4c9724e3d9',
'cid': 'e0e27209-e7b4-4bbc-a7e4-84f654670078',
'anonymous': True,
'postId': 232054152,
'createdAt': '2019-09-10T15:48:59.323Z',
'updatedAt': '2019-09-10T15:48:59.323Z',
'floor': 1,
'content': '...',
'likeCount': 0,
'withNickname': False,
'hiddenByAuthor': False,
'meta': {},
'gender': 'F',
'school': '實踐大學',
'host': False,
'reportReason': '',
'mediaMeta': [],
'hidden': False,
'inReview': False,
'reportReasonText': '',
'postAvatar': ''}]
}
```

Perform the crawl, updating the database with the crawled data.

### Configuration

db_config: MongoDB database configuration settings (host, username, password).

query: The query to crawl (e.g., "美妝" for beauty).

index_date: The range of dates to crawl (e.g., from '2019-09-12' to '2011-12-16').


Output

The crawled data will be saved in JSON format in the specified save_to directory. The data will also be updated in the specified MongoDB database.


Note

Please respect the website's terms of service and robots.txt file when crawling. Adjust the wait time between requests to avoid overloading the server.



Happy crawling!