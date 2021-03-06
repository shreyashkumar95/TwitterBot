# TwitterBot

A simple program that replies to tweets. Response is generated using the CleverBot API.

# Usage

TwitterBot requires one positional argument to run, your twitter handle. Make sure to include the '@'
symbol.

Example: `python3 twitter_bot.py @yourhandle` or `./twitter_bot.py @yourhandle`

### Program Arguments

    usage: Twitter Bot [-h] [-r] [-q] [-l {0,1,2}] twitter_handle
    
    positional arguments:
      twitter_handle        your twitter @handle
    
    optional arguments:
      -h, --help                    show this help message and exit
      -r, --reply_to_thread         toggles reply to thread where mentioned
      -q, --quiet                   disables console output of non-errors
      -l {0,1,2}, --log {0,1,2}     change logging level


    Logging Levels
    - 0 : logging is disabled (default)
    - 1 : errors and critical failures are logged
    - 2 : in addition, tweets (incoming and outgoing) are logged


***Note**: if the account tweeting you is private, TwitterBot will not reply.*

# Installation

Generate API keys for [Twitter](https://apps.twitter.com) and [CleverBot](https://www.cleverbot.com/api/)

Find the credentials.py file and paste your credentials into the empty fields:
    
    class Twitter:
        CONSUMER_KEY = ''
        CONSUMER_SECRET = ''
        ACCESS_TOKEN_KEY = ''
        ACCESS_TOKEN_SECRET = ''
    
    
    class CleverBot:
        API_KEY = ''

Install Dependencies: `pip3 install python-twitter CleverWrap`
