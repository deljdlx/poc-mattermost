Doc https://docs.mattermost.com/deployment-guide/server/deploy-containers.html


### Quick start
```bash
git clone https://github.com/mattermost/docker
cd docker

mkdir -p ./volumes/app/mattermost/{config,data,logs,plugins,client/plugins,bleve-indexes}
sudo chown -R 2000:2000 ./volumes/app/mattermost

# maybe useless
# mkdir -p ./volumes/db/var/lib/postgresql/data
# sudo chown -R 2000:2000 ./volumes/db/var/lib/postgresql/data


docker compose -f docker-compose.yml -f docker-compose.without-nginx.yml up -d
```