# Property `height`

The `height` property is used inside [spacer blocks](copernica-docs:ResponsiveEmail/json/block-spacer)
to configure how much whitespace it should represent, this will default to 50px.


````json
    {
        "from" : "info@example.com",
        "subject" : "Email with a single spacer",
        "content" : {
            "blocks" : [ {
                "type": "spacer",
                "height": 50
            } ]
        }
    }
````


For more information and more examples, please check the documentation
of [spacer blocks](copernica-docs:ResponsiveEmail/json/block-spacer).