# Property `platforms`

Each social block has a list of social medias, which are represented in the property 'platforms'.

Each platform in the platforms property has specific subproperties:

| Property | Value | Description                                                                                                                                                 |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| platform | _string_ | The name of the social platform                                                                               |
| image | _string_ | The image used for the social platform block. For now a default image is set for each social media                                                                         |
| [link](copernica-docs:ResponsiveEmail/json/property-link) | _object_ | Object with the link properties `url`, `title` and `params`.                                            |
| [share](copernica-docs:ResponsiveEmail/json/property-social-share) | _bool_ | Is this share or follow social platform                               |
| [width](copernica-docs:ResponsiveEmail/json/property-social-width) | _string_ | Optional width of the social block, default is auto (which is set to 32px)                                                    |
| [height](copernica-docs:ResponsiveEmail/json/property-social-height) | _string_ | Optional height of the social blcok, default is auto (which is set to 32px)              |                                                              |
 
## Example use

The following input JSON shows how to add a social platform to a document. This is
the basic usage, to include only one platform:

```javascript
{
    "from" : "info@example.com",
    "subject" : "Email with a single platform",
    "content" : {
        "blocks" : [ {
            "type" : "social",
            "label" : "Follow us on:",
            "platforms" : [
	       {
		    "platform": "facebook",
		    "image": "http://copernica.com/facebook.png",
		    "link": {
		      "url": "www.myfacebook.com"
		    },
		    "share": true,
		    "width": "auto",
		    "height": "auto"
	       }
	    ]
        } ]
    }
}
```
