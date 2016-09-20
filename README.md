A dockerized version of the reveal-md presentation software. To try it out, just do:

docker run -d -p 8000:1948 muellermich/reveal-md:latest
And open a browser to http://localhost:1948

To use your own slides in Markdown format use the -v flag e.g:

docker run -d -p 8000:1948 -v /path/to/my/slides.md:/usr/src/app/slide.md muellermich/reveal-md:latest

You can use the the test slides to get an idea for the formatting.

If you need to include other files e.g. images, keep them with the presentation file and just mount the directory e.g:

docker run -d -p 8000:1948 -v /my/slide/dir:/usr/src/app/ muellermich/reveal-md:latest

To build your own version just clone https://github.com/webpro/reveal-md and modify the Dockerfile as you want