# NewsFeed - A news aggregator

Solution for the innoscripta take home challenge.

This compose setup pulls the code from the remote git repositories and provides options to customize the frontend and backend ports in the _.env_ file. Default ports used are: **8000** for the **backend** and **3000** for the **frontend**.

### How to run this?

- Clone this repository.
- If you want to change the frontend and backend ports you can update them in the .env file.
- Run the docker compose command: `docker-compose up -d`.

**Voila! That's it—you should now be up and running and see a screen similar to this one:**



**Now go to the browser and access the NewsFeed app at [http://localhost:3000](http://localhost:3000). (Change the port 3000 to the one you added in the .env file)**

### Next Steps:

Initially news database is empty. Follow these steps to pull the articles from the news sources.

1. Login as admin user using the shared credentials.
2. Navigate to Admin page.
3. Pull the news articles from the provided sources.

Alternatively you can run the below artisan command in the backend docker container:

`php artisan news:pull --source=SOURCE_OPTION`

Available source options are: NewsApi, NewsData, TheGuardian, NyTimes.
