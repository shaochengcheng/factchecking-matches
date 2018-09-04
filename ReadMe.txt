This dataset is for the paper titled “Tracking and Characterizing the
Competition of Fact Checking and Misinformation: Case Studies” by Chengcheng shao et al.

Please note that we cannot provide full tweet objects due to the Twitter
policies. Sometimes the tweets could be deleted and the accounts could be
suspended. Thus you may not re-fetch some tweets in the file we provided.
To be compliance with Twitter policies, as well as the replication
of the analysis, we tried our best to provide the neccessary fields, e.g., `id` of
the tweet, `id` of the user, and even for the json fields path like
`{retweeted_status, id}` (named as `retweeted_status_id` in the file).


Files and descriptions are:

1. pairs-M0-manual-20.csv
Description: 20 pairs of Snopes and fake news matched by hand
Fields:
    snopes: URL of fact-checking articles from snopes.com
    fake_news: URL of claim articles

2. pairs-M1-112.csv
Description: 121 pairs of Snopes and fake news matched by Links extraction method (M1)
Fields: see 1.

3. pairs-M2-quote-35.csv
Description: 35 pairs of Snopes and fake news matched by Social Fact-checking method (M2)
Fields: see 1.

4. pairs-M2-reply-202.csv
Description: 202 pairs of Snopes and fake news matched by Social Fact-checking method (M2)
Fields: see 1.

5. pairs-cleaning-73.csv
Description: 73 pairs of Snopes and fake news after merge and cleaning
Fields:
    snopes: URL of fact-checking articles from snopes.com
    fake_news: URL of claim articles
    s_pd: publication date of the snopes article
    s_ftw: first tweet date of the snopes article
    f_pd: publication date of the claim article
    f_ftw: first tweet date of the claim article
    f_n: number of claim tweets before debunking
    id: id

6 tweets-snopes.csv
Description: tweets that share snopes articles
Fields:
    tweet_created_at: created_at of the tweet
    tweet_id: id of the tweet
    tweet_user_id: user of the tweet
    retweeted_status_id: if this tweet is a retweet, this field will be populated, see `retweeted_status` from the Twitter documentation
    quoted_status_id: if this tweet is a quotes, this field will be populated, see `quoted_status_id` from the Twitter documentation
    in_reply_to_status_id: if this tweet is a reply, this field will be populated, see `in_reply_to_status_id` from the Twitter documentation.
    snopes: the tweeted link of the snopes article

7 tweets-fakenews.csv
Description: tweets that share fake news articles
Fields: see 6.

8. bot_score.json
Description: bot score for top 10% of the two groups

9. case_I.csv
Description: Data for case I.
Fields: see 6.

10. case_III.csv
Description: Data for case III.
Fields: see 6.




