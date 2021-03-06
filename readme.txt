NodeJS Template

1. Installed Libraries
	Mongoose -- MongoDB driver for Schemas/Models
	Compression -- Gzip compression of server content
	Node UUID - Generate global IDs
	Bower - Client library manager
	Sendgrid - Email client


2. Middleware
	EnableCORS -- Allow cross-browser requests

3. Templating 
	EJS -- Embedded Javascript (in the /views directory)
	HTML -- HTML files can be placed in the /public directory

4. App.js
	Main application file 

5. Default port configuration
	Default is 3000. But also reads server.address().port in case port is different. 
	Run application at http://localhost:3000

6. Run application
	npm install
	bower install
	open a new terminal/console and run 'mongod' (make sure mongodb is installed)
	in original terminal/console, run nodemon app.js (if required, npm install -g nodemon)
	[NB* To run in production mode, switch env to 'production' in app.js, then run MONGOLAB_URL=urlnamehere nodemon app.js Database url is set as an environmental variable]

7. Deployment
	Set environment to production (app.js)
	Comment out app.loadTestValues (application.js) [Loads test values for development purposes]
	Deploy using eb deploy (ptap-production.elasticbeanstalk.com)
