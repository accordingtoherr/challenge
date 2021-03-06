This repo contains two codebases: [web](https://github.com/clerestoryio/fullstack-challenge/tree/main/web) contains a React app that is powered by a REST API in the   [api](https://github.com/clerestoryio/fullstack-challenge/tree/main/api) directory. The API uses [TypeORM](https://typeorm.io/) to talk to a SQLite database.


## Self-Critique

- The main items I would focus on and add/iterate with more time would be design and also separating into more atom component structure so some pieces can be potentially reused. 
- Also, the bug I was encountering looks to be related to the ORM itself as I was having errors about how the data was sent to SQL with non null and also proxying from client side to server side. To correct the first one I ensured valid data that was not undefined was being sent, and that it matched the model. Also, I utilized Postman where I could access the database perfectly fine which led me to conclude it was in the onSubmit function. Also, the proxy looked as though not the frontend and backend were running at the same time which they both were, with concurrent which led me to believe the bug was due to the express server interacting with the ORM. 
- I would have liked to add tests that the data was rendering per route and per UI
- The API routes do work as expected when using CURL and I made sure to use helmet and remove the x-powered-by field for security reasons 


## Setup
1. Install Node: https://nodejs.org/en/download/
2. Install yarn: https://classic.yarnpkg.com/en/docs/install/#mac-stable
3. Install deps by running `yarn deps`
4. Start the app with `yarn start`

###

If all went well, you should be able to access the app at [http://localhost:3000/](http://localhost:3000/).
#   c h a l l e n g e  
 