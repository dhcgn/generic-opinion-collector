# Planning

## First Steps

#### Web Backend

This is the backend for the users who wants to create and manage campaings.

Feautures:

- With click of a button a campaing can be created
  - Name of the campaing is required
- A link and a Qr-Code are created for the campaign and show on the website
- All campaings can be listed on the website

#### API Backend

This is the API which can be used to get the data from the campaings and import it into own systems.

Feautures:

- there is a postman collection with all the rest call to the API
- All data can be retrieved with a GET call

#### Web Frontend

This is the frontend for the users who wants to give feedback to the campaings.

Feautures:

- The campaing link can be visited and the user can give 1-5 stars to the campaing and has the option to leave a comment
- The is a link created to delete your data, this can be called and there is only a confirmation needed to delete the data

#### Implementing Details

- For web, plain HTTP, CSS, JS are used
- Persisiing data is done with a JSON file
- the code strucutre is done with speration of concerns and the single responsibility principle, and interfaces are used to make the code more flexible and testable
- Pipelines (or Hithub Actions) are used to build and test the code
