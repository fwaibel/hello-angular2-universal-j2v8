# Angular-Universal with Java backend using J2V8
This repository contains a simple (and very initial) example of using angular-universal with java backend using J2V8.

##Supported:
- Rendering using angular universal from java using J2V8
- Serving both the application and other rest endpoint from java using sparkjava
- Basic live-reload support for the universal server build 
- Linux x64 only
- Multi-Node (each in its own thread) rendring
- Very basic url based cache for increasing performance 

##TODO:
- Fetch J2V8 from maven central
- Support other platforms
- ~~Extracting internal implementation details from the angular-universal `server.js` and expose a proper API instead.~~
- ~~Support for rendering multiple requests at once~~
- Performance tests 
- Documentation and code-cleanup
- ~~Remove express dependency (currently the angular2-express-engine is used for rendring)~~
- Orginize project structure
- Implement a more complex application
- Check if can model the bootstrap configuration object in java in order to remove the need for server.js completely 
- Extend the configuration api (and cache) to receive the whole request instead of just the url

##Requirements
- x64 Linux (tested on ubuntu 16.04)
- Java 8
- Maven
- NPM
 
##Running Instructions
1. Clone the repository
2. Install node dependencies (`npm install`)
3. Build the java server(`mvn clean package`)
4. Build&Watch angular-universal + angular client side code (`npm start`)
5. Execute the java server (`mvn -e exec:java -Dexec.mainClass="hello.ngu.j2v8.Server"`)
6. Open your browser on `http://localhost:3000/app/`

##Links
- [Angular-Universal](https://github.com/angular/universal)
- [J2V8](https://github.com/eclipsesource/J2V8)
- [Spark-Java](http://sparkjava.com/)
- [Angular 2 Universal starter kit](https://github.com/angular/universal-starter)

###Thanks and credits
- The Angular-Universal-related files are based on Angular 2 Universal starter kit with very small modifications
- Special thanks to @irbull for the great J2V8 library and he's help.
