# Creative Layer Users Challenge

I created an app for [Creative Layer](https://www.creativelayer.com/) for an coding challenge which I was tasked to create an app which would grab mock user data from an [API](https://5fbc04c1c09c200016d4160c.mockapi.io/api/v1/customers) and display it on the screen.  I then had to implement the ability to sort through any of the fields, as well as add a way to filter through the users, and have a way to click on a user and bring up their full details.

See live project [here](https://cl-users-challenge.netlify.com).

I built this out within Vue and leaned a lot on BootstrapVue for putting it together due to the time window given for this.

To run the app locally, `git clone` this repo, and then `npm i` to install the necessary plugins and packages.  Then run `npm start serve` to get the local server which will be on `localhost:8080`.

When the app starts, it will automatically populate the table with all the data gathered from the API.  You can click on one of the first 3 headers to sort that column of data (ascending and descending).  You can also type in the input bar at the top to filter through all fields and populate data to matches, and will be given a message if no data matches.  The user can also click the button in each row to bring up a modal with the full details of that user.
