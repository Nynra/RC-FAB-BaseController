Suggested changes
----------------------------------
While the controller is working as is there is always room for improvement. I have a few suggestions for changes that could be made to improve the controller.

- Add a response id to responses send back to the pc (so the pc can parse which command was the source of the response)
- Make it possible to have the controller send the error state periodically to the computer. This makes it so the pc doesn't have to send a request to the controller to get the error state.