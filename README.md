# HTTP2 Enabled Nginx Docker Image with PHP

HTTP2 Enabled Nginx PHP Docker image, with sample TLS configuration
This image also has resource compression preconfigured.

## Running

To build the image, you need to have the TLS Certificate. You can get one for free at [LetsEncrypt](https://letsencrypt.org/). Place the certificate private key and the certificate file in the `certs` directory under a subdirectory with your desired domain name (e.g. www.example.com).

Edit the `site.conf` file and replace all occurrences of *www.example.com* with your domain name. 

After you have completed the previous steps, just run\
```docker compose up -d```\
and you're all set.

## Troubleshooting

### Log files
You can inspect the log files in the mounted volume directory provided during the run command (`logs` directory on host).