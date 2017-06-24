# Get started

Swoole framework is released as a PHP extension \(PECL\) and run as a PHP CLI application.

## [Installation](/get-started/installation.md)

## Run the first Swoole program

Write your first HTTP server with Swoole in PHP:

1. Save the hello world source code as file *server.php*

    ``` php

    $http = new swoole_http_server("127.0.0.1", 9501);

    $http->on('request', function ($request, $response) {

        $response->header("Content-Type", "text/html; charset=utf-8");

        $response->end("<h1>Hello World. #".rand(1000, 9999)."</h1>");

    });

    $http->start();
    ```

2. Execute the command: php sever.php to run swoole HTTP server. \(Show developer friendly message\)

3. See the result in your browser: open [http://127.0.0.1:9501/](http://127.0.0.1:9501/)

#### 


