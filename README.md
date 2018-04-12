# TweetBotDockerImage
A ubuntu based docker image for running tweet bot using python api


### Usage
<pre><code>
usage: run_tweet_dm_bot.py -h
                           -d DB_NAME 
                           -f QUICK_REPLY_DATA 
                           -m MESSAGE_DATA
                           -i BOT_ID 
                           -t TOKEN_FILE

optional arguments:
  -h, --help                                   Show this help message and exit
  -d ,--db_name DB_NAME                        SQLite db name
  -f ,--quick_reply_data QUICK_REPLY_DATA      Quick reply data json file
  -m ,--message_data MESSAGE_DATA              Message data json file
  -i ,--bot_id BOT_ID                          Bot twitter id
  -t ,--token_file TOKEN_FILE                  Twitter api token file
</code></pre>

### Example of quick reply data
Twitter has a specific structure for the [quick replies using direct messaging](https://developer.twitter.com/en/docs/direct-messages/quick-replies/api-reference/options). The data for the "quick_reply" post data senction can be provided using a json file.

#### An example json structure for quick reply data
<pre><code>
{
          "type": "options",
          "options": [
            {
              "label": "Red Bird",
              "description": "A description about the red bird.",
              "metadata": "external_id_1"
            },
            {
              "label": "Blue Bird",
              "description": "A description about the blue bird.",
              "metadata": "external_id_2"
            },
            {
              "label": "Black Bird",
              "description": "A description about the black bird.",
              "metadata": "external_id_3"
            },
            {
              "label": "White Bird",
              "description": "A description about the white bird.",
              "metadata": "external_id_4"
            }
          ]
}
</code></pre>
