# Person object

Person is a 'real world' person. Magento doesn't have such concept in it, so 
this object is compiled from other objects (customer, order, quote, guest, subscriber).
Email address is used as a way to distinguish various persons from each other. 

Example, when someone registers on your website, or places an order for the first 
time, a new person record will be created, and the data known about this person 
will be stored in it. Months later, this same person can decide to do another 
purchase but now as an anonymous guest, using the same email address. For Magento 
internally, those are two seperate users. Copernica however, will link together 
those two entities based on the provided email address and merge them into one 
single object: a person. 

Information inside person object are the most recent information that was received
by MarketingSuite. When new data is synchronized with Marketing Suite changes to 
person object are automatically applied.

## Persons, guests and customers

One person can have one customer assigned. On other hand, one person can have
multiple guest objects assigned to it. It's cause of how guests are created.
For every guest order placed there is one guest object. Cause of that when
data is compiled into person object all guests will be assigned to person. They
are accessible via `guests` property.

## Personalization properties

| Property name   | Property type                                                                                        | Description                                                                                  |
|-----------------|------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| email           | _string_                                                                                             | Person's email address.                                                                      |
| firstname       | _string_                                                                                             | Person's first name.                                                                         |
| prefix          | _string_                                                                                             | Person's prefix.                                                                             |
| middlename      | _string_                                                                                             | Person's middle name.                                                                        |
| lastname        | _string_                                                                                             | Person's last name.                                                                          | 
| gender          | _string_                                                                                             | Person's gender. 'male' or 'female' are expected. When unknown FALSE value will be returned. |
| customer        | _[Customer](copernica-docs:MarketingSuite/magento-integration/object/customer)_                      | Customer object assigned to person.                                                        | 
| webstore        | _[Webstore](copernica-docs:MarketingSuite/magento-integration/object/webstore)_                      | Webstore object assigned to person.                                                        |
| orders          | _collection of [Order](copernica-docs:MarketingSuite/magento-integration/object/order)_              | Collection of all person's orders. Placed as customer or guest likewise.                     |
| quotes          | _collection of [Quote](copernica-docs:MarketingSuite/magento-integration/object/quote)_              | Collection of all person's quotes.                                                           |
| guests          | _collection of [Guest](copernica-docs:MarketingSuite/magento-integration/object/guest)_              | Collection of all guest objects assigned to person.                                        |
