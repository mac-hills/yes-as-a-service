# Yes-as-a-Service

Sometimes what we truly need is an enthusiastic, unambiguous **YES** — and this service provides exactly that, **FREE OF CHARGE!**

---

### Why Yes-as-a-Service?

- Because !NO is YES, but it doesn’t look like a YES.

- Because !!YES is technically fine, but confusing.

- Because NOT NOT YES is clever... but also a mouthful.

- Because sometimes all you need is YES!

Just say YES — powered by !NO.

---

### How to do it

Keep it simple — just like a real yes, in code the easiest way to express a YES is a boolean `true` value:

#### cURL
```bash
curl  https://mac-hills.github.io/yes-as-a-service/request.json 
```

#### JavaScript
```js
fetch('https://mac-hills.github.io/yes-as-a-service/request.json')
  .then(res => res.json())
  .then(json => console.log(json)); // { "response": true }
```

#### OkHttp (Java Virtual Machine & Android) - written in Kotlin
```
val client = OkHttpClient()
val request = Request.Builder()
    .url('https://mac-hills.github.io/yes-as-a-service/request.json')
    .build()

client.newCall(request).enqueue(object : Callback {
    override fun onFailure(call: Call, e: IOException) {
        // Do something with your error
    }

    override fun onResponse(call: Call, response: Response) {
        // do something with the response
    }
})
```

#### iOS
```
let session = URLSession.shared
let requestUrl = URL(string: "https://mac-hills.github.io/yes-as-a-service/request.json")!

session.dataTask(with: requestUrl, completionHandler: { data, response, error in
    if let error = error {
        print(error)
        return
    }
    
    guard let data = data else { return }
    
    // Do something with the response
}).resume()
```

---

### ⚖️ License & Attribution

This project is based on [No-as-a-Service](https://github.com/gotev/no-as-a-service) by Aleksandar Gotev, licensed under the [Apache License 2.0](https://www.apache.org/licenses/LICENSE-2.0).

Modifications have been made to return a "YES" response instead of "NO".  
This project is also licensed under the Apache License 2.0.

---

### YES!

If you’re reading this, you’re probably ready to say YES.  
So... just do it. ✅
