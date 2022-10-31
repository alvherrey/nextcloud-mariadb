# nextcloud-mariadb
Nextcloud with MariaDB


## Configure files:

nextcloud_config/config.php
```
  'trusted_domains' => 
    array (
      0 => '192.168.1.10:8001',                     # ip of the host
      1 => 'https://nextcloud.xxxxxxxxxxxx.com',    # my domain
      2 => 'nextcloud.xxxxxxxxxxxx.com',
    ),
    'trusted_proxies'   => ['127.0.0.1'],
    'overwritehost'     => 'nextcloud.xxxxxxxxxxxx.com',
    'overwriteprotocol' => 'https',
    'datadirectory' => '/var/www/html/data',
    'dbtype' => 'mysql',
    'version' => '24.0.5.1',
    'overwrite.cli.url' => 'nextcloud.xxxxxxxxxxxx.com',
    'dbname' => 'nextcloud',
    'dbhost' => 'mariadb:3306'
```

nginx-certbot/conf/nginx.conf
```
    client_max_body_size 100G;
    client_body_buffer_size 400M;

```
