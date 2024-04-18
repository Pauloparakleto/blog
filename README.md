# README

This project provides trade off about creating a gem rewriting micro resources or relying on rails engine functionalities.

The [blog engine](https://github.com/Pauloparakleto/blorgh) provides minimal article blog functionality to the main application.

Let us think about each functionality as mirroring the indicators. E.g. If an indicator is bigger, it is a strong candidate for isolation in its own engine.

Each calculator can be its own engine. It also isolates the tests for each resource in order to deal with huge number of indicators.

Additionally, there is no need to extract templates inside the main application as they can be part of the gem in the engine's layout folder.

1. Install dependencies:

```
bundle
```

2. Extract the sample migration from engine:
```
rails blorgh:install:migrations
```

3. Run the migrations
```
rails db:migrate
```

4. Start the server
```
rails server
```

5. Go to mounted engine at `http://localhost:3000/blog/articles`
