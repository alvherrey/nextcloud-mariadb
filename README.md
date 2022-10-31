# nextcloud-mariadb
Nextcloud with MariaDB


## Configure files:

nextcloud_config/config.php
```
  'trusted_domains' => 
    array (
      0 => '192.168.1.10:8001',
      1 => 'https://nextcloud.alvarocloud.com',
      2 => 'nextcloud.alvarocloud.com',
    ),
    'trusted_proxies'   => ['127.0.0.1'],
    'overwritehost'     => 'nextcloud.alvarocloud.com',
    'overwriteprotocol' => 'https',
    'datadirectory' => '/var/www/html/data',
    'dbtype' => 'mysql',
    'version' => '24.0.5.1',
    'overwrite.cli.url' => 'nextcloud.alvarocloud.com',
    'dbname' => 'nextcloud',
    'dbhost' => 'mariadb:3306'
```

nginx-certbot/conf/nginx.conf
```
    client_max_body_size 100G;
    client_body_buffer_size 400M;

```
