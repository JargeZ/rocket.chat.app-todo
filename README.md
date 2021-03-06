# Rocket.Chat ToDo App

## Attribution

Based in part on Diego Sampaio's [Rocket.Chat Poll App](https://github.com/sampaiodiego/rocket.chat.app-poll).

## Requirements

Rocket.Chat Version: **1.4.0**

## Installing

Rocket.Chat ToDo App is not yet provided via Rocket.Chat Marketplace https://rocket.chat/marketplace.

To install ToDo on your Rocket.Chat server, you have to turn on the setting `Enable development mode` on the Rocket.Chat server under `Admin > General > Apps`.

Then you can then upload a release .zip from the [Releases Page](https://github.com/ianmclinden/rocket.chat.app-todo/releases/latest).

### Styling Workaround

The default Rocket.Chat styling for attachment buttons limits the maximum width to 220 pixels. To prevent Rocket.Chat from truncating todo list items, you can add a custom style rule.

Go to `Admin > Layout > Custom CSS` and add a custom style to increase the max width: 

```css
.attachment .text-button {
    max-width: 1024px;
}
```

## Usage

Use the slash command to create a todo list:

```
/todo "Changes before release" "Fix some bugs" "Adjust some formatting" "Clean up code"
```

The following todo list will be created:

![Todo list](https://user-images.githubusercontent.com/8931381/77254108-04ea1800-6c2d-11ea-8e2f-d6a788ae6522.png)

After an item is complete, you can click the item to check it off the list. For example:

![Todo list completion](https://user-images.githubusercontent.com/8931381/77254109-0582ae80-6c2d-11ea-912e-76f3363627b7.png)


## Contributing

You'll need to set up the Rocket.Chat Apps dev environment, please see https://rocket.chat/docs/developer-guides/developing-apps/getting-started/

To install the using the command line, you have to turn on the setting `Enable development mode` on the Rocket.Chat server under `Admin > General > Apps`.

Then you can clone this repo and then:

```bash
npm install
rc-apps deploy
```

Follow the instructions and when you're done, the app will be installed on your Rocket.Chat server.
