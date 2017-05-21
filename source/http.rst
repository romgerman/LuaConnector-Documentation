HTTP requests library
=======================
.. highlight:: lua

LuaConnector has built-in http requests library

#############
Functions
#############

============
request [#1]
============

Prepares an http request::

    http.request(method, url, callback)

^^^^^^^^^^
Arguments
^^^^^^^^^^

* ``string`` method
    an http method. Available methods: GET, HEAD, POST, PUT, DELETE, OPTIONS

* ``string`` url
    request url

* ``function`` callback
    callback function gets called when a response has been acquired. Has two arguments:

    * ``httpRequest``
        current http request object

    * ``httpResponse``
        response from current http request

^^^^^^^^^^
Returns
^^^^^^^^^^

* ``httpRequest`` http request object

============
request [#2]
============

Prepares an http request::

    http.request(options, callback)

^^^^^^^^^^
Arguments
^^^^^^^^^^

* ``table`` options
    table of request options

    * ``string`` method
        an http method. Available methods: GET, HEAD, POST, PUT, DELETE, OPTIONS

    * ``string`` url
        request url

    * ``table`` headers
        request headers

    * ``string`` content
        applies only to POST and PUT requests

* ``string`` url
    request url

* ``function`` callback
    callback function gets called when a response has been acquired. Has two arguments:

    * ``httpRequest``
        current http request object

    * ``httpResponse``
        response from current http request

^^^^^^^^^^
Returns
^^^^^^^^^^

* ``httpRequest`` http request object

#############
Objects
#############

============
httpRequest
============

Represents a HTTP request

^^^^^^^^^^
send
^^^^^^^^^^

Sends the http request

=============
httpResponse
=============

Has three fields:

* ``string`` content

* ``number`` status

* ``table`` headers

##########
Examples
##########

.. code-block:: lua

    local request = http.request("GET", "https://jsonplaceholder.typicode.com/posts/1", function(req, res)
        print(res.content)
    end)

    request.send()

.. code-block:: lua

    local options = {
        method = "POST",
        url = "https://discordapp.com/api/auth/login",
        content = json.serialize({email = "", password = ""}),
        headers = {
            ["Content-Type"] = "application/json"
        }
    }

    http.request(options, function(req, res)
        print(res.content)
    end).send()
