Gson Codec
===================

This module adds support for encoding and decoding JSON via the Gson library.

Add `GsonEncoder` and/or `GsonDecoder` to your `Feign.Builder` like so:

```java
GitHub github = Feign.builder()
                     .encoder(new GsonEncoder())
                     .decoder(new GsonDecoder())
                     .target(GitHub.class, "https://api.github.com");
```

Or add them to your Dagger object graph like so:

```java
GitHub github = Feign.create(GitHub.class, "https://api.github.com", new GsonModule());
```
