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

# rubyのversionを確認する時
①ruby -v　ではローカルPCが使用しているrubyの環境が表示されてしまう
ruby 2.6.10p210 (2022-04-12 revision 67958) [universal.x86_64-darwin24]のような感じ
②docker run runteq-ruby ruby -v　で、dockerのコンテナのrunteq-rubyタグで使用しているverを知るとき
ruby 3.0.7p220 (2024-04-23 revision 724a071175) [x86_64-linux]って表示される

