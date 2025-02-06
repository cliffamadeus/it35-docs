# IT35-Lab-02 - Deployment
## Description
On a Software Development Life Cycle (SDLC), deployment is one of the key phases that shows the completion of a product for public use. In
order to see through the developed application's scalability, some configurations and specifications must be well documented to ensure
for the life cycle to iterate once again. 
Ionic uses the Vite, a web server and build tool that comes within the latest Ionic version. Combined with the `gh-pages` npm package,
the repository that was established from the `Laboratory 1` shall be deployed through GitHub pages.

**Objectives**
1. To configure the project repository deployment server using Vite.
2. To add the `gh-pages` packages within the project repository.
3. To deploy the repository on GitHub Pages.
   
**Methodology**
1. Reconfigure existing `git config --global` on the workstation.
2. Clone the established `it35-lab` repository.
3. Run the `npm install` in order to install the needed `node_modules` to your local repository
4. Start your development server using `ionic serve` command
5. Create and access a development branch named `dev-deployment`

6. Configure Vite base server
    - [ ] On your project repostory go to the `vite.config.ts` file
    - [ ] Insert the following line of code:  `base:"it35-lab",` on line `13` and save the file
    - [ ] Go your App.tsx and append the base changes to your routes
   
          <Route exact path="/it35-lab/home">
              <Home />
          </Route>
          <Route exact path="/it35-lab/">
              <Redirect to="/it35-lab/home" />
          </Route>
          
    - [ ] On your browser refresh the application preview or access the following url `localhost:{portnubmer}/it35-lab`
          
  **Note:** To ensure code readability and maintenance please secure a commit if the application is working

7. GH Pages
   - [ ] On your terminal install the following package `npm install gh-pages --save-dev` in order to deploy your application into the gh-pages
   - [ ] After installing the package add the following lines of code to your `package.json`:
         
         "homepage": "https://{username}.github.io/{repository-name}/"
            "scripts": {
            "predeploy" : "npm run build",
            "deploy" : "gh-pages -d dist",
         
   - [ ] Then run the `npm deploy` to deploy your application
