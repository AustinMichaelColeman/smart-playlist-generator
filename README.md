# smart-playlist-generator

A smart playlist generator plugin for ChatGPT and for YouTube Music™

## Under development

This plugin is in development, but if you'd like to see it in action check out [this recording I made](https://www.linkedin.com/feed/update/urn:li:activity:7067945888945508352/).

Also if you're curious, you can see some of the [playlists](https://music.youtube.com/browse/UC7S-wmivIpyNwZVrc3PlA-A) I've generated so far while developing it.

## Features

- **Generate playlists for YouTube Music™**: Given a list of songs and a playlist title, the plugin will search for each song on YouTube and put them into a playlist.

- **Informed Consent**: Prior to generating the playlist, the plugin ensures transparency by informing the user of the following actions and seeking their express consent that:
  - The generated YouTube playlist will be public.
  - The playlist will be publicly associated with the user's YouTube account.
  - The user will be provided with the list of songs planned to be added to the playlist.
  - The user will be informed of the playlist name that is planned to be used.

## Collaborating

I welcome collaboration! Reach out to me. My email is listed on https://www.austincoleman.dev/

## Configuration

For future reference to myself or others who'd like to fork this project, here is how you configure it:

1. Set the following environment variables:
   - `SERVER_URL`: Your server URL, such as `app.vercel.com`
   - `CONTACT_EMAIL`: Your contact email address
   - `OPENAI_VERIFICATION_TOKEN`: Obtain this token from OpenAI. See the [ChatGPT Plugin docs](https://platform.openai.com/docs/plugins/introduction)
   - `SCOPE`: Enter the scopes you're using from Google API. Unfortunately Google does not give granular permissions over playlist creation for YouTube Music. So in order for this plugin to work, it requires very broad YouTube scopes to create playlists and insert songs into playlists: `https://www.googleapis.com/auth/youtubepartner https://www.googleapis.com/auth/youtube https://www.googleapis.com/auth/youtube.force-ssl`
   - `AUTH_PROVIDER_URL`: URL for the authentication provider (e.g., `https://accounts.google.com/o/oauth2/v2/auth`)
   - `TOKEN_PROVIDER_URL`: URL for the token provider (e.g., `https://oauth2.googleapis.com/token`)

Additionally, in your Google Cloud console be sure to update the authorized JavaScript origins and Authorized redirect URIs. The token that comes from OpenAI during the plugin creation process needs to go into the authorized redirect URI.

## Use of Trademarks

YouTube Music™ is a trademark of Google Inc. Use of this trademark is subject to [Google Permissions](https://about.google/brand-resource-center/).

ChatGPT is a trademark of OpenAI. Use of this trademark is subject to [OpenAI Brand guidelines](https://openai.com/brand).
