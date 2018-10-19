# hiring-docker
Dockerfiles to use for verifying candidates' hiring assignments

## How to use
For example:

Go to the folder with your chosen dockerfile:

`cd j8pure`

Build the image:

`docker build . --tag hiring`

Run it, mounting the candidate's repo folder:

`docker run -it --mount type=bind,source=/<insert-your-path>/zofia_iksinska,target=/app hiring`

You might also need to expose the app's port:

`docker run -it --mount type=bind,source=/<insert-your-path>/zofia_iksinska,target=/app -p 4567:4567 hiring`
