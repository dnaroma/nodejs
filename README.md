# nodejs
Dockerized Node.js 4.x LTS

## Usage
Create a `Dockerfile` and write e.g.:
```Dockerfile
FROM tangpei506/nodejs

# if your_app_port !=8000 then should EXPOSE
EXPOSE your_app_port
```
then add `"start": "node <your_app_entrypoint.js>"` to `package.json` like this:
```JSON
{
  "name": <your app name>,
  "private": true,
  "main": "index.js",
  "dependencies": {
    ... your deps
  },
  "devDependencies": {
    ... your dev deps
  },
  "scripts": {
    "start": "node index.js"
  }
}
```
