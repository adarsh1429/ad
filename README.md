## Download tokens.json to Multiple Locations and Restart Services

You can download the `tokens.json` file to multiple locations and then restart all services using the following commands:

1. Download the `tokens.json` file to multiple locations:

    ```bash
    for path in "/root/semrush_yt_scraper/tokens.json" "/root/semrush_ig_posts_scraper/tokens.json" "/root/semrush_tiktok/tokens.json" "/root/semrush_yt_videos_scraper/tokens.json" "/root/semrush_insta_scraper/tokens.json" "/root/semrush_yt_id_scraper/tokens.json"; do wget -O $path https://raw.githubusercontent.com/adarsh1429/ad/main/token.json; done
    ```

2. Restart all services using `supervisorctl`:

    ```bash
    sudo supervisorctl restart all
    ```

These commands will download the `tokens.json` file from the specified URL to each of the paths listed and then restart all services managed by Supervisor.
