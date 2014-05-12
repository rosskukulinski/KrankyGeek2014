Speakit.io plugin for reveal.js
================


Move the voice folder into the reveal.js plugin folder such that it looks like: `revealjs/plugin/voice/voice.js`, and include the following in the presentation HTML:

```javascript
Reveal.initialize({
  // speakit.io config
  // @param voiceRoom - Name of the room
  // @param voiceAPIKey - API Key needed to create a room (not needed to join a room)
  voiceRoom: 'revealjs',
  voiceAPIKey: '',

  // Optional libraries used to extend on reveal.js
  dependencies: [
    { src: 'plugin/voice/voice.js', async: true, condition: function() { return !!document.body.classList; } }
  ]
});
```
