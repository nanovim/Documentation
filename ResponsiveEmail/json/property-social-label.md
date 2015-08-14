# Property `label`

The `label` property is used inside [social blocks](copernica-docs:ResponsiveEmail/json/block-social)
and should hold the visible text for the social.

```javascript
{
    "from" : "info@example.com",
    "subject" : "Email with no platforms",
    "content" : {
        "blocks" : [ {
            "type" : "social",
            "label" : "Follow us on:",
            "platforms" : []
        } ]
    }
}
```

For more information and more examples, please check the documentation
of [social blocks](copernica-docs:ResponsiveEmail/json/block-social).
