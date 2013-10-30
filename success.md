FORMAT: 1A

# Rails + Dredd proof of concept

# Posts [/posts]

## Creating a POST [POST]

+ Request (application/json)
    + Headers

            Accept: application/json
            Content-Length: 92

    + Body

            {
                "post": {
                    "title": "My post title",
                    "content": "Some content"
                }
            }

+ Response 201
