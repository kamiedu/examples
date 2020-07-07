## Try it Out!

### With Docker

We've prepared a Docker image with indexed data. You can run it with:

```bash
docker run -p 45678:45678 jinaai/hub.app.distilbert-southpark
```

Check out more details about the Docker image [here](rest-api/README.md).

Note: You'll need to run the Docker image before trying the steps below

#### Querying with Jinabox

1. Go to [jinabox](https://jina.ai/jinabox.js) in your browser
2. Ensure you have the server endpoint set to `http://localhost:45678/api/search`
3. Type a phrase into the search bar and see which South Park lines come up

Find out more about [jinabox.js](https://github.com/jina-ai/jinabox.js/), including how to use the front-end code in your own project.

#### Querying with `curl`

Alternatively, you can open your shell and check the results via the RESTful API. The matched results are stored in `topkResults`.

```bash
curl --request POST -d '{"top_k": 10, "mode": "search",  "data": ["text:hey, dude"]}' -H 'Content-Type: application/json' 'http://0.0.0.0:45678/api/search'
```