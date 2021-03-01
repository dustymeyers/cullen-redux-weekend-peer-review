# Weekend Challenge 11 - React-Redux Feedback Form

## Instructions

Reviewing code is an important role developers play. We're going to practice reviewing code from others.

- Get the repo url from your partner
- Get your partner's project running on your computer
- Review the code from your partner and give relevant feedback
- Complete the Markdown section and submit that in the notes section on the assignment app. (Make sure you include who's code you reviewed.)

Practicing compassionate code reviews is important (you can learn more from this video on the topic: https://www.youtube.com/watch?v=Ea8EiIPZvh0 )

## Review Checklist

## Base Required Features 

- Multi-Part Form:  
  - [x] Able to add feedback
    - [x] Data collected on individual pages & components
    - [x] Click on next takes you to the next page in sequence
    - [x] Data saves in DB after *all* the parts are completed (not piecemeal)
    - [x] Thank you page takes you back to the first view
    - [x] Old Data is cleared on form completion

- Client code:
  - [x]  Individual components for each form part
  - [x]  Redux setup complete
    - [x] Store linked to react with `<Provider>`
    - [x] Store setup with reducer(s) and logger middleware 
  - [x] Reducers & Actions Working
    - [-] Actions are in SCREAMING_SNAKE_CASE and semantically named
    - [x] Actions have a `type` key, and `payload` if sending data
    - [x] Reducers are returning a new state, or the old state (not mutating)
    - [x] Reducers are using spread correctly (to keep old data, while adding new)
  - [x] Review Component shows at all times with current redux state
  - [x] React-Redux Working
  - [x] Axios POST request to add feedback


- Server code:   
  - [x] Router made for GET, POST


## General Items
Feedback should be provided for these items, but they do not impact scoring.

- Git 
  - [x] Multiple git commits showing incremental progress
  - [x] Commits are descriptive of the changes made or feature added 
  - [x] Has .gitignore with node_modules
  - [x] Readme file updated (assuming this is previously discussed)
- Code Style 
  - [-] Appropriate amount of code comments
  - [-] Code is consistently formatted
- Client
  - [x] Appropriate use of HTML tags
  - [x] Basic CSS styling with margins/padding


## Stretch Goals
First must be complete for score of _5 - Exceeds Expectations_

- Previous Steps
  - [x] allows a user to go to a previous step, either directly or by cycling backward thru the steps
  - [x] user can upate their score for a step
    - [x] new score is validated to not be empty
    - [x] redux is updated with new score
  - [x] user can continue on to review page and submit as in Base Mode


- Admin View
  - [x] All entries are visible with correct data from inputs
    - [x] Most recent is at the top
  - [x] Can Delete an entry
    - [x] User is prompted before deleting
  - [x] Axios GET request to get all feedback for `/admin` view in componentDidMount

  Busywork Goals, consider removing or making more useful

- [x] Styling with Material UI
- [ ] Ability to flag a feedback item on `/admin` for further review
- [x] Deployed to Heroku


## Markdown

```
Hey Alvin,

Great work with this weekend's assignment! It shows that you've got a great foundation for your understanding of react and redux and how to implement third-party libraries into your applications. 

---
| Functional Requirements | Complete |
| --- | :---: |
| Multi page form with client side routing and navigation (next button) | yes |
| Data stored in Redux when navigating from page to page | yes |
| User is notified when trying to leave a blank score | yes |
| Review Component displays scores and comments from current redux state | yes |
| Submit button sends data to the server via Axios | yes |
| Confirmation Page displays after data is POSTed to the server | yes |
| Button on Confirmation Page clears Redux and starts a new survey | yes |
| Views are broken down into components | yes |

---
### Notes:

This is looking really great, Alvin! I'm not really sure why your Flagging doesn't seem to work. I attempted to alter your SQL text to what I had and it still didn't seem to do much. I'd suggest putting in more console.logs along the way so it's a little easier to dig through that. But besides that, I think everything works swimmingly. The only other detail that I might consider thinking about when using actions to set your reducer state, would be to make them just a little more descriptive of what they are doing. ei `SET_FEELING_SCORE` or even `SET_FEELING`. Overall though, the variable names you choose to use are pretty self explanatory!

---
| General Items | Complete? |
| --- | :---: |
| More than 15 git commits | yes |
| Commits are descriptive of the changes made or feature added | yes |
| Readme file updated | yes |
| Appropriate amount of code comments | no |
| Code is consistently formatted | no |
| Server code organized with router & module files | yes |

---
### Notes:

Notes on General Items

Seriously, great working app here, despite that one flagging issue. You've got a few comments here and there from component to component, but there doesn't seem to be much consistency with each comment. Most things a reader could parse out, but maybe using comments consistently to label your imports, different html components in you JSX (especially when you use a different kind of syntax that might be provided by a third-party library). I find it's helpful to dedicate some time to reviewing each component just to make sure my formatting is readable. It can help over all when you are trying to use a turnery to render inside your jsx. Overall, though you don't have a lot of excess code and the current formatting doesn't make it confusing to look at! Great work!
