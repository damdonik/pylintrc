server {
    listen 80;
    server_name example.com;

    location / {
        return 200 "Hello, World!\n";
    }
}
