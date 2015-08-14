# Property `share`

It is possible to make each social platform either to be used to share content or to follow account. You do this by providing the
[share](copernica-docs:ResponsiveEmail/json/property-social-share) subproperty. This can 
be a boolean true - for share and boolean false - for follow.
In case of share (share subproperty is true) - the provided [link](copernica-docs:ResponsiveEmail/json/property-link)
 property is used to point to the content you want to share. 
In case of follow (share subproperty is false) - the provided [link](copernica-docs:ResponsiveEmail/json/property-link)
 property is used to point to the account you want to follow.
The following example shows the input for an email with the two ways to process social platform - share and follow.

```javascript
{
    "from" : "info@example.com",
    "subject" : "Email with two platforms",
    "content" : {
        "blocks" : [ {
		"type": "social",
		"label": "Follow us on:",
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
