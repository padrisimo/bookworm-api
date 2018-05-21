# Bookworm

Set a Mongo db called bookworm:

```
> use bookworm
```


Insert the user model: 

```
> db.users.insert({ email: "test@test.com", passwordHash: "$2b$10$bQ4v8cIaq.YfUdaTa5v5lu2vaLwzhsNIBKwsQcfkShhbS7iyVByaq"})
WriteResult({ "nInserted" : 1 })
```

Check if you did right by typing:
```
> db.users.find()
```

Should return:

```
{ "_id" : ObjectId("5b01ba971af1cdff393fdaf3"), "email" : "test@test.com", "passwordHash" : "$2b$10$bQ4v8cIaq.YfUdaTa5v5lu2vaLwzhsNIBKwsQcfkShhbS7iyVByaq" }
```

> passwordHash is _12345_ bcrypted