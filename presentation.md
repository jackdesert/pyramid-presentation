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
        return Response(f'Hello {request.matchdict}')

    if __name__ == '__main__':
        with Configurator() as config:
            config.add_route('hello', '/hello/{name}')
            config.add_view(hello_world, route_name='hello')
            app = config.make_wsgi_app()
        server = make_server('0.0.0.0', 8080, app)
        server.serve_forever()

---

The Magic is in the CookieCutters
==

---

Take Your Power Adapter
==


