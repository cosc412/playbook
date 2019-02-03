# Common Errors
Common errors can occur during the process development.  The purpose of this file is to have a quick solution available for reference
if someone is lost.

## Compiling Errors
If you are experiencing compiling errors and it has nothing to do with the code you have written you may have to stop the frontend or
backend and re-initiating it.

If this fails, then it probably has to do with your node_modules.  Make sure you pull the latest branch and run the command "npm i" in order
to reinstall all of the node modules.  Then try re-initiating it.

If this fails, then try deleting the node_modules folder in the project directory and running npm i again.

If all else fails, ask another project team member if they know how to solve the issue.

## Running the development environment
We are using Angular 2+ (not angularjs) and a node.js/express API environment.  Angular serves as our frontend and express serves as
our backend.  Remember, API simply is a means to get data to and from the internet, it is the middleman between the frontend and the
database.

To run the frontent environment, use the command "ng serve --open" to automatically open your browser on http://localhost:4200/.
Or run the "ng serve" command and open your browser to that link.

To run the backend environment, use the command "nodemon app.ts" to initialize the API.  Nodemon is a node.js module that detects if
there is a change in the files and recompiles the application so you don't have to.  You can also run "node app.ts" but note if you make
a change you will have to retype the command when a change is made.
