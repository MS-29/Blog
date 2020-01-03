## Deploy React Application

- Provision an [Amazon Linux 2 AMI EC2 Instance][1]
- Install Nginx
  - `sudo amazon-linux-extras install nginx1.12`
- Configure Nginx
  - Move to `/etc/nginx/conf.d/`
  - Create a configuration file for your website such as `example-com.conf` [_It is best practice to create the file name as your website name_]
  - Update the content of the file as follows
    ```Nginx
      server {
        listen 80;
        server_name example.com;
        
        gzip on;
        gzip_http_version 1.1;
        gzip_vary on;
        gzip_comp_level 6;
        gzip_buffers 16 8k;
        gzip_types text/plain text/html text/css text/javascript text/xml 
            application/javascript application/json application/xml;
        
        location / {
          proxy_pass http://127.0.0.1:3000; #App need to run at 3000 port
        }
      }
    ```
  - Start the Nginx (_Run any of the following_)
    - `sudo systemctl start nginx`
    - `sudo service nginx start`

[1]: https://github.com/MahediSabuj/blog/blob/master/src/Amazon-Web-Service/Launch-EC2-Instance.md
