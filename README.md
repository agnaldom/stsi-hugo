# Semana de Tecnologia e Segurança da Informação
Site da Semana de Tecnologia e Segurança da  Informação

## Hugo Docker image

[Hugo](https://gohugo.io/) is a fast and flexible static site generator, written in Go. 
Hugo flexibly works with many formats and is ideal for blogs, docs, portfolios and much more. 
Hugo’s speed fosters creativity and makes building a website fun again.

This Lightweight Docker Image is based on Alpine, and comes with rsync for Continuous Deployment.

## Running

To print Hugo Help:

``bash
docker run --rm -it jguyomard/hugo-builder hugo help
``

To create a new Hugo managed website:

``bash
docker run --rm -it -v $PWD:/src -u hugo jguyomard/hugo-builder hugo new site mysite
cd mysite
``

To build your site:
 
``bash
docker run --rm -it -v $PWD:/src -u hugo jguyomard/hugo-builder hugo
``

To serve your site locally:

``bash
docker run --rm -it -v $PWD:/src -p 1313:1313 -u hugo jguyomard/hugo-builder hugo server -w --bind=0.0.0.0
``

Then open [`http://localhost:1313/`](http://localhost:1313/) in your browser.
