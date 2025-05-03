# Music4U App


<img src="https://github.com/user-attachments/assets/1b1c2d8a-b0d6-4d06-abda-25a75ae304d5" width="192" height="192"/>


## Done by:
1. Karimkhanov Tursynkhan (Team Lead)
2. Akhanayeva Aruzhan (Main Designer)
3. Amangeldi Zhanserik (Tech Support)


The app is built in Kotlin with a modern Jetpack Compose UI. On launch, you’re greeted by a list of music genres, with a heart icon in the top corner takes you to your Favorites. Tapping a genre opens an artist's screen showing performers in that style; selecting an artist brings up their profile and a list of albums. From the Artist Details page, you can dive into any album’s page, where you can preview tracks for 30 seconds and add or remove them from your Favorites. Those same previews—and the ability to stop them at any time—are available on your Favorites page, where you can also unfavorite songs. Finally, the entire app seamlessly supports both light and dark themes for comfortable listening in any setting.



## Video from app 📱

<div>
  
  <video src='https://github.com/AhmetOcak/DeezerApp/assets/73544434/d3938ef7-89ed-4bb1-ba2a-92c784e1f779' />
  
</div>



|                    | Dark | Light |
|--------------------|------|-------|
|  |<img src="https://github.com/AhmetOcak/AppcentDeezerApp/assets/73544434/cddde99e-8ea9-4867-b40d-71e709385862" width="240" height="480"/>     | <img src="https://github.com/AhmetOcak/AppcentDeezerApp/assets/73544434/b71db5ee-51e1-40c8-a5f9-ce0ba536192b" width="240" height="480"/>      |

## Modulirization  📦

<img src="https://github.com/AhmetOcak/DeezerApp/assets/73544434/42d768b5-cb84-4909-b41a-4cc2fe084cdf"/>
 
* ``:app`` The module responsible for navigation.
* ``:feature:albumdetail``,``:feature:artistdetail`` ,``:feature:artists`` ,``:feature:favorites`` ,``:feature:musicgenres``, ``:feature:playmusic`` Each module represents a screen.
* ``:feature:designsystem``  It houses the components and icons present in the application. It sets the theme of the application.
* ``:feature:ui`` It houses the common components used by screens.
* ``:core:models`` It contains the models to be used on the UI side.
* ``:core:domain``  It houses use cases. It serves as a bridge between the data layer's repositories and the UI.
* ``:core:data`` It retrieves data from sources and sends it to the UI through the ``:core:domain`` module. 
* ``:core:network``  It sends requests to APIs and processes the returned responses.
* ``:core:database`` It stores data in a local database using Room.
* ``:core:common`` Stores common classes shared between modules.

## Architecture 🏗
The app uses MVVM [Model-View-ViewModel] architecture to have a unidirectional flow of data, separation of concern, testability, and a lot more.

![mvvm](https://github.com/user-attachments/assets/874f7380-3e00-49ae-8cad-f268596b09c0)
