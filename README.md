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

## Outputs 🖼

|                    | Dark | Light |
|--------------------|------|-------|
| Music Genres | <img src="https://github.com/AhmetOcak/AppcentDeezerApp/assets/73544434/cddde99e-8ea9-4867-b40d-71e709385862" width="240" height="480"/>     | <img src="https://github.com/AhmetOcak/AppcentDeezerApp/assets/73544434/b71db5ee-51e1-40c8-a5f9-ce0ba536192b" width="240" height="480"/>      |
| Artists  | <img src="https://github.com/AhmetOcak/AppcentDeezerApp/assets/73544434/7431094e-7c76-478f-9683-c54e85791bcb" width="240" height="480"/>     |  <img src="https://github.com/AhmetOcak/AppcentDeezerApp/assets/73544434/42e08cd0-dcc5-4c4a-a9ca-f4fcfa558ec7" width="240" height="480"/>     |
| Artist Detail      | <img src="https://github.com/AhmetOcak/DeezerApp/assets/73544434/ccaae8d5-f531-46b0-8a6a-bf7d33451d0c" width="240" height="480"/>     |  <img src="https://github.com/AhmetOcak/DeezerApp/assets/73544434/e1e6416b-c030-42ab-8d03-4fb14abc7590" width="240" height="480"/>     |
| Album Detail        | <img src="https://github.com/AhmetOcak/DeezerApp/assets/73544434/f6508ea8-4206-4207-93af-ab648dc426c8" width="240" height="480"/>     |  <img src="https://github.com/AhmetOcak/DeezerApp/assets/73544434/d4df63dd-03ef-421d-a75d-a92acbbfaff4" width="240" height="480"/>     |
| Favorites       | <img src="https://github.com/AhmetOcak/AppcentDeezerApp/assets/73544434/e009941b-fbd4-4153-96f5-23fd49d727f3" width="240" height="480"/>     |  <img src="https://github.com/AhmetOcak/AppcentDeezerApp/assets/73544434/f801affa-a08a-47d7-bccb-0802865fbdad" width="240" height="480"/>     |
| Play Music       | <img src="https://github.com/AhmetOcak/DeezerApp/assets/73544434/89f05073-21ca-484f-86a3-cc9ce32faef0" width="240" height="480"/>     |  <img src="https://github.com/AhmetOcak/DeezerApp/assets/73544434/5e42a0ab-b128-469b-bf60-a3b4c47f0739" width="240" height="480"/>     |

## Modularization 📦

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

![mvvm](https://user-images.githubusercontent.com/73544434/197416569-d42a6bbe-126e-4776-9c8f-2791925f738c.png)
