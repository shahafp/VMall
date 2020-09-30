========================
REST API Documentation
========================

Mall API
~~~~~~~~~~~~~~~

GET
+++++

Returns a list of all current services tracked by Stashboard

.. code-block:: bash

   GET /malls

.. code-block:: js

 [
  {
    "id": 11,
    "mallName": "The Mall",
    "users": [
      {
        "id": 1,
        "fullName": "Meidan",
        "userName": "Meidan",
        "password": "Meidan",
        "role": "Owner",
        "personType": "Citizen"
      }
    ],
    "stores": [
      {
        "id": 9,
        "storeName": "shufersal",
        "owners": [
          {
            "id": 1,
            "fullName": "Meidan",
            "userName": "Meidan",
            "password": "Meidan",
            "role": "Owner",
            "personType": "Citizen"
          }
        ],
        "catalogList": [
          {
            "id": 6,
            "catalogName": "Top&Shirts",
            "itemList": [
              {
                "id": 3,
                "name": "Shirt",
                "category": "Cloth",
                "price": 15.5
              }
            ],
            "categoryList": [
              "Cloth"
            ]
          },
          "discountMap":
          {
            "soldier": 0.15,
            "pensioner": 0.15,
            "cripple": 0.15
           }
       ]



GET 
++++++

Get a specific store from the mall

==============   ===============
Variable            Description
==============   ===============
mallName         Name of the mall 
==============   ===============

.. code-block:: text

   GET /getStore/{mallName} /getStore/The%20mall

.. code-block:: js

        [
    {
        "id": 9,
        "storeName": "shufersal",
        "owners": [
            {
                "id": 1,
                "fullName": "Meidan",
                "userName": "Meidan",
                "password": "Meidan",
                "role": "Owner",
                "personType": "Citizen"
            },
            {
                "id": 2,
                "fullName": "bar",
                "userName": "bar",
                "password": "bar",
                "role": "Customer",
                "personType": "Soldier"
            }
        ],
        "catalogList": [
            {
                "id": 6,
                "catalogName": "Top&Shirts",
                "itemList": [
                    {
                        "id": 3,
                        "name": "Shirt",
                        "category": "Cloth",
                        "price": 15.5
                    }
                ],
                "categoryList": [
                    "Cloth"
                ]
            },
            {
                "id": 7,
                "catalogName": "Kids",
                "itemList": [
                    {
                        "id": 5,
                        "name": "Lego",
                        "category": "Toys",
                        "price": 15.5
                    }
                ],
                "categoryList": [
                    "Toys"
                ]
            },
            {
                "id": 8,
                "catalogName": "Food",
                "itemList": [
                    {
                        "id": 4,
                        "name": "Burger",
                        "category": "Food",
                        "price": 15.5
                    }
                ],
                "categoryList": [
                    "Food"
                ]
            }
        ],
        "discountMap": {
            "soldier": 0.15,
            "pensioner": 0.15,
            "cripple": 0.15
        }
    },
    {
        "id": 10,
        "storeName": "Corona",
        "owners": [
            {
                "id": 1,
                "fullName": "Meidan",
                "userName": "Meidan",
                "password": "Meidan",
                "role": "Owner",
                "personType": "Citizen"
            },
            {
                "id": 2,
                "fullName": "bar",
                "userName": "bar",
                "password": "bar",
                "role": "Customer",
                "personType": "Soldier"
            }
        ],
        "catalogList": [
            {
                "id": 6,
                "catalogName": "Top&Shirts",
                "itemList": [
                    {
                        "id": 3,
                        "name": "Shirt",
                        "category": "Cloth",
                        "price": 15.5
                    }
                ],
                "categoryList": [
                    "Cloth"
                ]
            },
            {
                "id": 7,
                "catalogName": "Kids",
                "itemList": [
                    {
                        "id": 5,
                        "name": "Lego",
                        "category": "Toys",
                        "price": 15.5
                    }
                ],
                "categoryList": [
                    "Toys"
                ]
            },
            {
                "id": 8,
                "catalogName": "Food",
                "itemList": [
                    {
                        "id": 4,
                        "name": "Burger",
                        "category": "Food",
                        "price": 15.5
                    }
                ],
                "categoryList": [
                    "Food"
                ]
            }
        ],
        "discountMap": {}
    }
]
   

POST
++++
Register as a user before call any other function

.. code-block:: bash

    POST /register/{mallName} -> /register/The%20mall

.. code-block:: js

        {
    "id": 11,
    "mallName": "The Mall",
    "users": [
        {
            "id": 1,
            "fullName": "Meidan",
            "userName": "Meidan",
            "password": "Meidan",
            "role": "Owner",
            "personType": "Citizen"
        },
        {
            "id": 2,
            "fullName": "bar",
            "userName": "bar",
            "password": "bar",
            "role": "Customer",
            "personType": "Soldier"
        },
        {
            "id": 12,
            "fullName": "Shahaf Pariente",
            "userName": "Shahaf",
            "password": "12346578",
            "role": "Owner",
            "personType": "Soldier"
        }
    ],
    "stores": [
        {
            "id": 9,
            "storeName": "shufersal",
            "owners": [
                {
                    "id": 1,
                    "fullName": "Meidan",
                    "userName": "Meidan",
                    "password": "Meidan",
                    "role": "Owner",
                    "personType": "Citizen"
                },
                {
                    "id": 2,
                    "fullName": "bar",
                    "userName": "bar",
                    "password": "bar",
                    "role": "Customer",
                    "personType": "Soldier"
                }
            ],
            "catalogList": [
                {
                    "id": 6,
                    "catalogName": "Top&Shirts",
                    "itemList": [
                        {
                            "id": 3,
                            "name": "Shirt",
                            "category": "Cloth",
                            "price": 15.5
                        }
                    ],
                    "categoryList": [
                        "Cloth"
                    ]
                },
                {
                    "id": 7,
                    "catalogName": "Kids",
                    "itemList": [
                        {
                            "id": 5,
                            "name": "Lego",
                            "category": "Toys",
                            "price": 15.5
                        }
                    ],
                    "categoryList": [
                        "Toys"
                    ]
                },
                {
                    "id": 8,
                    "catalogName": "Food",
                    "itemList": [
                        {
                            "id": 4,
                            "name": "Burger",
                            "category": "Food",
                            "price": 15.5
                        }
                    ],
                    "categoryList": [
                        "Food"
                    ]
                }
            ],
            "discountMap": {
                "soldier": 0.15,
                "pensioner": 0.15,
                "cripple": 0.15
            }
        },
        {
            "id": 10,
            "storeName": "Corona",
            "owners": [
                {
                    "id": 1,
                    "fullName": "Meidan",
                    "userName": "Meidan",
                    "password": "Meidan",
                    "role": "Owner",
                    "personType": "Citizen"
                },
                {
                    "id": 2,
                    "fullName": "bar",
                    "userName": "bar",
                    "password": "bar",
                    "role": "Customer",
                    "personType": "Soldier"
                }
            ],
            "catalogList": [
                {
                    "id": 6,
                    "catalogName": "Top&Shirts",
                    "itemList": [
                        {
                            "id": 3,
                            "name": "Shirt",
                            "category": "Cloth",
                            "price": 15.5
                        }
                    ],
                    "categoryList": [
                        "Cloth"
                    ]
                },
                {
                    "id": 7,
                    "catalogName": "Kids",
                    "itemList": [
                        {
                            "id": 5,
                            "name": "Lego",
                            "category": "Toys",
                            "price": 15.5
                        }
                    ],
                    "categoryList": [
                        "Toys"
                    ]
                },
                {
                    "id": 8,
                    "catalogName": "Food",
                    "itemList": [
                        {
                            "id": 4,
                            "name": "Burger",
                            "category": "Food",
                            "price": 15.5
                        }
                    ],
                    "categoryList": [
                        "Food"
                    ]
                }
            ],
            "discountMap": {}
        }
    ]
}

POST
+++++

Buy items from a specific store in the mall.

==============   ===============
Param            Description
==============   ===============
userName         The person userName  
password         Password of the user 
==============   ===============

==============   ===============  ==============    
Body             value            Description
==============   ===============  ==============
params           catalog          Name of the catalog
                 items            List of the item names
                 paymentMethod    The payment method name
==============   ===============  ==============

.. code-block:: text
  
    POST /buy/{mallName}/{storeName} /buy/The%20mall/shufersal
   
Body
.. code-block:: js
{
    "catalog":"Food",
    "items": [
        "Shirt",
        "Burger"
    ],
    "paymentMethod":"creditcard"
}

Response
.. code-block:: js

        Could not find some of your items: [Shirt]



GET
+++++++

Call for a help if you are person with disabillities
==============   ===============
Param            Description
==============   ===============
userName         The person userName  
password         Password of the user 
==============   ===============

.. code-block:: text

    GET /getHelp/{mallName} /getHelp/The%20mall?userName=bar&password=bar

.. code-block:: js

        "Help is on the way Sir!"

Service List
-------------

The Service List resource represents all a collection of related services

==============   ===============
Property         Description
==============   ===============
id	         The unique identifier by which to identify the service list
name             The name of the service list, defined by the user
description      The description of the service list
url	         The URL of the specific service list resource
==============   ===============

List Resource
~~~~~~~~~~~~~~~

.. code-block:: text

    /admin/api/v1/service-lists

GET
+++++

Returns a list of all current service lists tracked by Stashboard

.. code-block:: bash

   GET /admin/api/v1/service-lists HTTP/1.1

.. code-block:: js

        {
            "lists": [
                {
                    "name": "Example Foo",
                    "id": "example-foo",
                    "description": "An explanation of this service"
                    "url": "/api/v1/service-lists/example-foo",
                },
                {
                    "name": "Example Bar",
                    "id": "example-bar",
                    "description": "An explanation of this service"
                    "url": "/api/v1/service-lists/example-bar",
                }
            ]
        }

POST 
++++++

Creates a new service list and returns the new service list object.

==============   ===============
Param            Description
==============   ===============
name             Name of the service list
description      Description of service list
==============   ===============

.. code-block:: text

   POST /admin/api/v1/service-lists HTTP/1.1 name=New%20Service&description=A%20great%20service

.. code-block:: js

        {
            "name": "New List",
            "id": "new-list",
            "description": "A great service"
            "url": "/api/v1/service-list/new-list",
        }


Instance Resource
~~~~~~~~~~~~~~~~~~

.. code-block:: text

    /admin/api/v1/service-lists/{service-list}

The Service Instance resources represents an individual service list

GET
++++

.. code-block:: bash

    GET /admin/api/v1/service-lists/{service} HTTP/1.1

.. code-block:: js

        {
            "name": "Example List",
            "id": "example-list",
            "description": "An explanation of what this list represents"
            "url": "/api/v1/service-lists/example-list",
        }

POST
+++++

Updates a service list's description and returns the updated service list. All the listed parameters are optional.

==============   ===============
Param            Description
==============   ===============
name             Name of the service list
description      Description of service list
==============   ===============

.. code-block:: text
  
    POST /admin/api/v1/service-lists/{service-list} description=System%20is%20now%20operational

.. code-block:: js

        {
            "name": "Example List",
            "id": "example-list",
            "description": "System is now operational",
            "url": "/api/v1/service-lists/example-list",
        }


DELETE
+++++++

Deletes a service list and returns the deleted service object

.. code-block:: text

    DELETE /admin/api/v1/service-lists/{service-list} HTTP/1.1

.. code-block:: js

        {
            "name": "Example List",
            "id": "example-list",
            "description": "System is now operational",
            "url": "/api/v1/service-lists/example-list",
        }

Events
-----------

The Events List resource represents all event associated with a given service


==============   ===============
Property         Description
==============   ===============
sid	         The unique identifier by which to identify the event
message	         The message associated with this event
timestamp	 The time at which this event occurred, given in RFC 1132 format.
url	         The URL of the specific event resource
status	         The status of this event, as described by the Statuses resource
==============   ===============


List Resource
~~~~~~~~~~~~~~~~~~~~

.. code-block:: text

    /admin/api/v1/services/{service}/events

GET
++++

Returns all events associated with a given service in reverse chronological order.

.. code-block:: text

    GET /admin/api/v1/services/{service}/events HTTP/1.1

.. code-block:: js

        {
            "events": [
                {
                    "timestamp": "Mon, 28 Jun 2010 22:17:06 GMT",
                    "message": "Problem fixed", 
                    "sid": "ahJpc215d2Vic2VydmljZWRvd25yCwsSBUV2ZW50GBAM",
                    "url": "/api/v1/services/example-service/events/ahJpc215d2Vic2VydmljZWRvd2",
                    "status": {
                        "id": "down",
                        "name": "Down",
                        "description": "An explanation of what this status represents",
                        "level": "ERROR",
                        "image": "/images/status/cross-circle.png",
                        "url": "/api/v1/statuses/down",
                    },
                }, 
                {
                    "timestamp": "Mon, 28 Jun 2010 22:18:06 GMT",
                    "message": "Might be up", 
                    "sid": "ahJpc215d2Vic2VydmljZWRvd25yCwsSBUV2ZW50GA8M",
                    "url": "/api/v1/services/example-service/events/ahJpc215d2Vic..."
                    "status": {
                        "id": "down",
                        "name": "Down",
                        "description": "An explanation of what this status represents",
                        "level": "ERROR",
                        "image": "/images/status/cross-circle.png",
                        "url": "/api/v1/statuses/down",
                    },
                }
            ]
        }

The Events List resource also supports filtering events via dates. To filter events, place on of the following options into the query string for a GET request

While the format of these parameters is very flexible, we suggested either the RFC 2822 or RFC 1123 format due to their support for encoding timezone information.

Events List URL Filtering Options

======= ============
Option	Description
======= ============
start	Only show events which started after this date, inclusive.
end     Only show events which started before date, inclusive.
======= ============

.. code-block:: text

    GET /admin/api/v1/services/{service}/events?start=2010-06-10 HTTP/1.1

would return all events starting after June 6, 2010.

Similarly, both "start" and "end" can be used to create date ranges

.. code-block:: text

    GET /admin/api/v1/services/{service}/events?end=2010-06-17&start=2010-06-01 HTTP/1.1

would return all events between June 6, 2010 and June 17, 2010



POST
+++++

Creates a new event for the given service and returns the newly created event object. All arguments are required.

========  ==============
Param	  Description
========  ==============
status	  The system status for the event. This must be a valid system status identifier found in the Statuses List resource
message	  The message for the event
========  ==============

.. code-block:: text

    POST /admin/api/v1/services/{service}/events HTTP/1.1 status=AVAILABLE&message=System%20is%20now%20operational

.. code-block:: js

        {
            "timestamp": "Mon, 28 Jun 2010 22:18:06 GMT"
            "message": "Might be up", 
            "sid": "ahJpc215d2Vic2VydmljZWRvd25yCwsSBUV2ZW50GA8M",
            "url": "/api/v1/services/example-service/events/ahJpc215d2Vic2VydmljZWRvd25yCwsSBUV2ZW50GA8M",
            "status": {
                "id": "down",
                "name": "Down",
                "description": "An explanation of what this status represents",
                "level": "ERROR",
                "image": "/images/status/cross-circle.png",
                "url": "/api/v1/statuses/down",
            },
        }

Current Event
~~~~~~~~~~~~~~~~~

The Current Service Event resource simply returns the current event for a given service.

.. code-block:: text

    /admin/api/v1/services/{service}/events/current

GET
++++

Returns the current event for a given service.

.. code-block:: text

    GET /admin/api/v1/services/{service}/events/current HTTP/1.1

.. code-block:: js

        {
            "timestamp": "Mon, 28 Jun 2010 22:17:06 GMT",
            "message": "Might be up", 
            "sid": "ahJpc215d2Vic2VydmljZWRvd25yCwsSBUV2ZW50GA8M",
            "url": "/api/v1/services/example-service/events/ahJpc215d2Vic2VydmljZWRvd25yCwsSBUV2ZW50GA8M",
            "status": {
                "id": "down",
                "name": "Down",
                "description": "An explanation of what this status represents",
                "level": "ERROR",
                "image": "/images/status/cross-circle.png",
                "url": "/api/v1/statuses/down",
            },
        }

Instance Resource
~~~~~~~~~~~~~~~~~~~~

The Event Instance resource represents an individual event for a given service.

.. code-block:: text
 
    /admin/api/v1/services/{service}/events/{sid}

GET
++++

Returns a service event with the given event sid. The event's status object is also returned as well.

.. code-block:: text

    GET /admin/api/v1/services/{service}/events/{sid} HTTP/1.1

.. code-block:: js

        {
            "timestamp": "Mon, 28 Jun 2010 22:17:06 GMT",
            "message": "Might be up", 
            "sid": "ahJpc215d2Vic2VydmljZWRvd25yCwsSBUV2ZW50GA8M",
            "url": "/api/v1/services/example-service/events/ahJpc215d2Vic2VydmljZWRvd25yCwsSBUV2ZW50GA8M",
            "status": {
                "id": "down",
                "name": "Down",
                "description": "An explanation of what this status represents",
                "level": "ERROR",
                "image": "/images/status/cross-circle.png",
                "url": "/api/v1/statuses/down",
            }
        }


DELETE
++++++++

Deletes the given event and returns the deleted event

.. code-block:: text

    DELETE /admin/api/v1/services/{service}/events/{sid} HTTP/1.1

.. code-block:: js

        {
            "timestamp": "Mon, 28 Jun 2010 22:17:06 GMT",
            "message": "Might be up", 
            "sid": "ahJpc215d2Vic2VydmljZWRvd25yCwsSBUV2ZW50GA8M",
            "url": "/api/v1/services/example-service/events/ahJpc215d2Vic2VydmljZWRvd25yCwsSBUV2ZW50GA8M",
            "status": {
                "id": "down",
                "name": "Down",
                "description": "An explanation of what this status represents",
                "level": "ERROR",
                "image": "/images/status/cross-circle.png",
                "url": "/statuses/down",
            },    
        }

Statuses
-----------
The Status resource represents a possible status for a service.

==============   ===============
Property         Description
==============   ===============
id	         The unique identifier by which to identify the status
name	         The name of the status, defined by the user
description	 The description of the status
url	         The URL of the specific status resource
level	         The level of this status. Can be any value listed in the Levels List resource
image	         The URL of the image for this status
==============   ===============

List Resource
~~~~~~~~~~~~~~~~

.. code-block:: text

    /admin/api/v1/statuses


The Status List resource represents all possible systems statuses.


GET
+++++

Returns all service statuses

.. code-block:: text

    GET /admin/api/v1/statuses HTTP/1.1

.. code-block:: js

        {
            "statuses": [
                {
                    "name": "Available",
                    "id": "available",
                    "description": "An explanation of what this status represents",
                    "level": "NORMAL",
                    "image": "/images/status/tick-circle.png",
                    "url": "api/v1/statuses/up",
                },
                {
                    "name": "Down",
                    "id": "down",
                    "description": "An explanation of what this status represents",
                    "level": "ERROR",
                    "image": "/images/status/cross-circle.png",
                    "url": "api/v1/statuses/down",
                },
            ]
        }

POST
++++++

Creates a new status and returns this newly created status. All parameters are required.

============  ==============
Param	      Description
============  ==============
name	      The name of the status
description   The description of the status
level	      The level of the status. lues listed in the rce
image	      The filename of the image, with no extension. See the status-images resource
============  ==============

.. code-block:: text

    POST /admin/api/v1/statuses HTTP/1.1 name=Down&description=A%20new%20status&severity=1000&image=cross-circle.png

.. code-block:: js

        {
            "name": "Down",
            "id": "down"
            "description": "A new status",
            "level": "ERROR",
            "image": "cross-circle",
            "url": "/api/v1/statuses/down",
        }

Instance Resource
~~~~~~~~~~~~~~~~~~~~~

The Status Instance resource represents a single service status

.. code-block:: text

    /admin/api/v1/statuses/{name}


GET
+++++

Returns a status object

.. code-block:: text

   GET /admin/api/v1/services HTTP/1.1

.. code-block:: js

        {
            "name": "Down",
            "id": "down",
            "description": "A new status",
            "level": "ERROR",
            "image": "/images/status/cross-circle.png",
            "url": "/api/v1/statuses/down",
        }

POST
++++++

Update the given status. All the following parameters are optional.

============  ==============
Param	      Description
============  ==============
name	      The name of the status
description   The description of the status
level	      The level of the status. lues listed in the rce
image	      The filename of the image, with no extension. See the status-images resource
============  ==============

.. code-block:: text

    POST /admin/api/v1/statuses HTTP/1.1 description=A%20new%20status&severity=1010&image=cross-circle.png

.. code-block:: js

        {
            "name": "Down",
            "id": "down",
            "description": "A new status",
            "level": "ERROR",
            "image": "/images/status/cross-circle.png",
            "url": "/api/v1/statuses/down",
        }

DELETE
+++++++++

Delete the given status and return the deleted status


.. code-block:: text

    DELETE /admin/api/v1/statuses/{name}

.. code-block:: js

        {
            "name": "Down",
            "id": "down",
            "description": "A new status",
            "level": "ERROR",
            "image": "/images/status/cross-circle.png",
            "url": "/api/v1/statuses/down",
        }

Status Levels
----------------
The Status Levels resource is a read-only resource which lists the possible levels for a status.

List Resource
~~~~~~~~~~~~~~~~~

.. code-block:: text

    /admin/api/v1/levels

GET
+++++
Returns a list of possible status levels in increasing severity

.. code-block:: text

    GET /admin/api/v1/levels

.. code-block:: js

        {
            "levels": [
                "NORMAL", 
                "WARNING", 
                "ERROR", 
                "CRITICAL",
            ]
        }


Status Images
----------------
The Status Images resource is a read-only resource which lists the icons available to use for statuses

List Resource
~~~~~~~~~~~~~~~

.. code-block:: text

    /admin/api/v1/status-images

GET
++++++

Returns a list of status images.

.. code-block:: text

    GET /admin/api/v1/status-images

.. code-block:: js

        {
            "images": [
                {
                    "name": "sample-image",
                    "url": "/status-images/sample-image.png",
                },
                {
                    "name": "sample-image",
                    "url": "/status-images/sample-image.png",
                },
            ]
        }
