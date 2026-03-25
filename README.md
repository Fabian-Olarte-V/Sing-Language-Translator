# Sign Language Translator

A mobile prototype that translates text and speech into Colombian Sign Language (LSC) using pre-recorded interpreter videos.

This repository represents the product, engineering, and research work behind an accessibility-focused React Native application built with Expo. The project later became the basis for the Springer conference paper ["Automatic Translation of Text and Audio to Colombian Sign Language"](https://doi.org/10.1007/978-3-031-47372-2_11).

## Why this project stands out

- Designed a mobile experience focused on accessibility and inclusive communication.
- Combined text input, speech-to-text, and video-based sign delivery in a single workflow.
- Added authentication, translation history, and favorites for repeat usage.
- Led to a peer-reviewed conference publication based on the delivered application.

From a portfolio perspective, this project demonstrates mobile product development, API integration, media handling, user-centered design, and the ability to turn applied software work into published research.

## What the app does

The application allows users to:

- Enter a word or sentence and receive a Colombian Sign Language video translation.
- Record speech, transcribe it into text, and then request the sign-language output.
- Save translation history and favorite translations per account.
- Use the experience through a mobile-first interface with authentication and profile settings.

## Technical overview

**Frontend**

- React Native
- Expo
- React Navigation
- Expo AV for audio and video handling

**Integrations used in the prototype**

- Firebase Authentication
- Firebase Realtime Database
- External translation/video API
- External speech-to-text service

**Core flow**

1. The user submits text or records audio.
2. Audio is transcribed into text through a speech-to-text service.
3. The app requests the corresponding sign-language video from a translation service.
4. The resulting video is played in the app and can be saved to history or favorites.

## Publication

This application served as the foundation for the following publication:

Fernandez Becerra, S., Olarte Vargas, F.A., Rosero Quenguan, J.M., Vasquez Rendon, A.F., Rueda-Olarte, A. (2024). *Automatic Translation of Text and Audio to Colombian Sign Language*. In: *Advances in Computing*, CCC 2023, Communications in Computer and Information Science, vol. 1924. Springer.

- DOI: https://doi.org/10.1007/978-3-031-47372-2_11
- Springer page: https://link.springer.com/chapter/10.1007/978-3-031-47372-2_11

## Current status

This repository is shared as a portfolio and reference project.

Some external services originally used by the prototype are no longer available or are no longer configured for public access. As a result, this repository should be viewed as:

- A solid example of the app architecture and product implementation.
- A real accessibility-focused software project with academic impact.
- A prototype that would need updated service integrations to run the full translation pipeline end to end again.

The primary unavailable pieces are the external speech-to-text and translation/video services referenced by the client. The Firebase flows, app structure, and core implementation remain useful for review, extension, or modernization.

## Highlights for recruiters

- End-to-end mobile product implementation beyond static UI work.
- Integration of authentication, persistence, media handling, and external APIs.
- Accessibility-driven product scope with a concrete social impact use case.
- Research-backed execution with a published paper tied to the software.
- Clear modernization path by replacing retired services with current APIs.

## Project structure

```text
src/
  components/     Reusable UI and media components
  context/        Account and theme state management
  navigation/     Login and in-app navigation flows
  screens/        Translator, history, profile, and authentication screens
  services/       API calls for translation and speech-to-text
  utils/          Firebase configuration
```

## Running locally

### Prerequisites

- Node.js
- npm
- Expo CLI or Expo Go

### Install dependencies

```bash
npm install
```

### Start the app

```bash
npm start
```

Other available scripts:

```bash
npm run android
npm run ios
npm run web
npm test
```

## If you want to reactivate the project

To make the full experience functional again, the main work would be:

- Replace the retired translation/video endpoint with a current service.
- Replace the retired speech-to-text endpoint with a supported speech API.
- Move runtime secrets and environment-specific configuration out of source files.
- Upgrade dependencies from the current Expo and React Native versions.

## License

No license has been added yet. If you plan to publish this repository publicly, add the license that matches your intended usage.
