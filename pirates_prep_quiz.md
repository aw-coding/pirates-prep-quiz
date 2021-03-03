# React Requests - Pirate API Quiz



Question 1

Which component is responsible for requesting all the pirates?

--- PirateContainer.js


Question 2

Which hook do we use to carry out the requestAll() method and when does it get triggered?

--- useEffect. It is triggered only once, when the application is initially rendered (hence the empty array).


Question 3

The requestAll() method creates a new instance of Request in order to gain the functionality to carry out various forms of request. Where is the Request class?

--- It is located in the helpers directory (request.js)

Question 4

Which method are we using from the Request class here?

---get

/Users/user/codeclan_work/week_14/day_3/hw/pirates_prep_quiz.md


Question 5

The PirateList component is in charge of rendering a list of pirate components. What is the pirateNodes function returning?

--- a pirate component (per pirate from the server's DataLoader)


# Viewing a Single Pirate


Question 1

In the browser, when we click on one of the pirates names in the pirate list, our app renders a PirateDetail component. PirateDetail is in charge of rendering the information for a single pirate. But where is it getting its props passed down from?

--- pirate.js


Question 2
 ```js
 if (!pirate){
  return "Loading..."
}
 ```
What is the purpose of this code in PirateDetail?

--- this replaces any details about a pirate while the data is being fetched.


Question 3

In PirateDetail, to delete a pirate, we have a button with a listener "onClick" which triggers a function called "handleDelete". The handleDelete function uses a function onDelete. Where is it receiving onDelete from?

--- near the top of PirateDetail: 

  const handleDelete = () => {
    onDelete(pirate.id)
  }


# Bonus Points Questions


Question 1

In PirateContainer, what does Promise.all return?

--- it turns piratePromise, shipPromise and raidPromise into a single promise, which will return an array of the promised data.


Question 2

Ideally, we want our state to live at the top of our component chain, except in one other scenario. This is when our component contains a, what?

--- a fetch from an api (so the resulting data can only exist where it is needed- the single responsibility principle)
