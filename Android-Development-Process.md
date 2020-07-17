
• Create github repo

## First part
- Add Material Design dependency
- Create activities
- Organize layout
- Add ViewModel + LiveData dependency (don't forget ktx)
- Connect ViewModel with Activities to handle view states (use LiveData)
- Extend AppTheme from heme.MaterialComponents.Light.NoActionBar
- Identify repeated sections and create custom styles

## Second part
- Add Retrofit2, Converter Gson and Logging Interceptor dependencies
- Create serialize data classes for Json Responses
- Create service interface (eg. WeatherService)
- Create RetrofitClient using builder
- Create Retrofit service class from service interface (retrofit.create)
- Create RemoteDatasource class and pass service as parameter
- Add Room dependencies (runtime, compiler, testing and ktx)
- Create entities with column info
- Create Dao interface for operations
- Create the database (you can add a Callback to populate everytime user reinstall the app)
- Create a LocalDatasource class and pass the Dao as parameter

## Third part
- Create a repository class. This class receive both datasources (local and remote).
- Mark each operation as suspend function and use withContext(Dispatcher.IO)
- Create an Application class and register
- Create an AppComponent class with references to the repository and its dependencies
- Create a ViewModelFactory<T> class
- Retrieve the appcomponent object through Application object
- Replace the direct creation of viewmodel in Activities for using ViewModelFactory class and pass the repository from appComponent.
- Complete ViewModel implementation (liveData{} and viewModelScope{})

## Fourth part
- Add github actions (CI)
- Add Hilt dependencies
