
# GPSMobileTrackingApp
Before we start, Please make sure you have latest version of node js installed.<br/>
Let's head out to https://nodejs.org/en/ and grab latest nodejs.<br/>
Once you have nodejs installed, open command prompt/terminal window.<br/>
$ node -v // make sure, this command comes back with a node version<br/>
$ npm -v // make sure, this command comes back with a npm version<br/><br/>

$ npm install -g @angular/cli<br/>
$ mkdir app<br/>
$ cd app<br/>
$ mkdir client<br/>
$ mkdir server<br/>
$ cd client<br/>
$ ng new GPS-Mobile-Tracker<br/>
$ cd GPS-Mobile-Tracker<br/>
$ ng serve<br/>

<h2>Back end :-</h2>
$ cd server<br/>
$ npm init<br/>
$ npm install --save nodemon cors express dotenv jsonwebtoken mysql bcrypt body-parser<br/>
$ nodemon app

MYSQL Tables
--
-- Table structure for table `user`
-- 
CREATE TABLE `user` (
  `name` varchar(30) NOT NULL,
  `email` varchar(50) NOT NULL,
  `password` varchar(300) NOT NULL,
  `question` varchar(100) DEFAULT NULL,
  `answer` varchar(100) DEFAULT NULL,
  `createdAt` datetime NOT NULL,
  `updatedAt` datetime NOT NULL,
  PRIMARY KEY (`email`)
) ENGINE=MyISAM DEFAULT CHARSET=latin1;

--
-- Table structure for table `usergps`
--

CREATE TABLE `usergps` (
  `email` varchar(100) NOT NULL,
  `lat` varchar(10) NOT NULL,
  `long` varchar(10) NOT NULL,
  `createdAt` datetime NOT NULL,
  PRIMARY KEY (`email`,`createdAt`)
) ENGINE=MyISAM DEFAULT CHARSET=latin1;
