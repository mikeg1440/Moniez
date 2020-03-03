

<!-- PROJECT SHIELDS -->
[![Contributors][contributors-shield]][contributors-url]
[![Forks][forks-shield]][forks-url]
[![Stargazers][stars-shield]][stars-url]
[![Issues][issues-shield]][issues-url]
[![MIT License][license-shield]][license-url]
[![LinkedIn][linkedin-shield]][linkedin-url]



<!-- PROJECT LOGO -->
<br />
<p align="center">
  <a href="https://github.com/mikeg1440/Moniez">
    <img src="https://github.com/mikeg1440/Moniez-Frontend/blob/master/src/images/moniez-green-logo.png" alt="Moniez Logo" width="80" height="80">
  </a>

  <h3 align="center">Moniez</h3>

  <p align="center">
    A personal budgeting application with a Ruby on Rails API back end and a React.js front end
    <br />
    <a href="https://github.com/mikeg1440/Moniez">View Demo</a>
    ·
    <a href="https://github.com/mikeg1440/Moniez/issues">Report a Bug</a>
    ·
    <a href="https://github.com/mikeg1440/Moniez/issues">Request Feature</a>
  </p>
</p>



<!-- TABLE OF CONTENTS -->
## Table of Contents

* [About the Project](#about-the-project)
  * [Built With](#built-with)
* [Getting Started](#getting-started)
  * [Prerequisites](#prerequisites)
  * [Installation](#installation)
* [Usage](#usage)
* [Roadmap](#roadmap)
* [Contributing](#contributing)
* [License](#license)
* [Contact](#contact)
* [Acknowledgements](#acknowledgements)



<!-- ABOUT THE PROJECT -->
## About Moniez

[![Moniez Dashboard Screen Shot][product-screenshot]](https://github.com/mikeg1440/Moniez-Frontend/blob/master/src/images/dashboard-screenshot.png)

Moniez is a simple budgeting application that allows users to create multiple budgets and input earnings, bills, and expenses.  Each budget category has its own view where existing entries are sorted from largest to smallest amount and users can add new entries or delete existing ones.  After a user has populated any of the budget categories the dashboard will display a pie chart that breaks down each category in terms of percentage and dollar amount for better comparison.  Each user has their own account that is password protected for data privacy.

### Built With

* [React.js](https://reactjs.org/)
  * [Recharts](http://recharts.org/en-US/)
  * [react-router-dom](https://www.npmjs.com/package/react-router-dom)
  * [Redux](https://redux.js.org/)
  * [Redux-Thunk](https://github.com/reduxjs/redux-thunk)
* [Ruby on Rails](https://rubyonrails.org/)
  * [PostgreSQL](https://www.postgresql.org/)
  * [Simple Token Authentication](https://github.com/gonzalo-bulnes/simple_token_authentication)
  * [Active Model Serializers](https://github.com/rails-api/active_model_serializers)


<!-- GETTING STARTED -->
## Getting Started

To get a local copy up and running follow these simple steps.

### Prerequisites

This is a list of software that you will need to get Moniez up and running.

* [npm](https://www.npmjs.com/get-npm) (Updated to latest ->  `npm install npm@latest -g`)
* [Ruby on Rails >= 2.6.1 installed](https://www.tutorialspoint.com/ruby-on-rails/rails-installation.htm)
  * [Bundler](https://bundler.io/)
* [PostgreSQL](https://blog.timescale.com/tutorials/how-to-install-psql-on-mac-ubuntu-debian-windows/)

### Installation

### Backend API
1. Clone the https://github.com/mikeg1440/Moniez
```sh
git clone --recursive https://github.com/mikeg1440/Moniez.git
```
  ** NOTE ** If you forget the `--recursive` option when cloning the repo you can pull down the front and back end repos by running `git submodule update --init` and that will pull each repo

2. Change to the `Moniez-Backend` folder
3. Run `bundle install` to install gems
4. [Configure PostgreSQL](https://medium.com/coding-blocks/creating-user-database-and-adding-access-on-postgresql-8bfcd2f4a91e) and add credentials to back end (either with [encrypted credentials](https://mikeg1440.github.io/2020/02/12/configure-rails-with-postgresql-using-encrypted-credentials/) or a gem like [DotEnv](https://github.com/bkeepers/dotenv))
  * The project is set up with rails encrypted credentials and is already configured to look for the database username and password in the following format in the credential store, so you must enter those in first (refer to link above for details on how to edit the encrypted credentials)
  ```
  database:
      username: [YOUR DB USERNAME]
      password: [YOUR DB PASSWORD]  
  ```
  * Since the project is using rails credentials store if you want to use some other way to handle credentials like with the dotenv gem then you need to change the `config/database.yml` file to grab the username and password from where ever you stored the information instead of the rails encrypted credential store.
  * Make sure the database is already running, on Debian/Ubuntu systems `systemctl status postgresql`.  If it does not show the `postgresql.service` as `active` then you can run the following to start it, `systemctl start postgresql`.
5. Run `rails db:setup` to create database and run migrations
6. Finally to run the API server run `rails s`

### Frontend Interface
1. Change to the `Moniez-Frontend` folder
2. Install NPM packages `npm install`
3. ##### `yarn start`
  Runs the app in the development mode.<br />
  Open [http://localhost:3000](http://localhost:3000) to view it in the browser.

4. ##### `yarn build` to build the application (not needed for development)
  Builds the app for production to the `build` folder.<br />
  It correctly bundles React in production mode and optimizes the build for the best performance.


<!-- USAGE EXAMPLES -->
## Usage

This can be useful for people looking to get an idea of where their money is going and how to best cut expenses so you can save as much as possible.  Users have the option of putting entering lists of Earnings, Expenses, and Bills that will then be calculated to show either how much money your left with to save or how much you r over spending by.  Each budget when selected is also rendered as a circle pie chart with each category displayed to get a better idea of how even or uneven your budget categories look.



<!-- ROADMAP -->
## Roadmap

See the [open issues](https://github.com/mikeg1440/Moniez/issues) for a list of proposed features (and known issues).



<!-- CONTRIBUTING -->
## Contributing

Contributions are what make the open source community such an amazing place to be learn, inspire, and create. Any contributions you make are **greatly appreciated**.

1. Fork the Project
2. Create your Feature Branch (`git checkout -b feature/AmazingFeature`)
3. Commit your Changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the Branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request



<!-- LICENSE -->
## License

Distributed under the MIT License. See `LICENSE` for more information.



<!-- CONTACT -->
## Contact

Michael Gaudreau - [@MyLogicBytes1](https://twitter.com/MyLogicBytes1) - cyberct@kbox.li

Project Link: [https://github.com/mikeg1440/Moniez](https://github.com/mikeg1440/Moniez)



<!-- ACKNOWLEDGEMENTS -->
<!-- ## Acknowledgements

* []()
* []()
* []() -->





<!-- MARKDOWN LINKS & IMAGES -->
<!-- https://www.markdownguide.org/basic-syntax/#reference-style-links -->
[contributors-shield]: https://img.shields.io/github/contributors/mikeg1440/Moniez.svg?style=flat-square
[contributors-url]: https://github.com/mikeg1440/Moniez/graphs/contributors
[forks-shield]: https://img.shields.io/github/forks/mikeg1440/Moniez.svg?style=flat-square
[forks-url]: https://github.com/mikeg1440/Moniez/network/members
[stars-shield]: https://img.shields.io/github/stars/mikeg1440/Moniez.svg?style=flat-square
[stars-url]: https://github.com/mikeg1440/Moniez/stargazers
[issues-shield]: https://img.shields.io/github/issues/mikeg1440/Moniez.svg?style=flat-square
[issues-url]: https://github.com/mikeg1440/Moniez/issues
[license-shield]: https://img.shields.io/github/license/mikeg1440/Moniez.svg?style=flat-square
[license-url]: https://github.com/mikeg1440/Moniez/blob/master/LICENSE.txt
[linkedin-shield]: https://img.shields.io/badge/-LinkedIn-black.svg?style=flat-square&logo=linkedin&colorB=555
[linkedin-url]: https://linkedin.com/in/michael-gaudreau
[product-screenshot]: https://github.com/mikeg1440/Moniez-Frontend/blob/master/src/images/dashboard-screenshot.png
