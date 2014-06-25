Scaling WebRTC Audio for Gaming and Other Applications
===========================

Talk Summary
---------
Peer-to-Peer is all fun and games until you need to scale.
In this talk, we"ll cover p2p architectures and then dive into
how SpeakIt.io is scaling WebRTC conferences to over 50+ attendees
through a real-time audio mixing platform.


Outline
--------

* Welcome Slide
* Overview of problem
  * P2P is great for <4-6 people
  * Show comparison of platform max-user count
  * Audio mixing (CPU) & Transmission (Bandwidth)
* Solution: Server!







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
