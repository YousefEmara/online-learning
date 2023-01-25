
# Online learning platform

This project is about online learning, it helps individual to reach out interesting courses wherever he/she is.

#### Motivation:
As the internet and technology is spreading world widely; an online learning platform would be helpful for both parties the knowledge seekers and the knowledge providers, as for both of them this platform would be accessible anywhere around the world only a laptop and internet access will be sufficient to lean a new skill or provide yours.

#### Build Status:
There is a bug in the logout, as whenever a user logs in if he logs out the front-end crashes and you will have to re-run it again from the client (front-end) terminal using
```
$npm start
```
#### Code style:
Starndard style

#### Screenshots:
* Home
<div>
<img src="https://user-images.githubusercontent.com/104331757/214641967-46cf24d8-7a60-4724-9168-f7852dcd5eb8.png"width="300" height="150">
</div>


* Sign-in & Sign-up
<div>
<img src="https://user-images.githubusercontent.com/104331757/214640555-abe0ef02-ee3d-4dcd-9543-b820d1875245.png"width="300" height="150">
<img src="https://user-images.githubusercontent.com/104331757/214640998-b155d7ec-6dac-4066-95f0-1d74b7e014fc.png"width="200" height="150">
  </div>


  * Different panels

  <div>
  <img src="https://user-images.githubusercontent.com/104331757/214642872-22b06c4e-9fe5-4fcd-b9f0-b8fa981f7b46.png"width="300" height="150">
  <img src="https://user-images.githubusercontent.com/104331757/214642842-0bae9080-6299-4cdb-8528-a8401565fa3d.png"width="300" height="150">
  <img src="https://user-images.githubusercontent.com/104331757/214642904-4c5c7359-99aa-4d1b-b935-180c5c8c40f0.png"width="300" height="150">
  </div>

  #### Tech/Framework used :

The project was made using java-script with the following frameworks

For the front-end:
* Material ui for designing.
* Reactjs

for the back-end:
* Nodejs
* Express

for the database:
* Mongodb

#### Features:
The project simulates an online learning platform, Its very easy for the student to register for a course that they need also it's easy for the instructor to make courses with a set of different quizzes also students and give a certain feedbacks to keep the instructors updated if there were a probelm and whether the course is understandable.

#### Code Examples:

Most of the important features are included with a controller that deals individually with it like setting up a tutorials and quizzes and this is an example for deleting a lecture from setting up a tutorials and quizzes controller
```


export const deleteLecture = async (request, response) => {
  let Lecture;
  try {
      const Lecture = await Quiz.findById(request.params.id);
      
      await Lecture.delete()

      response.status(200).json('Lecture deleted successfully');
  } catch (error) {
      response.status(500).json(error)
  }
}

```

Also every model has different schemas like this one for the quizzes

```
const QuizSchema=new mongoose.Schema({
    title:{
        type: String,
    },
    name:{
        type :String,
    },
    avatar:{
        type:String,
    },
    cloudinary_id:{
        type:String,
    },
    classN:{
        type:String,
    },
    method:{
     type:String
    },
    tutorial: {
  
    
    },
    questionsTutorials:{
        type:Array,
    },
})
const Quiz=mongoose.model("Quiz",QuizSchema)
export default Quiz; 
```

#### Installation:

First of all you need to download VS-code using this link [vs-code](https://code.visualstudio.com/download) and then follow it's instructions to install

then you will need to download nodejs using this link [nodejs](http://nodejs.org/)


#### API reference:

You can find all API refernces in client (front-end) called api which mentions every route.

#### How to Use?
After installing the previous mentioned applications open vs-code then click on file then open folder then locate the folder that contains the project then click on select folder, then click ctrl+shift+E an explorer menu poped up at the very left of vs-code containing a folder with the project name and two sub folders called client and server right-click on each of them and click on open in integrated terminal a terminal should be opened

follow these steps when clicking open in integrated terminal for client folder :
Write the following the the terminal

```
$ npm install
$ npm start

```
and for the server folder write the following in the server terminal

```
$ npm install
$ node index.js
```
and now the project should be running on your local host.

#### Contribute:
Due the crash happenes in the log-out you can just send me suggestions on fixing it and other suggestions and extra features to be added using this email:emara99@gmail.com


#### Credits:
All credits goes to this amazing [Channel](https://www.youtube.com/channel/UCW5YeuERMmlnqo4oq8vwUpg)

#### License:

* Stripe
* For animation lottiefiles was used this is the link of it [lottiefiles](https://lottiefiles.com/).






















