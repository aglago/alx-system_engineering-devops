# Web Server

## Table of Content
- [What is Nginx](#what-is-nginx)

## What is Nginx
Nginx is a software web server that serves static web content.

Nginx is capable of hosting multiple websites (also known as virtual hosts or server blocks) on the same server. Each website can have its domain name (e.g., `example.com`, `fish.com`, `animal.io`) and configuration settings within separate `server` blocks. This allows Nginx to efficiently serve different websites or web applications from a single server instance.

## Installation and configuration files

It is installed with:
```bash
sudo apt-get install nginx
```
When installed, a directory is created under `/etc/` called `nginx` which will contain all the configuration files for the nginx software. Lets go over the files and durectories that will be inside the `/etc/nginx`.

## `/etc/nginx`

Inside the `/etc/nginx` directory, you'll typically find several important directories and files that play specific roles in the configuration and operation of Nginx:

1. **nginx.conf**: This is the main configuration file for Nginx. It contains global settings and directives that apply to the entire server. This includes settings like worker processes, error log paths, and include statements for additional configuration files.

2. **sites-available/**: This directory typically contains configuration files (server blocks) for individual websites or applications that Nginx can serve. These configuration files define settings specific to each site, such as domain names, root directories, SSL configurations, and more.

3. **sites-enabled/**: This directory contains symbolic links to configuration files from `sites-available` that are currently active or enabled. Nginx only reads and applies configurations from files that are symbolically linked from `sites-enabled`.

4. **conf.d/**: This directory is used for additional configuration snippets that can be included in `nginx.conf` or server blocks. Each file within `conf.d` contains specific directives that can be included using `include` statements.

5. **mime.types**: This file defines MIME types mappings used by Nginx for content-type determination when serving files.

6. **fastcgi_params**, **proxy_params**, **scgi_params**, **uwsgi_params**: These files contain default parameters used by Nginx when working with FastCGI, proxying requests, etc.

7. **sites-available/default**: A default configuration file that defines a basic server block for Nginx. It serves as a starting point for configuring specific websites or applications.

## Configuring Nginx

We configure Nginx using what we call directives.

Directives are fundamental components used in configuring Nginx. They are keywords or parameters that specify how Nginx should operate and handle various aspects of web server functionality.

Directives are in 2 forms, simple and block directives. Simple is a single line while block is a name and a curly braces with other simple directives or block directives in it, while a context is a block directive that has other directives in them.

To follow along, open `/etc/nginx/nginx.conf` file.

Forexample:
```
user www-data;
worker_processes auto;
pid /run/nginx.pid;
include /etc/nginx/modules-enabled/*.conf;
events {
        worker_connections 768;
        # multi_accept on;
}
```

The `user`, `worker_processes`, `pid` and `include` lines are simple directives.

While events, `http`, `mail`, `server` are block directives or contexts.

Let's start from what each directives is responsible for. Let's take each directive one at a time.

### `user www-data;`
This directive specifies the user and group Nginx will run as after starting. Here, www-data is the user under which Nginx processes will run. This is important for security, ensuring that Nginx doesn't run with higher privileges than necessary.

The www-data user is a system user created during the installation of web server software like Nginx. It's a standard user used to run web server processes securely. The name "www-data" is just a convention and isn't related to website addresses.

### `worker_processes`
This directive sets the number of worker processes. These processes handle the actual work of serving requests. Setting it to auto lets Nginx automatically determine the optimal number of worker processes based on the number of CPU cores. This helps maximize performance by utilizing available resources efficiently.

### `pid /run/nginx.pid;`
This directive specifies the file where Nginx will store its process ID (PID). The PID is a unique number assigned to each running process in the system. By storing it in /run/nginx.pid, Nginx (and system administrators) can easily manage and identify the running Nginx process, such as stopping or restarting it.

### `include /etc/nginx/modules-enabled/*.conf;`
This directive tells Nginx to include and process all configuration files ending in `.conf` from the `/etc/nginx/modules-enabled/` directory. This is useful for modular configuration, allowing you to enable or disable modules by simply adding or removing configuration files in this directory.

### `events {...}`
The events block should have directives that manage how Nginx handles network connections. Network connection-related directives involve:
+ Handling incoming requests (e.g., `worker_connections` to set the number of connections each worker can handle). 
+ Optimizing performance (e.g., `multi_accept` to accept multiple connections simultaneously).
+ Event handling mechanisms (e.g., `use` to specify the event method).
These settings directly affect how Nginx deals with traffic, ensuring efficient processing and resource use.

### `http {...}`
Within the `http` block in Nginx configuration, you'll find directives that govern how HTTP requests are processed and responded to. These include:

- **server**: Defines settings for a specific virtual server, such as its domain name and root directory.
- **location**: Specifies how Nginx should handle different URIs within a server block.
- **include**: Allows including additional configuration files.
- **error_page**: Configures custom error pages for HTTP status codes.

The `error_page` directive in Nginx allows you to specify custom pages to display when specific HTTP status codes are returned. For example:

```nginx
error_page 404 /404.html;
error_page 500 502 503 504 /50x.html;
```

Each `server` block can have its own root directory, domain name, SSL configuration, error pages, and more, making Nginx highly versatile for hosting diverse web content.                                                                                                              It has a configuration file at `/etc/nginx/nginx.conf`. 
The configuration file is a set of instructions that helps nginx to serve websites efficiently.
                                                        In the configuration file are what we call directives which are used to control what modules are included or not.
