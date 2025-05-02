## @ch3yne/electron-notifier

forked from `NSFI/electron-notifications-win`

## Installation

```
npm install --save @ch3yne/electron-notifier
```

## Usage

```javascript main.js
const notifier = require('@ch3yne/electron-notifier')

notifier.config({
  limit: 1000,
  spaceHeight: 20,
  icon: 'icon.png',
  autoClose: false,
  bigPopup: true,
  silent: false,
})

notifier
  .notify({
    title: 'from main process',
    body: 'hello',
  })
  .on('close', (id) => {
    console.log('close', id)
  })

// only use sound
notifier.beep()
```
