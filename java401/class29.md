# Room

## Save data in a local database using Room

The most common use case is to cache relevant pieces of data so that when the device cannot access the network, the user can still browse that content while they are offline.

The Room persistence library provides an abstraction layer over SQLite .

![room_architecture](../assets/class29/room_architecture.png)


## Setup
`Groovy`

    dependencies {
    def room_version = "2.4.2"
    
        implementation "androidx.room:room-runtime:$room_version"
        annotationProcessor "androidx.room:room-compiler:$room_version"
    
        // optional - RxJava2 support for Room
        implementation "androidx.room:room-rxjava2:$room_version"
    
        // optional - RxJava3 support for Room
        implementation "androidx.room:room-rxjava3:$room_version"
    
        // optional - Guava support for Room, including Optional and ListenableFuture
        implementation "androidx.room:room-guava:$room_version"
    
        // optional - Test helpers
        testImplementation "androidx.room:room-testing:$room_version"
    
        // optional - Paging 3 Integration
        implementation "androidx.room:room-paging:2.5.0-alpha01"
    }

## Primary components
- Database class that holds the database and serves
- Data entities that represent tables in your app's database
- Data access objects (DAOs) that provide methods that your app can use to query, update, insert, and delete data in the database.


## Defining data using Room entities 
you define entities to represent the objects that you want to store. Each entity corresponds to a table in the associated Room database, and each instance of an entity represents a row of data in the corresponding table.

## Define relationships between objects

Even though most object-relational mapping libraries allow entity objects to reference each other, Room explicitly forbids this .

In Room, there are two ways to define and query a relationship between entities: 

- Using an intermediate data class with embedded objects . 
- Relational query method with a multimap return type .
 