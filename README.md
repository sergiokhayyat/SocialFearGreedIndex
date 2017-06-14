# SocialFearGreedIndex
Simple fear &amp; greed global index using social data.

Sentiment analysis is powered by [Machinebox](http://machinebox.io/)'s textbox.

## Usage

- Edit `docker-compose.yml` to add your twitter credentials (`TWITTER_*` environment variables) and machinebox key (`MB_KEY`)
- Use docker swarm or docker-compose to deploy this stack (`docker stack deploy -c docker-compose.yml sfgi`)
- Access kibana on port **80** (you can change it editing the `docker-compose.yml`)
- Use the index call "tweets"

## Architecture

This is the diagram of the components that are deployed:

![Module Diagram](module-diagram.png)

