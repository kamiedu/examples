# Building Your First Jina App

## Files and Folders

After running cookiecutter, you should see a new folder called `south_park`. Let's have a look inside:

| File               | What it Does                                                             |
| ---                | ---                                                                      |
| `app.py`           | The main Python script where you initialize and pass data into your Flow |
| `Dockerfile`       | Lets you spin up a Docker instance running your app                      |
| `flows/`           | Folder to hold your flows                                                |
| `pods/`            | Folder to hold your pods                                                 |
| `README`           | The index to this tutorial                                               |
| `requirements.txt` | A list of requirements for `pip`                                         |

In the `flows/` folder we can see `index.yml` and `query.yml` - these define the indexing and querying Flows for your app.

In `pods/` we see `chunk.yml`, `craft.yml`, `doc.yml`, and `encode.yml` - these Pods are called from the Flows to process data for indexing or querying.