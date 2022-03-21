#  REACT JS
## React learning path;

Four types of components in React;
1. Similar in look but different in data.
2. Container components where one or more similar components are contained in border catagory.
3. keeping components in beakdown system for sakeness of work in website.
 Example : left site or right side of a page.best example in www.thejsdude.com(right side) and left side in www.youtube.com in desktop.
4. alone components not like the above components e.g. footer section or header section is stand alone component.

SIngle Page application(SPA) vs Multi Page application(MPA)

1.SPA --Quick Loading time but MPA - slow Loading time.
2. Uses Less Bandwidth but MPA-  more Bandwidth.
3.SPA has Seamless/ good User Experience but MPA - less good User Experience.
4. SPA is something securtiy essue  but MPA - has securtiy strong.
5. SPA Doesn't Perform well with SEO but MPA - Performs well with search Engine Optimization.

// Single Page application has a ROUNTING option .Depending on Routing , We can see the option of Page.
it enables the navigation among views of various components in a React Application, allows changing the browser URL, and keeps the UI in sync with the URL.

// Attributes vs properties.
actually The Attributes used in html are named properties in using for javscript.suppose dom properties but html Attributes title, id, href.

// properties calls as PROPS in React.

// user can change STATE in web app(React state). if user interact in app , state can be changed.if totally depends on user. If He doesn't change state, Suppose visiting in app ,he doesn't apply any react like in facebook.add to card in ecommerce is a state changing example.to Wrap up, Web Application data that could be changed.

# 6 Core Concepts of ReactJS to UnderStant Easily

1.JSX == Javacript objects.It is system for writing html.its Babble takes html codes and convert it to javscript.
we can use style in 3 ways internal , external and inline in JSX.(app.js). JSX(Javacript Xml)

// JSX----

// 2. useState() // used for creating new state in website like increasing product count or add to product.It has [] empty array with 2 elements . one is counter value and the other is function for the counter. So we can destructering 

this array const [count, SetCount] = useState()

and afftecting for this state useEffect(arrow function , array[]) with these two parts

///

const ExternalUsers = ()=>{

  const [users, setUsers] = useState([]) 
  useEffect(()=>{
    fetch('https://jsonplaceholder.typicode.com/users')
    .then(res => res.json())
    .then(resData => setUsers(resData))
  }, 
  
  []);

///

/// 3. components
/// 4. Props.(Attributes for HTML but properties for React)
/// 5. Dynamic creating function <functionNme></functionNme>
/// 6. Events

 return result with (

)

 import logo from './logo.svg';
import './App.css';

const myInfo = {name:'Mahmodul Karim', age: 27, graduate: 'Masters'}
const {name, age, graduate} = myInfo;
const myPhoneNumber = '0164721332';
const myWorking = 'Learning Programming';
const myaddress = 'Lalbag Thana, Dhaka South Area, code-1381';

const myWorkingStyle ={
  color:'violet',
  backgroundColor:'#61dafb',
  padding:'20px',
  margin : '10px'
}

function App() {
  return (
    <div className="App">
      <header className="App-header">
        <img src={logo} className="App-logo" alt="logo" />

    <h1>JSX</h1>
    <p className='welcomeMsg'>Hellow Dude , React , How R You</p>
    <h3>Name : {name}</h3> <span>{graduate}</span>
   <p style={{color:'black', backgroundColor:'yellow'}}>My Contact Number : {`+88-${myPhoneNumber}`}</p>
   <p>My Learning Way : {myWorking}</p>
   <address>My Location : {mydress}</address>


        <p style={myWorkingStyle}>
          Edit the source <code>src/App.js</code> and save to reload.
        </p>
        
      </header>
    </div>
  );
}

export default App;


---- creating new Folder name component in src folder.Then js , css and other working files including here.
(Code Runner
)
(
  Code Spell Checker


)
two important extension of VS code.

// React extension pack for shortcut snippet , such as rsc mean full function with name and export.


// creating a React component like from API
Methods Here : 1. useState([]) ,

 2. useEffect( () =>{}, [])

 3. Fething data in the useEffect arrow function.

4. working with map or others in return(
  <div> 
  </div>
  and calling here the fucntion that used to show data
)

5. Makeanother function to show data easily and clearly with giving properties that used in main function html tag Attributes inside(e.g. name) these < name= {}> </>.

// Properties(html tag in js) can be taken in a variable to use direct function . no need to use propeties one by one in calling function <></> in this ways. 

example 

 {
               EachCountry.slice(0,20).map(EachCountryData  => <Country // best way this to use all props.
                country_data = {EachCountryData}
               
                //  CountryName = {EachCountryData.name.common} |
                //  Population = {EachCountryData.population}    | all these previous sytem to use properties
                //   Area = {EachCountryData.area}

               ></Country>)
               
           }

           more useful system .
           example by using directly destructering 


Example Here :

const Country = (props) => {
    const {name:{common},area, population} = props.country_data;
    return (
        <div>
            <h4 className='countryStyle'>Country name : {common}</h4>
            <h5>Population : {population}</h5>
            <h6>AREA : {area}</h6>
        </div>
    );
};
           
           and finally the best way to use and call the propeties

// React app to deploy in netlify -- npm run build writing in VS Code terminal or cmd.then After every updates , npm run build is mandatory to write in terminal.it will build in same project folder in my app.

// To use Bootstrap in React , run in terminal "npm install react-bootstrap bootstrap@5.1.3" . to get latest version go to "https://react-bootstrap.github.io/getting-started/introduction/"

// properits can be sent One folder js file to another folder by calling props that is Attributes in another folder.

Example ===  App.js --- Menubar.js(child of src) --- Test.js(child of src) 
app.js ---   <Menubar inCreament={counter} Decrement={decreCounter}

></Menubar> (import Menubar from './Components/Menubar/Menubar';)

Menubar.js ---  <Test Increasing={inCreament}  decreasing = 

{Decrement}></Test> (import Test from '../Tests/Test';)

Test.js ---<button className='ms-3 p-3' onClick={Increasing}>+</button>

    <button className='ms-3 p-3' onClick={decreasing}>-</button>

    /// NPM is a Package manager that works for run, start, play and functionals.NMP Is a full Package manager give us a Package with many features for Creating React APP.

     /// NPX--- Node Package Execute ,it comes with npm.It works together NPX and NPM.

    /// creat-react-app is a one type of command line interface for creating react APP.it give up huge facilities like npm start, run build.We find full setup by installing it.Such as mode_modules, .git , build, .gitignore , README.md, src folder with its files and other built-in itself.

    ///JSX(Javascript XML) html codes are written smoothly in js fil and js expressions are also written easily in html inside Curely brackets {}.So JSX is a syntectic sugar system.

    /// Unidirectional(One way binding) --- parent to child , and child to its  child sending data of the components.Like App.js ---to---allProduct.js ---- everyproduct.js(by properties/props)

    /// Usestate update value with the second array (like SetCount) it is asyncrounous system. First array(Count) will not execute the true value in function calling , it is updating as a asyncrounous.for getting the latest value instantly use --- useEffect or settimeInterval.State is updated asyncrounously.
    useEffect(() => {
      console.log(count)
    }, [count])

    /// calling the count arrray in dependency here [] -- we will get the latest value instantly.That means to get syncrounously must use useEffect for state.it change asyncrounous to syncrounous way.
     
     "  HOOK is  a special function of react to  implement react functionality to optimize codes. such as Usestate , useEffect, useref and other ".
     Usestate() count([first array]) can be sent to componen to component by Props.
     where found Usestate(), it callled be a statefull componet or Presentional component.

     /// " Be remember that props can not change/ read only but not write only"

     /// "REACT WORKS IN VIRTUAL DOM means that We want to change anything in components so, it becomes hard and tough. That's why React keeps a virtual DOM whenever want to change WE can do it easily".Think of your HTML code as a tree. In fact, that is exactly how the browser treats your DOM (your rendered HTML on the browser). React allows you to effectively re-construct your DOM in JavaScript and push only those changes to the DOM which have actually occurred. 

     follow the link to understand easily  https://www.freecodecamp.org/news/react-under-the-hood/

to wrap up, React will keep VIRTUAL DOM and Brower will have Brower DOM. React developer can change any thing easily in VIRTUAL DOM by creating a DOM to compare the Broweser DOM.in this, We need add "key" in tag.


VIRTUAL DOM works here index.js file of src folder.

 ReactDOM.render(
  <React.StrictMode>
    <App />
  </React.StrictMode>,
  document.getElementById('root')
);


<ul>
    <li key="A">A</li>
    <li key="B">B</li>
</ul> 
from it to change 
 <ul>
    <li key="Z">Z</li>
    <li key="A">A</li>
    <li key="B">B</li>
</ul>   

     ///  componet lifecycle.

     /// not found './' this while importing means that import from node odules. 
     E.G. './products.css' it is custom designed by us not from node modules.
     node modules folder has a react folder name 'react' from where we find meny files for importing in react files.

          /// COMPONENT function WORKS can be Export default jsdk() and in the component I want to props the export component, must add in head import, import the file.

          /// we send the function/component like this.here no need to import anything from react

           export {Show, AnotherBrand, Myshow}

           parent function /component behaviour like this : 

           import React from 'react';
import { AnotherBrand, Myshow, Show } from './CasualItems/Items';

const Cosmetics = () => {
  let showBrand = 'Bata';
  let showprice = 1790;   
  const reulst = Myshow(showBrand, showprice)
    return (
        <div>
            <Show></Show> <br />
            <AnotherBrand></AnotherBrand> <br />
            <p>show information i s; ${reulst}</p>
        </div> )};
export default Cosmetics;

/// Json generator follow the link https://json-generator.com/

/// creating a json file in public folder name.json means .json file, we can fetch it by locally.

/// to import file from many inner folders to parent folder ../../../../ we have go in this way. but same folder ./ that's it.

/// 3 way to access object suppose : var obj = {} --- obj.name, obj{'name'} and the other obj[id]

/// remeber that -- When the property name is dynamic or is not a valid identifier, a better alternative is square brackets property accessor: object[propertyName]. 

The first expression should evaluate to an object and the second expression should evaluate to a string denoting the property name.

 Here's an example:

const property = 'name';
const hero = {
  name: 'Batman'
};
// Square brackets property accessor:
hero['name'];   // => 'Batman'
hero[property]; // => 'Batman'

to learn more follow the link  https://dmitripavlutin.com/access-object-properties-javascript/ .

/// offtopic --- event.preventdefault() is used in form submitting function to save us from reload repeatedly while submitting .

to know more follow the link here   https://youtu.be/2KlBKrt_GMQ

/// to know more details about Locl storage add item and delete follow the link : https://youtu.be/Ci1vQWFzz-g
    
    