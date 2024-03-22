# [2024] Senior Mobile Exercise (React Native)

This App renders the list of movies in the list and users can view, add favorite movies in the storage.

## Running locally

Make sure you have all the necessary dependencies installed on your system:

- Node.js
- Ruby
- Xcode
- CocoaPods
- Android Studio and all Java dependencies.

You can follow the instructions on the React Native docs to set up your local environment: https://reactnative.dev/docs/environment-setup

To run the project locally:

- Clone the repo
- Install the dependencies with `npm install`
- Run `cd ios && pod install && cd ..` to install all iOS dependencies
- Run the dev server with `npx react-native start`
- Build and Run the app with `npx react-native run-ios` for the iOS version or `npx react-native run-android` for the Android version

If you have problems with any of the instructions above, please refer to the React Native docs. This is a newly created app and the latest instructions there should help you get your environment up and running without issues.

Please keep in mind that this app doesn't use Expo and we need you to run the app with the React Native CLI.

## Requirements

For the sake of the example and requirements below, let’s assume I show to make an anime demo app.

1. The app should be able to **list** all of entities for the user to pick from
    1. For example, a list of all animes
2. The app should be able to tap on an entity from the list view and dive into the details
    1. For example, if I clicked on One Piece, I would now see a page with more information about the anime
3. The app should be able to favorite a given entity
    1. For example, I could favorite One Piece and it would show up as favorited. I can unfavorite it and it would also show up as unfavorited (for the sake of simplicity, this can be done locally and does not need API integration)
4. The app should be able to search for a given entity from within the list
5. The app should gracefully handle errors/issues as it would on production
6. The app would have a very simple onboarding screen before the user interacts with it for the first time telling them what the app is about and the features it contains


## Overview
- Screens
Onboarding, Discover, Details and Favorites
- Technologies
JavaScript, React native cli, Redux, React navigation
- Main features
It uses **FlatList** to render the list of the data, implemented the pagination for the large amount of data.
It uses public movie API to retrieve the data.
It uses AsyncStorage to save the favorite movies in the local.
It uses Redux to store the movie items.
It uses combination of the stack navigator and tab navigator for the user friendly interfaces.
It uses eslint and prettier for the coding standards.

## I am gonna improve more things here if I have more time.
1. Testing.
I am gonna write some testing for the components with unit testing and integration testing (Using Jest)
2. Improve filter functionality
Right now, it filters from the local list data, but if there is an endpoint to get the filtered list from the movie list in the back-end, I would like to get the filtered data using debounce for optimization.
Also I am gonna improve the component with some search icon and placeholder.
3. Implement Toast component.
If there are issues while connecting to the endpoint, or the execution is succeed like favorite items, I would like to show the toast in the react native for the user-friendly implementation.
4. Bring the additional styling library with the theme customization.
I am going to bring some styling libraries like native-base, react-native-paper or tamagui for the better components. (Right now, it uses the original components from react native with the stylesheet)

## Images
![favorite](https://github.com/MikeLiuag/firekamp-exercise/assets/122606053/ae63e000-fb56-4a55-97d6-07e9dca6cebd)
![discover-2](https://github.com/MikeLiuag/firekamp-exercise/assets/122606053/c33e7886-58df-4580-bb05-3574b5f1544a)
![discover-1](https://github.com/MikeLiuag/firekamp-exercise/assets/122606053/2b72e37a-bb8d-4100-aed0-711a593a7b95)
![detail-2](https://github.com/MikeLiuag/firekamp-exercise/assets/122606053/34a2d514-fafa-481b-a8b7-d575fd5c8de3)
![detail](https://github.com/MikeLiuag/firekamp-exercise/assets/122606053/1adc3707-443c-47a6-ae8c-c1921c534315)
