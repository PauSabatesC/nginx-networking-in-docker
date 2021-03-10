## http80-maintenance-web

Run it to create a ngix webserver on port 80 to return an html maintenance webpage while deploying or maintaning your main webserver.

```sh
docker run -d -p 80:80 --name maintanance-page pausabates/http80-maintenance-web:latest
```

- HTTPS:

Your web will normally run after a lb or reverse proxy that redirects https to http.

If your web is the last layer to internet and receives ssl connections, use this other docker: [here](../nginx-https443-maintenance-web/README.md)

---

(Handy commands just for myself for new images deploys):
```
1.- docker build -t http80-maintenance-web .
2.- docker run -rm -it -p 80:80 http80-maintenance-web
3.- docker tag {IMAGE_ID} pausabates/http80-maintenance-web:X.X.X
4.- docker push pausabates/http80-maintenance-web:X.X.X
```


