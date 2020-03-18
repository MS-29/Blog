## Deploy React Application

- Provision an [Amazon Linux 2 AMI EC2 Instance][1]
- Install Packages
  - Nginx
    - `sudo amazon-linux-extras install nginx1.12`
  - Git
    - `sudo yum install git`
  - Node
    - `curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.34.0/install.sh | bash`
    - `. ~/.nvm/nvm.sh`
    - `nvm install <VERSION_NO>`
  - Yarn (_if you preferred Yarn as your Package Manager_)
    - `npm install -g yarn`
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
- Move to your preffered directory (i.e. ~/projects/) where you want to clone your Project.
- Clone your Github Project
  - `git clone <GITHUB_REPOSITORY_URL>`
- Install all the NPM Packages
  - `npm install` or `yarn install`
- Build your Project
  - `npm run build` or `yarn build`
- Deploy your Project
  - Add the following scripts in the package.json
    - `"deploy": "pm2 start server.js --name example --max-memory-restart 700M --node-args='--max_old_space_size=500'"`
  - `npm run deploy` or `yarn deploy`
- Congrats, You have completed to deploy your Application. Now, Check the Website at your Preferred Browser.

[1]: https://github.com/MahediSabuj/blog/blob/master/src/Amazon-Web-Service/Launch-EC2-Instance.md
