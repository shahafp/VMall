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


==============   ===============  ==============    
Body             value            Description
==============   ===============  ==============
params           Person           The person data
==============   ===============  ==============

.. code-block:: bash

    POST /register/{mallName} -> /register/The%20mall

.. code-block:: js
   {
       "fullName":"Shahaf Pariente",
       "userName":"Shahaf",
       "password":"12346578",
       "role":"Owner",
       "personType":"Soldier"
   }

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
params           catalog,          Name of the catalog,
                 items,            List of the item names,
                 paymentMethod,    The payment method name,
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

Store API
~~~~~~~~~~~~~~~


GET
+++++

Returns a list of all stores

.. code-block:: bash

   GET /stores

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

GET 
++++++

Get a specific store by id

.. code-block:: text

   GET /storeById/{id} /storeById/9 

.. code-block:: js

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
   }


GET
++++
Get store by name
.. code-block:: bash

    GET /storeByName/{name} /storeByName/shufersal

.. code-block:: js

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
   }

GET
+++++

Get all the catalogs

==============   ===============
Param            Description
==============   ===============
storeName        Name of the store
==============   ===============

.. code-block:: text
  
    GET /store/catalogs /store/catalogs?storeName=shufersal

.. code-block:: js

           [
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
   ]


GET
+++++++

Get catalog by its name

==============   ===============
Param            Description
==============   ===============
storeName        Name of the store
catalogName      Name of the catalog 
==============   ===============

.. code-block:: text

    DELETE /store/catalog /store/catalog?storeName=shufersal&catalogName=Kids

.. code-block:: js

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
   }


GET
++++

Returns all the categories.

==============   ===============
Param            Description
==============   ===============
storeName        Name of the store
==============   ===============

.. code-block:: text

    GET /store/categories /store/categories?storeName=shufersal

.. code-block:: js

           [
       "Cloth",
       "Toys",
       "Food"
   ]


GET
+++++

Get all the items.

==============   ===============
Param            Description
==============   ===============
storeName        Name of the store
==============   ===============

.. code-block:: text

    GET /store/items /store/items?storeName=shufersal

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


POST
++++

Add new store.

==============   ===============
Body             Description
==============   ===============
Store            store details
==============   ===============

.. code-block:: text

    POST /addStore
.. code-block:: js

   {
       "storeName": "blayyh",
       "owners": [
           {
               "fullName": "test2",
               "userName": "test3",
               "password": "Meidan",
               "role": "Owner",
               "personType": "Citizen"
           },
           {
               "fullName": "test",
               "userName": "teest",
               "password": "bar",
               "role": "Customer",
               "personType": "Soldier"
           }
       ],
       "catalogList": [
           {
               "catalogName": "Top&Shirts",
               "itemList": [
                   {
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
               "catalogName": "Kids",
               "itemList": [
                   {
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
               "catalogName": "TV",
               "itemList": [
                   {
                       "name": "LGLCD",
                       "category": "LCD",
                       "price": 15.5
                   }
               ],
               "categoryList": [
                   "Food"
               ]
           }
       ]
   }

.. code-block:: js

           {
       "id": 34,
       "storeName": "blayyh",
       "owners": [
           {
               "id": 12,
               "fullName": "test2",
               "userName": "test3",
               "password": "Meidan",
               "role": "Owner",
               "personType": "Citizen"
           },
           {
               "id": 13,
               "fullName": "test",
               "userName": "teest",
               "password": "bar",
               "role": "Customer",
               "personType": "Soldier"
           }
       ],
       "catalogList": [
           {
               "id": 31,
               "catalogName": "Top&Shirts",
               "itemList": [
                   {
                       "id": 28,
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
               "id": 32,
               "catalogName": "Kids",
               "itemList": [
                   {
                       "id": 29,
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
               "id": 33,
               "catalogName": "TV",
               "itemList": [
                   {
                       "id": 30,
                       "name": "LGLCD",
                       "category": "LCD",
                       "price": 15.5
                   }
               ],
               "categoryList": [
                   "Food"
               ]
           }
       ]
   }


POST
++++

Add list of stores.

==============   ===============
Body             Description
==============   ===============
List of stores   List of store details
==============   ===============

.. code-block:: text

    POST /addStores
.. code-block:: js

   [
         {
          "storeName": "blayyh",
          "owners": [
              {
                  "fullName": "test2",
                  "userName": "test3",
                  "password": "Meidan",
                  "role": "Owner",
                  "personType": "Citizen"
              },
              {
                  "fullName": "test",
                  "userName": "teest",
                  "password": "bar",
                  "role": "Customer",
                  "personType": "Soldier"
              }
          ],
          "catalogList": [
              {
                  "catalogName": "Top&Shirts",
                  "itemList": [
                      {
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
                  "catalogName": "Kids",
                  "itemList": [
                      {
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
                  "catalogName": "TV",
                  "itemList": [
                      {
                          "name": "LGLCD",
                          "category": "LCD",
                          "price": 15.5
                      }
                  ],
                  "categoryList": [
                      "Food"
                  ]
              }
          ]
      }
   ]

.. code-block:: js

           [
                  {
       "id": 34,
       "storeName": "blayyh",
       "owners": [
           {
               "id": 12,
               "fullName": "test2",
               "userName": "test3",
               "password": "Meidan",
               "role": "Owner",
               "personType": "Citizen"
           },
           {
               "id": 13,
               "fullName": "test",
               "userName": "teest",
               "password": "bar",
               "role": "Customer",
               "personType": "Soldier"
           }
       ],
       "catalogList": [
           {
               "id": 31,
               "catalogName": "Top&Shirts",
               "itemList": [
                   {
                       "id": 28,
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
               "id": 32,
               "catalogName": "Kids",
               "itemList": [
                   {
                       "id": 29,
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
               "id": 33,
               "catalogName": "TV",
               "itemList": [
                   {
                       "id": 30,
                       "name": "LGLCD",
                       "category": "LCD",
                       "price": 15.5
                   }
               ],
               "categoryList": [
                   "Food"
               ]
           }
       ]
   }
           ]


PUT
++++++++

Updates the store

==============   ===============
Param            Description
==============   ===============
userName         the username of the owner
==============   ===============

==============   ===============
Body            Description
==============   ===============
store            store deatils
==============   ===============

.. code-block:: text

    PUT /store/update /store/update?userName=test3

.. code-block:: js
   {
       "id":10,
       "storeName": "updated",
       "owners": [
           {
               "fullName": "test2",
               "userName": "test3",
               "password": "Meidan",
               "role": "Owner",
               "personType": "Citizen"
           },
           {
               "fullName": "test",
               "userName": "teest",
               "password": "bar",
               "role": "Customer",
               "personType": "Soldier"
           }
       ],
       "catalogList": [
           {
               "catalogName": "Top&Shirts",
               "itemList": [
                   {
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
               "catalogName": "Kids",
               "itemList": [
                   {
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
               "catalogName": "TV",
               "itemList": [
                   {
                       "name": "LGLCD",
                       "category": "LCD",
                       "price": 15.5
                   }
               ],
               "categoryList": [
                   "Food"
               ]
           }
       ]
   }

.. code-block:: js

           {
       "id": 10,
       "storeName": "updated",
       "owners": [
           {
               "id": null,
               "fullName": "test2",
               "userName": "test3",
               "password": "Meidan",
               "role": "Owner",
               "personType": "Citizen"
           },
           {
               "id": null,
               "fullName": "test",
               "userName": "teest",
               "password": "bar",
               "role": "Customer",
               "personType": "Soldier"
           }
       ],
       "catalogList": [
           {
               "id": null,
               "catalogName": "Top&Shirts",
               "itemList": [
                   {
                       "id": null,
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
               "id": null,
               "catalogName": "Kids",
               "itemList": [
                   {
                       "id": null,
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
               "id": null,
               "catalogName": "TV",
               "itemList": [
                   {
                       "id": null,
                       "name": "LGLCD",
                       "category": "LCD",
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


POST
+++++

Add new item the the store with given store id

==============   ===============
Param            Description
==============   ===============
userName         the username of the owner
catalogName      The name of the catalog the item is added to
==============   ===============

.. code-block:: text

    POST /store/addItem/{id} /store/addItem/10?userName=Meidan&catalogName=Top%26Shirts

.. code-block:: js

    {

           "name": "Shirt",
           "category": "Cloth",
           "price": 15.5
   }

.. code-block:: js

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
                },
                {
                    "id": 13,
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

POST
++++++

Deletes an item by ID

==============   ===============
Param            Description
==============   ===============
userName         the username of the owner
catalogName      The name of the catalog the item is added to
==============   ===============

.. code-block:: text

    POST /store/deleteItem/{id} /store/deleteItem/10?userName=Meidan&catalogName=Top%26Shirts
.. code-block:: js

    {
           "id":13,
           "name": "Shirt",
           "category": "Cloth",
           "price": 15.5
   }

.. code-block:: js

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
                   },
                   {
                       "id": 13,
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
        

POST
+++++

Update an item by ID


==============   ===============
Param            Description
==============   ===============
userName         the username of the owner
catalogName      The name of the catalog the item is added to
==============   ===============

.. code-block:: text

    POST /store/updateItem/{id} /store/updateItem/10?userName=Meidan&catalogName=Top%26Shirts
.. code-block:: js

    {
           "id":13,
           "name": "Shirt",
           "category": "Cloth",
           "price": 15.5
   }

.. code-block:: js

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
                   },
                   {
                       "id": 13,
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

POST
++++++

Add catalog to the store with the store id as variable

==============   ===============
Param            Description
==============   ===============
userName         the username of the owner
==============   ===============

==============   ===============
Body            Description
==============   ===============
Catalog          catalog details
==============   ===============

.. code-block:: text

    POST /store/addCatalog/{id} 
    
.. code-block:: js
   {
            "catalogName": "newCatalog",
            "itemList": [
                {
                    "name": "Shirt",
                    "category": "Cloth",
                    "price": 15.5
                }
            ]
            
        }

.. code-block:: js

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
                   },
                   {
                       "id": 13,
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
           },
           {
               "id":9,
               "catalogName": "newCatalog",
               "itemList": [
                   {
                       "name": "Shirt",
                       "category": "Cloth",
                       "price": 15.5
                   }
               ],
               "categoryList": [
                   "Cloth"
               ]

           }
       ],
       "discountMap": {}
   }
        

POST
+++++++++

Delete catalog from store by store id


.. code-block:: text

    POST /store/deleteCatalog/{id} 
    
.. code-block:: js
 
{
    "id":9,
            "catalogName": "newCatalog",
            "itemList": [
                {
                    "name": "Shirt",
                    "category": "Cloth",
                    "price": 15.5
                }
            ]
            
        }
.. code-block:: js

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
                   },
                   {
                       "id": 13,
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


DELETE
+++++
Delete the store

==============   ===============
Param            Description
==============   ===============
userName         the username of the owner
==============   ===============

.. code-block:: text

    DELETE /store/delete/{id} /store/delete/10?userName=Meidan

.. code-block:: js

        "Deleted Store id: 10"



Person API
~~~~~~~~~~~~~~~

GET
++++++

Returns all persons

.. code-block:: text

    GET /persons

.. code-block:: js

           [
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
   ]


GET
++++++

Returns person by ID

.. code-block:: text

    GET /getPerson/{id} /getPerson/1

.. code-block:: js

   {
       "id": 1,
       "fullName": "Meidan",
       "userName": "Meidan",
       "password": "Meidan",
       "role": "Owner",
       "personType": "Citizen"
   }


GET
++++++

==============   ===============
Param            Description
==============   ===============
name              the name of the user
==============   ===============

Returns person by userName

.. code-block:: text

    GET /getPerson /getPerson?name=Meidan

.. code-block:: js

   {
       "id": 1,
       "fullName": "Meidan",
       "userName": "Meidan",
       "password": "Meidan",
       "role": "Owner",
       "personType": "Citizen"
   }

POST
++++++

Add new person to DB

==============   ===============
Body              Description
==============   ===============
person         person details
==============   ===============


.. code-block:: text

    POST /addPerson
    
.. code-block:: js

   {
       "fullName":"Shahaf Pariente",
       "userName":"SP",
       "password":"12346578",
       "role":"Owner",
       "personType":"Soldier"
   }

.. code-block:: js

   [
       {
           "id": 14,
           "fullName": "Shahaf Pariente",
           "userName": "SP",
           "password": "12346578",
           "role": "Owner",
           "personType": "Soldier"
       }
   ]

POST
++++++

Add list of persons to the db

==============   ===============
Body              Description
==============   ===============
person         person details
==============   ===============

Returns person by userName

.. code-block:: text

    POST /addPersons
    
.. code-block:: js
   [
      {
          "fullName":"Shahaf Pariente",
          "userName":"SP",
          "password":"12346578",
          "role":"Owner",
          "personType":"Soldier"
      }
   ]

.. code-block:: js

   [
       {
           "id": 14,
           "fullName": "Shahaf Pariente",
           "userName": "SP",
           "password": "12346578",
           "role": "Owner",
           "personType": "Soldier"
       }
   ]

PUT
++++++

Update a person details

==============   ===============
Body              Description
==============   ===============
person           person details
==============   ===============


.. code-block:: text

    POST /addPersons
    
.. code-block:: js

   {
       "id": 1,
       "fullName": "updateName",
       "userName": "Meidan",
       "password": "Meidan",
       "role": "Owner",
       "personType": "Citizen"
   }

.. code-block:: js

   {
       "id": 1,
       "fullName": "updateName",
       "userName": "Meidan",
       "password": "Meidan",
       "role": "Owner",
       "personType": "Citizen"
   }




