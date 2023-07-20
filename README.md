# Yolks tini

A curated collection of core images that can be used with Pterodactyl's Egg system. Each image is rebuilt
periodically to ensure dependencies are always up-to-date.

Images are hosted on `ghcr.io` and exist under the `games`, `installers`, and `yolks` spaces. The following logic
is used when determining which space an image will live under:

* `games` — anything within the `games` folder in the repository. These are images built for running a specific game
or type of game.
* `installers` — anything living within the `installers` directory. These images are used by install scripts for different
Eggs within Pterodactyl, not for actually running a game server. These images are only designed to reduce installation time
and network usage by pre-installing common installation dependencies such as `curl` and `wget`.
* `yolks` — these are more generic images that allow different types of games or scripts to run. They're generally just
a specific version of software and allow different Eggs within Pterodactyl to switch out the underlying implementation. An
example of this would be something like Java or Python which are used for running bots, Minecraft servers, etc.

All of these images are available for `linux/amd64` and `linux/arm64` versions, unless otherwise specified, to use
these images on an arm system, no modification to them or the tag is needed, they should just work.

## Contributing

When adding a new version to an existing image, such as `java v42`, you'd add it within a child folder of `java`, so
`java/42/Dockerfile` for example. Please also update the correct `.github/workflows` file to ensure that this new version
is tagged correctly.

## Available Images

### [Oses](/oses)

* [alpine](/oses/alpine)
  * `quintenqvd/pterodactyl_tini:alpine`
* [debian](/oses/debian)
  * `quintenqvd/pterodactyl_tini:debian`
* [ubuntu](/oses/ubuntu)
  * `quintenqvd/pterodactyl_tini:ubuntu`

### [Bot](/bot)

* [`bastion`](/bot/bastion)
  * `quintenqvd/pterodactyl_tini:bot_bastion`
* [`parkertron`](/bot/parkertron)
  * `quintenqvd/pterodactyl_tini:bot_parkertron`
* [`redbot`](/bot/red)
  * `quintenqvd/pterodactyl_tini:bot_red`
* [`sinusbot`](/bot/sinusbot)
  * `quintenqvd/pterodactyl_tini:bot_sinusbot`

### [Box64](/box64)

* [`Box64`](/box64)
  * `quintenqvd/pterodactyl_tini:box64`

### [Cassandra](/cassandra)

* [`cassandra_java8_python27`](/cassandra/cassandra_java8_python2)
  * `quintenqvd/pterodactyl_tini:cassandra_java11_python2`
* [`cassandra_java11_python3`](/cassandra/cassandra_java11_python3)
  * `quintenqvd/pterodactyl_tini:cassandra_java11_python3`

### [Dart](/dart)

* [`dart2.17`](/dart/2.17)
  * `quintenqvd/pterodactyl_tini:dart_2.17`

### [dotNet](/dotnet)

* [`dotnet2.1`](/dotnet/2.1)
  * `quintenqvd/pterodactyl_tini:dotnet_2.1`
* [`dotnet3.1`](/dotnet/3.1)
  * `quintenqvd/pterodactyl_tini:dotnet_3.1`
* [`dotnet5.0`](/dotnet/5)
  * `quintenqvd/pterodactyl_tini:dotnet_5`
* [`dotnet6.0`](/dotnet/6)
  * `quintenqvd/pterodactyl_tini:dotnet_6`
* [`dotnet7.0`](/dotnet/7)
  * `quintenqvd/pterodactyl_tini:dotnet_7`

### [Erlang](/erlang)

* [`erlang22`](/erlang/22)
  * `quintenqvd/pterodactyl_tini:erlang_22`
* [`erlang23`](/erlang/23)
  * `quintenqvd/pterodactyl_tini:erlang_23`
* [`erlang24`](/erlang/24)
  * `quintenqvd/pterodactyl_tini:erlang_24`

### [Games](/games)

* [`altv`](/games/altv)
  * `ghcr.io/parkervcp/games:altv`
* [`arma3`](/games/arma3)
  * `ghcr.io/parkervcp/games:arma3`
* [`dayz`](/games/dayz)
  * `ghcr.io/parkervcp/games:dayz`
* [`mohaa`](games/mohaa)
  * `ghcr.io/pterodactyl/games:mohaa`  
* [`samp`](/games/samp)
  * `ghcr.io/parkervcp/games:samp`  
* [`source`](/games/source)
  * `ghcr.io/parkervcp/games:source`
* [`valheim`](/games/valheim)
  * `ghcr.io/parkervcp/games:valheim`

### [Golang](/go)

* [`go1.14`](/go/1.14)
  * `quintenqvd/pterodactyl_tini:go_1.14`
* [`go1.15`](/go/1.15)
  * `quintenqvd/pterodactyl_tini:go_1.15`
* [`go1.16`](/go/1.16)
  * `quintenqvd/pterodactyl_tini:go_1.16`
* [`go1.17`](/go/1.17)
  * `quintenqvd/pterodactyl_tini:go_1.17`
* [`go1.18`](/go/1.18)
  * `quintenqvd/pterodactyl_tini:go_1.18`
* [`go1.19`](/go/1.19)
  * `quintenqvd/pterodactyl_tini:go_1.19`

### [Java](/java)

* [`java8`](/java/8)
  * `quintenqvd/pterodactyl_tini:java_8`
* [`java11`](/java/11)
  * `quintenqvd/pterodactyl_tini:java_11`
* [`java16`](/java/16)
  * `quintenqvd/pterodactyl_tini:java_16`
* [`java17`](/java/17)
  * `quintenqvd/pterodactyl_tini:java_17`
* [`java19`](/java/19)
  * `quintenqvd/pterodactyl_tini:java_19`

### [MariaDB](/mariadb)

  * [`MariaDB 10.3`](/mariadb/10.3)
    * `quintenqvd/pterodactyl_tini:mariadb_10.3`
  * [`MariaDB 10.4`](/mariadb/10.4)
    * `quintenqvd/pterodactyl_tini:mariadb_10.4`
  * [`MariaDB 10.5`](/mariadb/10.5)
    * `quintenqvd/pterodactyl_tini:mariadb_10.5`
  * [`MariaDB 10.6`](/mariadb/10.6)
    * `quintenqvd/pterodactyl_tini:mariadb_10.6`
  * [`MariaDB 10.7`](/mariadb/10.7)
    * `quintenqvd/pterodactyl_tini:mariadb_10.7`

### [MongoDB](/mongodb)

  * [`MongoDB 4`](/mongodb/4)
    * `quintenqvd/pterodactyl_tini:mongodb_4`
  * [`MongoDB 5`](/mongodb/5)
    * `quintenqvd/pterodactyl_tini:mongodb_5`
 * [`MongoDB 6`](/mongodb/6)
    * `quintenqvd/pterodactyl_tini:mongodb_6`    

### [Mono](/mono)

* [`mono_latest`](/mono/latest)
  * `quintenqvd/pterodactyl_tini:mono_latest`

### [Nodejs](/nodejs)

* [`node12`](/nodejs/12)
  * `quintenqvd/pterodactyl_tini:nodejs_12`
* [`node14`](/nodejs/14)
  * `quintenqvd/pterodactyl_tini:nodejs_14`
* [`node16`](/nodejs/16)
  * `quintenqvd/pterodactyl_tini:nodejs_16`
* [`node17`](/nodejs/17)
  * `quintenqvd/pterodactyl_tini:nodejs_17`
* [`node18`](/nodejs/18)
  * `quintenqvd/pterodactyl_tini:nodejs_18`
* [`node19`](/nodejs/19)
  * `quintenqvd/pterodactyl_tini:nodejs_19`
* [`node20`](/nodejs/20)
  * `quintenqvd/pterodactyl_tini:nodejs_20`

### [PostgreSQL](/postgres)

  * [`Postgres 9`](/postgres/9)
    * `quintenqvd/pterodactyl_tini:postgres_9`
  * [`Postgres 10`](/postgres/10)
    * `quintenqvd/pterodactyl_tini:postgres_10`
  * [`Postgres 11`](/postgres/11)
    * `quintenqvd/pterodactyl_tini:postgres_11`
  * [`Postgres 12`](/postgres/12)
    * `quintenqvd/pterodactyl_tini:postgres_12`
  * [`Postgres 13`](/postgres/13)
    * `quintenqvd/pterodactyl_tini:postgres_13`
  * [`Postgres 14`](/postgres/14)
    * `quintenqvd/pterodactyl_tini:postgres_14`  

### [Python](/python)

* [`python3.7`](/python/3.7)
  * `quintenqvd/pterodactyl_tini:python_3.7`
* [`python3.8`](/python/3.8)
  * `quintenqvd/pterodactyl_tini:python_3.8`
* [`python3.9`](/python/3.9)
  * `quintenqvd/pterodactyl_tini:python_3.9`
* [`python3.10`](/python/3.10)
  * `quintenqvd/pterodactyl_tini:python_3.10`
* [`python3.11`](/python/3.11)
  * `quintenqvd/pterodactyl_tini:python_3.11`

### [Redis](/redis)

  * [`Redis 5`](/redis/5)
    * `quintenqvd/pterodactyl_tini:redis_5`
  * [`Redis 6`](/redis/6)
    * `quintenqvd/pterodactyl_tini:redis_6`
  * [`Redis 7`](/redis/7)
    * `quintenqvd/pterodactyl_tini:redis_7`

### [Rust](/rust)

* ['rust1.31'](/rust/1.31)
  * `quintenqvd/pterodactyl_tini:rust_1.31`
* ['rust1.56'](/rust/1.56)
  * `quintenqvd/pterodactyl_tini:rust_1.56`
* ['rust1.60'](/rust/1.60)
  * `quintenqvd/pterodactyl_tini:rust_1.60`
* ['rust latest'](/rust/latest)
  * `quintenqvd/pterodactyl_tini:rust_latest`

### [SteamCMD](/steamcmd)
* [`SteamCMD Debian lastest`](/steamcmd/debian)
  * `ghcr.io/parkervcp/steamcmd:debian`
* [`SteamCMD Debian Dotnet`](/steamcmd/dotnet)
  * `ghcr.io/parkervcp/steamcmd:dotnet`
* [`SteamCMD Proton`](/steamcmd/proton)
  * `ghcr.io/parkervcp/steamcmd:proton`
* [`SteamCMD Ubuntu latest LTS`](/steamcmd/ubuntu)
  * `ghcr.io/parkervcp/steamcmd:ubuntu`

### [Voice](/voice)
* [`Mumble`](/voice/mumble)
  * `quintenqvd/pterodactyl_tini:voice_mumble`
* [`TeaSpeak`](/voice/teaspeak)
  * `quintenqvd/pterodactyl_tini:voice_teaspeak`

### [Wine](/wine)

* [`Wine`](/wine)
  * `quintenqvd/pterodactyl_tini:wine_latest`
  * `quintenqvd/pterodactyl_tini:wine_staging`

### [Installation Images](/installers)

* [`alpine-install`](/installers/alpine)
  * `ghcr.io/parkervcp/installers:alpine`
* [`debian-install`](/installers/debian)
  * `ghcr.io/parkervcp/installers:debian`
* [`ubuntu-install`](/installers/ubuntu)
  * `ghcr.io/parkervcp/installers:ubuntu`
