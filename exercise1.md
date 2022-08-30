## Linting, testing, and building. What are the specific tools for taking care of these steps in the ecosystem of the language you picked? You can search for the answers by google.

I'm going to answer this questions for developing API with Python's Flask framework. For testing in this framework I'm going to use pytest, which is good enough for basic unit testing. For linting I'm going to use flake8, which is a common linting tool for Python. For building step, for Flask it is good to recommended to use *Wheel*, but I think serving using *Docker* is a better option too.

### What alternatives are there to set up the CI besides Jenkins and GitHub Actions? Again, you can ask google!

There is options like Atlassian's Bitbucket Pipelines, AWS CodePipeline, Gitlab CI and so on. All of them are cloud based CI/CD solutions, unlike Jenkins which is a local one. However, I think it is better to use GitHub Actions for CI/CD if the code repository is hosted on GitHub as it requires minimal setup. 


## Would this setup be better in a self-hosted or a cloud-based environment? Why? What information would you need to make that decision?

I still think it is better to use GitHub Actions for CI/CD if the code repository. For Python flask application, I think it is better to use Docker for building and testing. Docker is a good choice for building and testing because it is a lightweight containerization technology. The CI/CD pipeline can be setup so that the application is built and tested in Docker container through GitHub Actions which is a cloud based CI/CD solution allowing a Linux server to run the application. It will probably require Docker first to be installed inside the Linux machine on the cloud. 