I wrote this project to see what it would look like to make a call to Deepgram from a Next app. I chose Next because of the ease of making server-side calls from a Next project -- since this API requires a private key, I didn't want to make my calls from the client.

To take a closer look at my project on your local machine, `git clone https://github.com/Cerchie/fun-with-deepgram-and-next && cd fun-with-deepgram-and-next && npm install && npm run dev`. (You'll need [npm](https://www.npmjs.com/) installed.)
You'll also need to make a file in your root directory called `env.local` and put your Deepgram apikey in it like so: `DEEPGRAM_APIKEY=your_apikey_here`

You can learn more about the inner workings by consulting the [Next](https://nextjs.org/docs) and [Deepgram](https://developers.deepgram.com/) documentation.

Right now the call is made to an audiofile hosted by Deepgram and simply renders the transcript to the home page. 

Here are my goals for this project in the future:

1. Render the words in a more interesting way. 
I'd like to make use of some sort of module to render the words based on something like frequency, perhaps. This would require a larger sample audio file. I also haven't made any changes to the out-of-the-box Next styles yet.  
2. Render a streaming transcript [via websocket](https://developers.deepgram.com/api-reference/#transcription-streaming). 
This would affect the design choices of my first goal -- for example, if I chose a frequency chart module, I'd have to pick one that was dynamic. 
3. Once I've rendered the streaming transcript, push the Deepgram API further by [utilizing parameters](https://developers.deepgram.com/api-reference/#transcription-prerecorded) like `search` or `callback`.
