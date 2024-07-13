# Planning

## First Steps

#### Web Backend

Feauter Set

- With click of a button a campaing can be created
  - Name of the campaing is required
- A link and a Qr-Code are created for the campaign and show on the website
- All campaings can be listed on the website

#### Web Frontend

- The campaing link can be visited and the user can give 1-5 stars to the campaing and has the option to leave a comment
- The is a link created to delete your data, this can be called and there is only a confirmation needed to delete the data

#### Implementing Details

- For web, plain HTTP, CSS, JS are used
- Persisiing data is done with a JSON file
- the code strucutre is done with speration of concerns and the single responsibility principle, and interfaces are used to make the code more flexible and testable
- Pipelines (or Hithub Actions) are used to build and test the code