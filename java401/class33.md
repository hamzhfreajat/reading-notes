# GraphQL @connection
### @hasOne
Create a one-directional one-to-one relationship between two models.

### @hasMany
Create a one-directional one-to-many relationship between two models.

### @belongsTo
Use a "belongs to" relationship to make a "has one" or "has many" relationship bi-directional .

### @manyToMany
Configures a "join table" between two models to facilitate a many-to-many relationship.


## CompletableFuture
Java 8 introduced the CompletableFuture class. Along with the Future interface, it also implemented the CompletionStage interface. This interface defines the contract for an asynchronous computation step that we can combine with other steps.

###  Using CompletableFuture as a Simple Future
The CompletableFuture class implements the Future interface, so we can use it as a Future implementation, but with additional completion logic.

    public Future<String> calculateAsync() throws InterruptedException {
    CompletableFuture<String> completableFuture = new CompletableFuture<>();
    
        Executors.newCachedThreadPool().submit(() -> {
            Thread.sleep(500);
            completableFuture.complete("Hello");
            return null;
        });
    
        return completableFuture;
    }

### CompletableFuture with Encapsulated Computation Logic

Static methods runAsync and supplyAsync allow us to create a CompletableFuture instance out of Runnable and Supplier functional types correspondingly , Both Runnable and Supplier are functional interfaces that allow passing their instances as lambda expressions thanks to the new Java 8 feature.

    CompletableFuture<String> future
    = CompletableFuture.supplyAsync(() -> "Hello");
    
    // ...
    
    assertEquals("Hello", future.get());

### Processing Results of Asynchronous Computations
The thenApply method does exactly that; it accepts a Function instance, uses it to process the result, and returns a Future that holds a value returned by a function

    CompletableFuture<String> completableFuture
    = CompletableFuture.supplyAsync(() -> "Hello");
    
    CompletableFuture<String> future = completableFuture
    .thenApply(s -> s + " World");
    
    assertEquals("Hello World", future.get());