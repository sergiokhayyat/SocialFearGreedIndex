# SocialFearGreedIndex
Simple fear &amp; greed global index using social data.

Sentiment analysis is powered by [Machinebox](http://machinebox.io/)'s textbox.

## Usage

- Check your host configuration is OK for elasticsearch (if using swarm, all hosts which may run ES must have `vm.max_map_count` set to at least 262144, `sysctl -w vm.max_map_count=262144`; see https://www.elastic.co/guide/en/elasticsearch/reference/current/docker.html )
- Edit `docker-compose.yml` to add your twitter credentials (`TWITTER_*` environment variables) and machinebox key (`MB_KEY`)
- Use docker swarm or docker-compose to deploy this stack (`docker stack deploy -c docker-compose.yml sfgi`)
- Access kibana on port **80** (you can change it editing the `docker-compose.yml`)
- Use the index call "tweets"

## Architecture

This is the diagram of the components that are deployed:

![Module Diagram](module-diagram.png)

