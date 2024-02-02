#### Testing using docker image:

You can use the following steps to make a test, using the same Docker image that will be deployed in kbuild/kbuild-dev:

1. Clone the repository: [SRE-Docs](https://github.com/mulesoft/sre-docs)<br>
<br>
`git clone git@github.com:mulesoft/sre-docs.git`

2. Make your changes in a new branch:<br>
<br>
`git checkout -b <new_branch>`

3. Build the Docker image with your changes:<br>
   ```sh
    docker build -t sre-docs-kbuild-dev:latest .
   ```

4. Create a temporary folder with two file: (from <https://github.com/mulesoft/sre-docs/blob/master/helm/sre-docs/templates/config.yaml>)<br>
<br>_note: the values for listen on the both files, was taking from [values.yaml](https://github.com/mulesoft/sre-docs/blob/master/helm/sre-docs/values.yaml)_<br>
<br>`mkdir -p /tmp/sre-docs-nginx`<br><br>
metrics.conf<br>

    ```json
        server {
            listen   9831;
            server_name         127.0.0.1;
            location /server_status {
                stub_status on;
                access_log off;
                allow all;
            }
        }
    ```
    <br>static.conf
    <br>

    ```json
        server {
            listen 8080;
            gzip_static on;
            root /usr/src/app;
            location = / {
                index index.html;
            }
            location = /status/ready {
                access_log off;
                error_log off;
                return 200;
            }
            location = /status/ping {
                access_log off;
                error_log off;
                return 200;
            }
            error_page 400 401 403 404 /40x.html;
            location = /40x.html {
                root /usr/src/app/errors;
                internal;
            }
            error_page 500 502 503 504 /50x.html;
            location = /50x.html {
                root /usr/src/app/errors;
                internal;
            }
        }
    ```
5. Run the Docker image and check your changes in your browser:<br>

    ```sh
       docker run --rm -p 3000:8080 -v /tmp/sre-docs-nginx:/etc/nginx/conf.d sre-docs-kbuild-dev:latest
    ```
6. Open your browser and open the following link: <http://localhost:3000/><br>
<p align="center"><a href="./img/intro.png" target="_blank"><img src="./img/intro.png" width="55%"/></a></p>
  
