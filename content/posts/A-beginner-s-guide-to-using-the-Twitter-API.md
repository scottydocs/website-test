---
title: A beginner’s guide to using the Twitter API
date: '2019-02-25T07:01:01.055Z'
excerpt: >-
  You can use the Twitter API to automatically send Tweets and media from your
  own account and to other Twitter users. That might sound…
thumb_img_path: >-
  images/A-beginner-s-guide-to-using-the-Twitter-API/1*wR479xgnnRycqZDiiGS7Ag.jpeg
layout: post
---
![](/images/A-beginner-s-guide-to-using-the-Twitter-API/1*wR479xgnnRycqZDiiGS7Ag.jpeg)

You can use the Twitter API to update your status or send Tweets and media to other users without actually logging into Twitter. You can also pull a list of the latest Tweets about a specific hashtag or from other users in your geographic location.

That might sound pretty complicated but you genuinely don’t need to be a developer to play around with the API and try some of these things out for yourself (**source**: I’m not a developer!).

You’ll need to familiarise yourself with opening the terminal and there are some tools to install beforehand but sending API calls is surprisingly easy once you get the hang of it.

### 🤔 What is the Twitter API?

An API, not to be confused with an IPA (Indian Pale Ale), is short for [Application Programming Interface](https://en.wikipedia.org/wiki/Application_programming_interface) — which is basically a list of methods in which two software applications can communicate with one another. The key methods are:

*   **GET**: Method to **retrieve** some data.
*   **POST**: Method to **create** some data.
*   **PUT**: Method to **update** some data.
*   **DELETE**: Method to **remove** some data.

One of the most popular analogies that people use to define an API is to think of it like a restaurant menu. It provides a list of items that can be ordered from the kitchen (one piece of software) by a customer (another piece of software).

The Twitter API allows you to access data and send data such as messages and media without having to open the Twitter application. Instead you send them using a command line tool like [cURL](https://en.wikipedia.org/wiki/CURL) or [Twurl](https://github.com/twitter/twurl), a tool that grants specified users with access to the Twitter API.

### 💻 How to open a terminal

Before you begin installing things, you should familiarise yourself with how to open a terminal. This is the command line interface (CLI) you use to send Twitter API calls:

![](/images/A-beginner-s-guide-to-using-the-Twitter-API/1*nnyokWJxIiWM3Jerr2Vhtw.png)

If you’re using a Mac, you can open the terminal by going to **Finder** > **Applications** > **Utilities** > **Terminal**. Or you can press **CMD** + **Space** to open Spotlight and search for ‘terminal’.

If you’re using a Windows 10 machine, select **Start** and search for ‘cmd’ to open the **Command Prompt**. For Windows 7 and older, select **Start** \> **All Programs** > **Accessories** \> **Command Prompt**.

### 🎬 Before you begin

Before you get started you must meet the following requirements:

*   Create a Twitter developer account. You can do this [here](http://href=%22https://developer.twitter.com/en/apply/user%22).
*   Open the Apps management page [here](https://developer.twitter.com/en/apps) and create an app. You only need to give it a name, enter any website URL and a 100-word description.
*   Install Ruby. You need this to run Twurl. See installation options [here](https://www.ruby-lang.org/en/documentation/installation/).
*   Install Twurl. See Twitter installation docs [here](https://developer.twitter.com/en/docs/tutorials/using-twurl.html).

Optionally you can install JQ, a command-line [JSON](https://en.wikipedia.org/wiki/JSON) processor. This makes the JSON responses returned by your API calls a lot easier to read.

    **NOTE**: Do not use JQ if you intend to use the output (e.g. a media ID) in a subsequent call. Integers longer than 53-bits break in JavaScript (mentioned in the JQ FAQ [here](https://github.com/stedolan/jq/wiki/FAQ#numbers)) so the numeric ID displayed will be incorrect. Thanks for the warning [Andy Piper](https://medium.com/u/da72a673691c)!

You can use this tool by typing `| jq` at the end of each request. See installation options [here](https://stedolan.github.io/jq/download/).

### 🔑 Get your API and secret keys

To send API calls to Twitter, you need a set of access keys that are unique to your developer account. To retrieve your keys:

1.  Login to your Twitter developer account.
2.  Go to your [Apps management screen](https://developer.twitter.com/en/apps) and click **Details** for your app.
3.  Click the **Keys and tokens** tab and generate a new API secret key.
4.  Copy or take note of the consumer API and secret keys.
5.  Authorise your Twitter app and account by running this command in your terminal (replacing `<key>`and `<secret>` with your unique keys):

    twurl authorize -consumer-key <key> -consumer-secret <secret>

6\. Twurl returns a URL. Copy and paste this into a browser to receive a PIN.

7\. Copy and paste the PIN into your terminal and press Enter.

Now, you’re good to go! See Twitter’s docs on [authentication](https://developer.twitter.com/en/docs/basics/authentication/guides/securing-keys-and-tokens) for more information.

### 🌪️ How to use Twurl

Twurl is basically cURL that has been modified specifically for the Twitter API. It grants an access token for you and signs all subsequent requests you send with that access token.

For guidelines on basic usage, you can run `twurl -h` help command in your terminal. The most useful options are:

    **-d, --data [data]  **                
    Sends the specified data in a POST request to the HTTP server.
    **-A, --header [header] **             
    Adds the specified header to the request to the HTTP server.
    **-H, --host [host] **                 
    Specify host to make requests to (default: api.twitter.com)
    **-X, --request-method [method]  **    
    Request method (default: GET)
    **-f, --file [path_to_file] **         
    Specify the path to the file to upload
    **-F, --file-field [field_name]  **    
    Specify the POST parameter name for the file upload data (default: media)

For a basic tutorial on how it works run: `twurl -T` or `twurl --tutorial` .

### 📮 Update your Twitter status

You can update your Twitter status using the `statuses/update` POST endpoint. As the [documentation](https://developer.twitter.com/en/docs/tweets/post-and-engage/api-reference/post-statuses-update) says this “updates the authenticating user’s current status” (also known as sending a Tweet).

To update my Twitter status to read “Testing out the Twitter API…” I sent the following request:

    twurl -d 'status=Testing out the Twitter API...' /1.1/statuses/update.json | jq

This is how the Tweet I sent using Twurl appears:

<blockquote class="twitter-tweet">tweet<a href="https://twitter.com/scottydocs/status/1097511310961639427"></a></blockquote><script async="" src="https://platform.twitter.com/widgets.js" charset="utf-8"></script>

### 📀 Upload media to Twitter

You can also upload the following media to Twitter using Twurl:

*   An image up to 5MB in size.
*   A GIF up to 15MB in size.
*   A video up to 15MB in size.

To upload a file from your computer you can use the `media/upload` endpoint:

    twurl -X POST -H upload.twitter.com "/1.1/media/upload.json" -f <file_location> -F <file_type>

For example, to upload a GIF from my desktop I ran the following command:

    twurl -X POST -H upload.twitter.com "/1.1/media/upload.json" -f ~/Desktop/itworked.gif -F media

The response contains the media ID you need to post it to Twitter:

    {  
      "media_id": 1097859492425973760,  
      "media_id_string": "1097859492425973760",  
      "size": 469653,  
      "expires_after_secs": 86400,  
      "image": {  
      "image_type": "image/gif",  
      "w": 500,  
      "h": 271  
      }  
    }

You can read more about uploading media to Twitter [here](https://developer.twitter.com/en/docs/media/upload-media/overview).

### 📟 Respond to a Tweet

You can upload a post in response to previous Tweet using the `statuses/update` POST endpoint once more.

To update my previous Tweet with a response containing the GIF I uploaded, I sent the following request:

    twurl -X POST -H api.twitter.com "/1.1/statuses/update.json?status=@scottydocs It worked&in_reply_to_status_id=1097511310961639427&media_ids=1097859492425973760" | jq

The response appeared on Twitter as follows:

<blockquote class="twitter-tweet">tweet<a href="https://twitter.com/scottydocs/status/1097518502573948928"></a></blockquote><script async="" src="https://platform.twitter.com/widgets.js" charset="utf-8"></script>

### 🚀 Retrieve Tweets with a specific hashtag

You can retrieve all Tweets with a specific hashtag using the `search/tweets` GET endpoint. By default this only retrieves Tweets that have been sent in the previous seven days.

For example, if you wanted to retrieve all Tweets which have used the hashtag #starwars you could run:

    twurl "/1.1/search/tweets.json?q=#starwars"

Alternatively, to retrieve the most popular Tweets with the #starwars hashtag you could run:

    twurl "/1.1/search/tweets.json?q=#starwars&result_type=popular"

### 📈 Find trends for your local area

To find out what is trending in your location, you can use the `trends/place` GET endpoint. The only mandatory field you need to provide is the Yahoo! Where on Earth ID (WOEID) for your location. I found mine using [this site](http://woeid.rosselliot.co.nz/).

For example, if I want to find out the latest things trending on Twitter in London (WOEID 44418):

    twurl "/1.1/trends/place.json?id=44418" | jq

The response looks like this:

<script src="https://gist.github.com/Jwscott22/7f2524326cd96f366c19081a0c8f5c1b.js"></script>

### 🤖 What else can you do?

These are just some of the basic functions you can invoke using the Twitter API and Twurl. If you want to take things a step further, you can use these endpoints and others to create Twitter bots. Here are some resources that might be useful:

*   [Twitter Bots Tutorials](https://digitalinspiration.com/docs/twitter-bots).
*   [How to make a Twitter bot: A full guide for beginners](https://learn.g2crowd.com/how-to-make-a-twitter-bot).
*   [How to make a Twitter bot in under an hour](https://medium.com/science-friday-footnotes/how-to-make-a-twitter-bot-in-under-an-hour-259597558acf).

Some potential use cases for bots you could build include:

*   Retweeting and sharing content with a specific hashtag.
*   Displaying live updates about a certain topic or hashtag.
*   Reminding yourself or your followers about specific events.

Hopefully some of this guide was helpful. Good luck sending your first Tweets using the Twitter API or possibly even building something far cooler!
