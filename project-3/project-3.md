# **MERN STACK IMPLEMENTATION**

* ##  **BACKEND CONFIGURATION**
          so i updated my ubuntu with the code below



`sudo apt update`

![apt update](./images/apt%20update.PNG)


       and i upgraded my ubuntu with the code below
`sudo apt upgrade`


![apt upgrade](./images/apt%20upgrade.PNG)

      i got the location of my Node.js software from Ubuntu repositories with the code below

`curl -fsSL https://deb.nodesource.com/setup_18.x | sudo -E bash -`


![curl d](./images/curl%20d.PNG)

      installed node.js with the code below



`sudo apt-get install -y nodejs`

![nodejs](./images/nodejs.PNG)


       verified the nodejs installation  with "node -v" & "npm -v"


![-V](./images/-v.PNG)      



       I created a Todo directory and run `npm init`


![todo](./images/todo.PNG)      

![init](./images/init.PNG)



* ##  **INSTALLING EXPRESSJS**
        I `npm install express` `touch index.js` and npm `install dotenv` in the Todo directory


![install ex](./images/install%20ex.PNG)

       `vim index.js` pasting the necessary code 

![VIM 1](./images/vim%201.PNG)

       After that i `node index.js`, verified on the web broswer if its working fine, created a routes directory and `touch api.js` in the routes directory
    
![pro](./images/pro.PNG)

![welc](./images/welc.PNG)

       i pasted the provided code in the api.js 

![vim 2](./images/vim%202.PNG)


* ## **CREATING MODELS**

         i  installed mongoose with `npm install mongoose`, created a models directory and `touch todo.js` in  models directory

![pro 2](./images/pro%202.PNG)


          i pasted the provided code in the todo.js file


![todo.js 1](./images/todo.js%201.PNG)

        i updated my api.js file in the routes directory

![update api.js](./images/update%20%20api.js)



* ## **CREATED A MONGODB DATABASE**



![mongodb](./images/mongodb.PNG)

           craeted a .env file in the Todo directory and i paste my mongodb strings in it


![.env](./images/.env.PNG)


         I updated my index.js file with the code provided
        
![index.js updaed](./images/index.js%20updated.PNG)


          then i started my server using `node index.js` to connect to our mogodb database

![db connect](./images/db%20connect.PNG)



         so i tested our API with postman

![post 1](./images/post%201.PNG)

![post 2](./images/post%202.PNG)


* ## **FRONTEND CREATION**

          i started my frontend creation by installing the react-app with the code below


` npx create-react-app client`

![NPX 1](./images/NPX%201.PNG)

![NPX 2](./images/NPS%202.PNG) 

           installed concurrently with the code below

`npm install concurrently --save-dev`

![conc](./images/conc.PNG)

        installed nodemon with the code below

`npm install nodemon --save-dev`

![nodemon](./images/nodemon.PNG)

 
          i updated my package.json file in the Todo directory by adding the new script code 


![pack t update](./images/pack%20t%20update.PNG)

         update my package.json file in the client directory by adding "proxy": "http://localhost:5000"


![pack tc update](./images/pack%20tc%20update.PNG)



         THEN I RAN THE `npm run dev` command 

![npm run dev](./images/npm%20run%20dev.PNG)


![react](./images/react.PNG)


           i follow the steps on the page below

![page 1](./images/page%201.PNG)

![cont](./images/cont.PNG)
 
          my Input.js file

![Input.js](./images/Input.js)

          my ListTodo.js file 

 ![Listtodo.js](./images/ListTodo.js)


          my Todo.js file   

![Todo.js 4](./images/Todo.js%204.PNG)


          I made little adjustment to my App.js file, App.css file and index.css file in our SRC folder as instructed


         App.js file

 ![App.js](./images/App.js) 

         App.css file

![App.css](./images/App.css)

         index.css file

![index.css](./images/index.css)



         i went back to Todo directory and ran `npm run dev` command


![npm run dev 2](./images/npm%20run%20dev%202.PNG)


        went bak to my web broswer to verify my result


![final result](./images/final%20result.PNG)