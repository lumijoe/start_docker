# start_docker
学習用Dockerテスト

# docker build -t runteq-ruby .　コマンド決める.はレシピ通りでってこと
# docker images 使用する食材の一覧
# docker run runteq-ruby　走らせる
rubyファイルの中身がターミナルで表示される

# ポーターというログチェックやアプリ実行サイトで確認することもそのうちできる
docker volume create portainer_data
docker run -d -p 9000:9000 \
  --name portainer \
  --restart=always \
  -v /var/run/docker.sock:/var/run/docker.sock \
  -v portainer_data:/data \
  portainer/portainer-ce

