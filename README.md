
//creating nested header element using React.Element(h1,h2,h3 inside div with class="title")
const header= React.createElement(
  "div",
  {
    className: "Title",
  },
  [
    React.createElement(
      "h1",
      {},
      "This is h1 Tag"
    ),
    React.createElement(
        "h2",
        {} ,
        "This is h2 Tag"
      ),
      React.createElement(
        "h3",
        {},
        "This is h3 Tag"
      )
  ]
);
//creating sample element using jsx
consts header= (
  <div className="Title" key="title">
    <h1 key="h1">This is h1 tag</h1>
    <h2 key="h2">This is h2 tag</h2>
    <h3 key="h3">This is h3 tag</h3>
  </div>
);
//creating functional component of the same with jsx
const Header = () => {
  return (
    <div className="Title" key="title">
      <h1 key="h1">This is h1 tag</h1>
      <h2 key="h2">This is h2 tag</h2>
      <h3 key="h3">This is h3 tag</h3>
    </div>
  );
};
//passing attiribute into the tag in jsx
const Header = () => {
  return (
    <div className="Title" key="title">
      <h1 style={{color:"blue"}} key="h1">This is h1 tag</h1>
      <h2 style={{color:"palevioletred"}} key="h2">This is h2 tag</h2>
      <h3 style={{color:"green"}} key="h3">This is h3 tag</h3>
    </div>
  );
};

//Composition of Component (Add a component inside another)
const AnotherComponent = function(){
  return <h2> This is Another Component</h2>
}

const Header= () => {
return (
  <div className="Title" key="title">
    <h1 style={{color:"blue"}} key="h1">This is h1 tag</h1>
    <h2 style={{color:"palevioletred"}} key="h2">This is h2 tag</h2>
    <AnotherComponent/>
    <h3 style={{color:"green"}} key="h3">This is h3 tag</h3>
  </div>
);
};
//{TitleComponent} vs {<TitleComponent/>} vs {<TitleComponent></TitleComponent>} in JSX.

const element = <h1>This is React Element</h1>; // This is React element or {TitleComponent}

const TitleElement = () => {
  return <h2 style={{ color: "red" }}>This Title Element</h2>;
}; // This is Title Component

const i = () => {
  return (
    <div className="Title" key="title">
      {/* This is {TitleComponent} */
      /*{element}
      <h1 style={{ color: "blue" }} key="h1">
        This is h1 tag
      </h1>
      {/* This is {<TitleComponent/>} */
      <TitleElement/>
      <h2 style={{ color: "palevioletred" }} key="h2">
        This is h2 tag
      </h2>
      //{ This is {<TitleComponent></TitleComponent>}}
      <TitleElement></TitleElement>
      <h3 style={{ color: "green" }} key="h3">
        This is h3 tag
      </h3>
    </div>
  );
};
/*Create a Header Component from scratch using Functional Component with JSX
Add a Logo on Left
Add a search bar in middle
Add User icon on right
Add CSS to make it look nice*/
const t = () => {
    return(
        <>
        <header className="header">
            <div className="left">
                <img src={logo} alt="Logo" />
            </div>
            <div className="center">
                <input className="input" type="text" placeholder="Search anything you want..."/>
                <button type="submit">Submit</button>
            </div>
            <div className="right">
                <img src={userIcon} alt="User Icon"/>
            </div>
        </header>
        </>
    )
}