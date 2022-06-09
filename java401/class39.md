# Kinesis

## Get the last known location 

Using the Google Play services location APIs, your app can request the last known location of the user's device. In most cases, you are interested in the user's current location, which is usually equivalent to the last known location of the device

## Set up Google Play services

- Download and install the Google Play services component via the SDK Manager and add the library to your project. 
- Apps whose features use location services must request location permissions

## Create location services client

    private FusedLocationProviderClient fusedLocationClient;
    
    // ..
    
        @Override
        protected void onCreate(Bundle savedInstanceState) {
        // ...
        
            fusedLocationClient = LocationServices.getFusedLocationProviderClient(this);
    }

## Get the last known location

When your app is connected to these you can use the fused location provider's getLastLocation() method to retrieve the device location.

    fusedLocationClient.getLastLocation()
    .addOnSuccessListener(this, new OnSuccessListener<Location>() {
        @Override
        public void onSuccess(Location location) {
        // Got last known location. In some rare situations this can be null.
            if (location != null) {
            // Logic to handle location object
            }
        }
    });

## Choose the best location estimate

- getLastLocation() gets a location estimate more quickly and minimizes battery usage that can be attributed to your app.
- getCurrentLocation() gets a fresher, more accurate location more consistently.