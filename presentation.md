<!-- page_number: true
     $theme: gaia
     template: invert
     prerender: true
     $height: 768
     $width: 1360


     _footer: github.com/jackdesert/pyramid-presentation

-->




Pyramid
==

Treasures In Store?

# ![](images/pyramid_photo_1.jpg)

---


Who am I?
==

---

Who am I and Why am I Writing Python?
==

<!-- Flexibility at BIP as to what language -->
Jack Desert
Developer for Hire
Lots of Rails Experience
Aspires to be Data Scientist

---

Framework Choices
==
<!-- How did I Choose Pyramid -->


* Flask
* Pylons
* Pyramid (a simpler Pylons)
* Zope
* Look Ma, No Framework!

---


How Did I Choose Pyramid
==

<!-- SlashDB -->

* Which ORM do I want to use?
* Which frameworks easily support that ORM?
* What (Python) frameworks have I used before?
* What are other people using?

---




Basic Web App
==
<!-- Reminds me of basic flask apps -->

    from wsgiref.simple_server import make_server
    from pyramid.config import Configurator
    from pyramid.response import Response


    def hello_world(request):
        name = request.matchdict['name']
        return Response(f'Hello {name}')

    if __name__ == '__main__':
        with Configurator() as config:
            config.add_route('hello', '/{name}')
            config.add_view(hello_world, route_name='hello')
            app = config.make_wsgi_app()
        server = make_server('0.0.0.0', 8080, app)
        server.serve_forever()


---

The Magic is in the CookieCutters
==

* Bootstraps your ORM and template engine of choice
* Sets up a common directory structure


---

CookieCutters 101
==

1. Choose a cookiecutter from  https://cookiecutter.readthedocs.io/en/latest/readme.html#python-pyramid
2. Find the invocation in the README
3. Follow steps printed after invocation
4. env/bin/pserve and /env/bin/pshell

---

Stethoscope
==

A location predictor
Uses bluetooth

---
# ![](images/house_with_walls.png)

---

API
==
bip-stethoscope.elitecare.com


---

What I Expect from a Framework (1)
==

Serve static assets in development

    config.add_static_view(name='static',
                           path='/var/www/static')
---

What I Expect from a Framework (2)
==

Reload code in development

    env/bin/pserve development --reload



---

What I Expect from a Framework (3)
==

Plays nicely with nginx

(Had no problems with waitress + nginx via tcp)

---

What I Expect from a Framework (4)
==

4. Popularity
6. No Bugs
7. Template integration
8. Consistency
9. REPL-based development
10. Console
11. Documentation

---

Using it in Production
==
1. Logger?
2. Training Keras ~ 500MB resident size
3. uWSGI is a rabbit hole!! (waitress + systemd is much easier)
---

Rabbit Hole!! :hole: :rabbit: :hole:
==

## Serving via uWSGI

(Built-in `waitress` server + systemd is much easier)

---

Will I use Pyramid in the Future?
==
Yes!

1. arscca.jackdesert.com
2. dan.jackdesert.com
3. drive.jackdesert.com
4. shop.jackdesert.com
5. website-monitor.jackdesert.com (coming soon)

---

Preparation
==

* Put podium near stage right looking out
* mon4
* Press home button twice on back of white remote to get lamp warning to go away
* If screen does not respond, for example after running on laptop monitor for a long time, unplug and replug HDMI cord into laptop
* If screen does not respond, for example after running on laptop monitor for a long time, unplug and replug HDMI cord into lapto
* Bring power adapter
* Bring extension cord for power
* Microphone is available...LP1
* Check screen resolution
* Find a way to make in-browser stuff big enough (CTRL-PLUS makes everything but the url bar bigger)(What about bigger icons or lower resolution?)
* Make in-terminal stuff big enough (CTRL-SHIFT-PLUS)
* Export slides and make available on github (post to meetup?)
* Create a cookiecutter project ahead of time in case no internet
* Take keyboard so you can type fast
* Get Internet Connection while there
* Check IP address from there
* Print slides: 1366x768 and 1360x768
* Print slips of paper with
  - bip-stethoscope.elitecare.com (Do we want to remap to pyramid-demo.jackdesert.com?
  - Pyramid
  - github.com/jackdesert/arscca
  - arscca.jackdesert.com
  - list of all sites and source code I've built using pyramid
  - link to cookiecutters
  - link to this presentation
* Make a backup of stethoscope database so I can wipe it after these guys clobber it
* Write in to meetup to ask them to bring laptops if they want to poke the API
* Put source code to arscca on github so people can see it