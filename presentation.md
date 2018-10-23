<!-- page_number: true 
     $theme: gaia
     template: invert
     prerender: true


     _footer: github.com/jackdesert/pyramid-presentation

-->




Pyramid
==
Why you want it

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

Preparation
==

* Bring power adapter
* Check screen resolution 
* Find a way to make in-browser stuff big enough (CTRL-PLUS makes everything but the url bar bigger)(What about bigger icons or lower resolution?)
* Make in-terminal stuff big enough (CTRL-SHIFT-PLUS)
* Export slides and make available on github (post to meetup?)
* Create a cookiecutter project ahead of time in case no internet
