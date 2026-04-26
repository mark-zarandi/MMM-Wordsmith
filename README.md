# MMM-Wordsmith

A [MagicMirror²](https://magicmirror.builders/) module that displays past **Wordsmith.org Word of the Day** entries.

MMM-Wordsmith shows a word and its meaning on your mirror, rotating through a local JSON word list. It is based on the structure of MagicMirror's default `compliments` module, but instead of compliments, it displays vocabulary words and definitions.

---

## Preview

Add a screenshot here once the module is running:

```md
![MMM-Wordsmith preview](screenshot.png)
```

---

## Features

- Displays a word and its definition
- Includes a bundled `wordsv2.json` word list
- Rotates words automatically
- Supports random or sequential display
- Can load a local or remote JSON word file
- Supports time-of-day word groups
- Supports date-specific and cron-style word groups
- Can react to MagicMirror weather notifications if weather-based word groups are configured

---

## Installation

From your MagicMirror `modules` directory:

```bash
cd ~/MagicMirror/modules
git clone https://github.com/mark-zarandi/MMM-Wordsmith.git
```

No build step is required.

Restart MagicMirror after adding the module to your config.

---

## Basic Configuration

Add this to the `modules` array in your MagicMirror `config/config.js` file:

```js
{
  module: 'MMM-Wordsmith',
  position: 'middle_center',
  classes: 'page0',
  config: {
    remoteFiles: 'wordsv3.json',
    updateInterval: 86400000 // update each day
  }
}
```

By default, the module loads words from:

```js
remoteFile: "wordsv3.json"
```

That file is included with the module.

---

## License

Add your license here.

If you are not sure what to use, MIT is a common choice for MagicMirror modules.
