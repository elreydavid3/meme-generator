# meme-generator

Here in meme-generator I created a React.js application with input boxes on the UI that post to the top and bottom of the picture  each time the user clicks the button.

I created 2 components (Header and MemeGenerator). Header only displays things as a fuctional component.
MemeGenerator will be calling to an API and holding on to data.

Using the componentDidMount method I made an API call to "https://api.imgflip.com/get_memes" and saved the 
data that comes back (`response.data.memes`) to a new state propertycalled `allMemeImgs`. 
(The data that comes back is an array).

I also created the onChange handler method that updates the corresponding state on every change of the input box.

Also I created a method (handleSubmit) so that, when the "Generate" button is clicked, it chooses one of the memes from our `allMemeImgs` array at random and makes it so that it's the meme image that shows up in the bottom portion of our meme generator site. I do that by getting a random int (index in the array), getting the meme from that index and setting `randomImg` to the `.url` 
