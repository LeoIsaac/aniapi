# aniapi
アニメの詳細な情報を、誰もが自由に使えるように


## About
アニメのAPIと言えば、秋葉原IT戦略研究所の[穹](https://github.com/Project-ShangriLa/sora-playframework-scala)が有名だが、正直申し上げて情報が足りない。かと言ってプルリクを送る勇気も無ければ、Javaあまり出来ない...

海外のサービスは結構良い線行っていて、[AniList](https://anilist.co/)が提供しているAPIなんかはまさに自分が欲していたAPIだ。だが日本語向きのサービスじゃない...

そこでRuby学習ついでにAPIサーバ作ってみることにした。


## Usage
```
git clone git@github:leoisaac/aniapi && cd aniapi
docker run -itd --name aniapi -v $(pwd):/mnt --workdir /mnt -p 80:3000 rails:5.0 bash -c 'bundle install && bash'
```
これでDockerコンテナを立ち上げます。

あとは、`docker exec -it aniapi rails server -b 0.0.0.0`すれば`http://localhost/`で確認できます。
