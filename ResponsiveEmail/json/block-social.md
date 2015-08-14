# Social block

The social block provides the ability to add social media buttons to your emails.
Aside from all the regular block properties there are some properties specific 
for socials, such as the [share](copernica-docs:ResponsiveEmail/json/property-src) 
property, which is used to mark if the social block is used to share or follow.

All available properties of this block type are mentioned in the table below.

## Social block properties

| Property | Value | Description                                                                                                                                                 |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| type | "social" | Property to identify the block as a social block.                                                                                                             |
| [label](copernica-docs:ResponsiveEmail/json/property-src) | _string_ | The label of the social block.                                                                                     |                   |
| [margin](copernica-docs:ResponsiveEmail/json/property-margin) | _mixed_ | Margins around the social block.                                                                            |
| [padding](copernica-docs:ResponsiveEmail/json/property-padding) | _mixed_ | Whitespace around the block, this whitespace will have a background 
| [background](copernica-docs:ResponsiveEmail/json/property-background) | _string_ | The background settings for the social block.                               |
| [align](copernica-docs:ResponsiveEmail/json/property-align) | _string_ | To which side should the social blcok be aligned? default is left.                                           |
| [width](copernica-docs:ResponsiveEmail/json/property-image-width) | _string_ | Optional width of the social block, default is 100%                                                    |
| [height](copernica-docs:ResponsiveEmail/json/property-image-height) | _string_ | Optional height of the social blcok, default is not set (image is automatically scaled)              |
| [platforms](copernica-docs:ResponsiveEmail/json/property-img) | _object_ | The separate social platforms, which are included in the social block                                            |                                                               |

Each platform in the platforms property has specific properties:

| Property | Value | Description                                                                                                                                                 |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [platform](copernica-docs:ResponsiveEmail/json/property-src) | _string_ | The name of the social platform block.                                                                                     |                   |
| [image](copernica-docs:ResponsiveEmail/json/property-margin) | _string_ | The image used for the social platform block.                                                                            |
| [link](copernica-docs:ResponsiveEmail/json/property-link) | _object_ | Object with the link properties `url`, `title` and `params`.                                            |
| [share](copernica-docs:ResponsiveEmail/json/property-background) | _bool_ | Is this share or follow social platform                               |
| [width](copernica-docs:ResponsiveEmail/json/property-image-width) | _string_ | Optional width of the social block, default is 100%                                                    |
| [height](copernica-docs:ResponsiveEmail/json/property-image-height) | _string_ | Optional height of the social blcok, default is not set (image is automatically scaled)              |                                                              |
 
## Example use

The following input JSON shows how to add an image to a document. This is
the basic usage, to only include an image with an extra "alt" tag:

```javascript
{
    "from" : "info@example.com",
    "subject" : "Email with a single image",
    "content" : {
        "blocks" : [ {
            "type" : "social",
            "label" : "Wil je niks missen? Volg ons dan op:",
            "platforms" : []
        } ]
    }
}
```

## Share or follow

It is possible to make each social platform either to share content or to follow account. You do this by providing the
[share](copernica-docs:ResponsiveEmail/json/property-link) property. This can 
be a boolean true - for share and boolean false - for follow.
In case of share (share property is true) - the provided [link](copernica-docs:ResponsiveEmail/json/property-link)
 property is used to point to the content you want to share. 
In case of follow (share property is false) - the provided [link](copernica-docs:ResponsiveEmail/json/property-link)
 property is used to point to the account you want to follow.
The following example shows the input for an email with the two ways to process social platform - share and follow.

```javascript
{
    "from" : "info@example.com",
    "subject" : "Email with two images",
    "content" : {
        "blocks" : [ {
		"type": "social",
		"label": "Wil je niks missen? Volg ons dan op:",
		"margin": "5",
		"padding": "5",
		"background": {
		  "color": "auto"
		},
		"align": "left",
		"width": "auto",
		"height": "auto",
		"platforms": [
		  {
		    "platform": "facebook",
		    "image": "http://copernica.com/facebook.png",
		    "link": {
		      "url": "www.myfacebook.com"
		    },
		    "share": true,
		    "width": "auto",
		    "height": "auto"
		  },
		  {
		    "platform": "twitter",
		    "image": "http://copernica.com/twitter.png",
		    "link": {
		      "url": "www.mytwitter.com"
		    },
		    "share": false,
		    "width": "auto",
		    "height": "auto"
		  }
		]
	      }
}
```
