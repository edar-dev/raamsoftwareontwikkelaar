[![Netlify Status](https://api.netlify.com/api/v1/badges/fa1083f1-955b-4d4d-9794-5d5f80752868/deploy-status)](https://app.netlify.com/sites/raamsoftwareontwikkelaar/deploys)

https://hugomods.com/docs/docker/#start-hugo-server

docker pull hugomods/hugo

docker run -p 1313:1313 -v ${PWD}:/src hugomods/hugo hugo server -D --bind 0.0.0.0
