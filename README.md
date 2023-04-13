<p align="center">
    <h1 align="center">docker-puppeteer</h1>
</p>

Base environment docker image for Puppeteer (Headless Chrome Node API)  
**This project has been deprecated. Please use [`puppeteer` official image](https://pptr.dev/guides/docker/).**


## Getting started

### Start node application
Run the container by passing node -e "<yourscript.js content as a string> as the command:

```bash
docker run -i --rm --cap-add=SYS_ADMIN \
    --name puppeteer-chrome zenato/puppeteer \
    node -e "`cat yourscript.js`"
```

### Start with your docker application
Write your Dockerfile and run:

```
FROM zenato/puppeteer

USER root

...

CMD node your-application
```

- See more example - https://github.com/zenato/puppeteer-renderer
