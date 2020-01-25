```
docker build --tag=grav-dev .
docker run -d -p 8000:80 -v $(pwd):/path/to/grav/site grav-dev
```
