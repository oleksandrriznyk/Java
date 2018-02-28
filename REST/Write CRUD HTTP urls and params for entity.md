If you want to write HTTP CRUD methods that will be match RESTful system you should write it in specific format.
Take, by way of example HTTP methods on user entity. Then HTTP methods would be like:

Create user (POST)

    ip:port/users

Update user (PUT)

    ip:port/users/{id}

Get user/all users (GET)

    ip:port/users/{id}
    ip:port/users

Delete user (DELETE)

    ip:port/users/{id}

Patch user (PATCH) (*partial update*)

    ip:port/users/{id}

