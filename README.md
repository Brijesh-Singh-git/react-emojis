# react-emojis

> :rocket: :hamster: :tada: Render all current emojis with proper accessibility markup, on any size

[![MIT Licence](https://img.shields.io/badge/license-MIT-blue.svg)](https://github.com/dreamyguy/react-emojis/blob/master/LICENSE)

Use **react-emojis** to output the recommended markup for accessible emojis:

```javascript
<Emoji emoji="woman-dancing"/>
```

...outputs:


```html
<span role="img" aria-label="woman dancing" class="react-emojis" style="line-height: 1;">💃</span>
```

## The emojis :tada: :balloon: :unicorn:

Instead of maintaining a list of _emojis_ on this README, I decided it would be best to create a living github page, that would serve both as a way of showcase the _emojis_, the **Emoji** component and facilitate their use:

https://dreamyguy.github.io/react-emojis/

On this page you can:

- Search for _emojis_
- Copy the _emoji_ to the clipboard by clicking on your choice
- Choose what you'd like to copy to the clipboard:
    - **emoji**: The 'emoji' itself _(this is the default option)_.
    - **markup**: Accessible emoji markup.
    - **reactEmojis**: **Emoji** component markup _(based on "react-emojis" usage)_.
    - **nameUrl**: Emoji name _(the reference used by "react-emojis")_.
    - **name**: Emoji name _(CLDR formatting)_.
    - **code**: Emoji's Unicode.
    - **id**: The emoji's id, as set by unicode.org.

## Scaling

**The emoji will inherit the font size set by the parent element**. However, you can override that behavior by doing the following:

- Setting a `font-size` to the class `react-emojis`, which the markup output provides out of the box.
- Passing a `size` _prop_ to the component.

The latter can be done as follows:

```javascript
<Emoji emoji="woman-dancing" size="100"/>
```

This will give the emoji `100px` _**font-size**_.

> I'll be working on passing units to the component, so one can scale the emoji in whichever way one prefers. For convenience, the default unit will remain `px` if no `sizeUnit` is passed as _prop_.

## Origin

The [emoji list](https://github.com/dreamyguy/react-emojis/blob/master/src/app/components/EmojiData.js) is based on [unicode.org](https://unicode.org/emoji/charts/full-emoji-list.html)'s current list of named emojis under "browser" column (as of 2019-05-30).

# Using _react-emojis_ through `npm`

**react-emojis** is also [available as a package on `npm`](https://www.npmjs.com/package/react-emojis) and can be installed as a depedency with:

    npm i react-emojis --save

More documentation coming soon!

# Development

## Getting started

Clone this repo locally. You'll need to have [NodeJS][1] installed. Install all dependencies by running:

    npm i

## Run it locally

To start the app locally, run:

    npm run start

This command fires up the application on port `9900`, making it visible on http://localhost:9900. Because this app is based on [create-react-app][3], the port number should be configured on the [.env](https://github.com/dreamyguy/react-emojis/blob/master/.env#L1) file.

## Building the frontend for Production

When you're ready to build for production, run:

     npm run build

This command compiles all production-optimised resources to a folder called **build**. It's meant to be run remotely, at the environment host, at build time.

## License

[MIT](LICENSE)

# About

**react-emojis** was conceived and developed by [Wallace Sidhrée][1]. is written in [React][4]. It was initialized through [create-react-app 2][6] and built upon that with some sensible strategies. [Jest][7] is used for tests. [VS Code][12] was used as the IDE of choice.

  [1]: http://sidhree.com/
  [2]: https://nodejs.org/
  [3]: https://github.com/creationix/nvm
  [4]: https://reactjs.org/
  [5]: https://redux.js.org/
  [6]: https://facebook.github.io/create-react-app/
  [7]: https://facebook.github.io/jest/
  [8]: https://facebook.github.io/watchman/
  [9]: https://airbnb.io/enzyme/
  [10]: https://momentjs.com/
  [11]: https://brew.sh/
  [12]: https://code.visualstudio.com/
