# chatbot-android


## Getting Started
You will need to create a local.properties file with these 2 variables:

```
DEBUG_INDEX_PAGE=
PRODUCTION_INDEX_PAGE=
```

To test with production please set both variables to

```
DEBUG_INDEX_PAGE=https://frontend-cs536.escglobal.co/
PRODUCTION_INDEX_PAGE=https://frontend-cs536.escglobal.co/
```

## The following steps are for debugging using a local chatbot-server, which will only work with http


To view the webpage, I recommend using something like [ngrok](https://ngrok.com/) to expose your localhost.

Once you have ngrok installed, start ngrok by the command:

```
ngrok http ${YOUR_LOCAL_DEV_BACKEND}
```

Then we can cd to the chatbot-server repository and in the root of the repository, we can run:

```
BACKEND_URL=${YOUR_NGROK_LINK_FROM_ABOVE} npm run serve
```

The above command will build a static front end and then use the local back end to serve the static files.

Finally, replace the value of `DEBUG_INDEX_PAGE` with the ngrok link. Then build + run the application with Android Studio.

In the future, we can look into setting up a staging environment for agility.
