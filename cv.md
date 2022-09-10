# Ilya Navumenka

## Contacts:
 >ICloud: ilyanavumenka@icloud.com

 >Telegram: @ilyanavumenka

 >[LinkedIn](https://www.linkedin.com/in/ilyanavumenka/)

---

## Task:

 To acquire knowledge and experience in frontend/javascript development for making perspective carrier and be professional in this field.

---

 ## Briefly About Myself:

 Hello, I am a Front End developer with knowledge of various development tools.

 For the last 4 years I have studied as a software engineer-economist. As a result, I chose the direction of Front-End development and really want to apply my skills to commercial projects.
 
 Very interesting in working with creative teams who are going to create something new and wonderful, working in a comfortable team-oriented environment.

---

## Skills and Proficiency:

 * HTML5, CSS3
 * Basic knowledge of languages: JS, Node.js
 * MongoDB, PostgreSQL, Microsoft SQL Server
 * Git, GitHub
 * VS Code
 * Adobe Photoshop, Figma

 ---

 ## Code example:

 Some part of my Telegram bot, which is written using the Node.js software platform

```js
const UUID_V4 = require('uuid/v4');

const WEEKDAYS = ["Sunday", "Monday", "Tuesday", "Wednesday", "Thursday", "Friday", "Saturday"];
const GAMES = ["Football", "Volleyball", "Basketball", "Tennis", "Hockey"];
const EVENT_TIME_REGEXP = /^(0[0-9]|1[0-9]|2[0-3]|[0-9]):[0-5][0-9]$/g;

let eventParser = function (ctx) {
    console.log("TEXT", ctx.message.text);
    if (!ctx.message.text) {
        return false;
    }

    if(ctx.message.chat.type === "private") {
        ctx.message.text = ctx.message.text.replace("/addevent","").trimStart();
    }

    console.log("CTX", ctx);
    console.log("message", ctx.message);



    let eventDetails = ctx.message.text.split(' ');
    console.log("EVENT DETAILS", eventDetails);
    let eventType;
    let eventDay;
    let eventTime;

    eventDetails.forEach((value) => {
        if (WEEKDAYS.includes(value)) {
            eventDay = value;
        }
        if (GAMES.includes(value)) {
            eventType = value;
        }
        if (EVENT_TIME_REGEXP.test(value)) {
            eventTime = value;
        }
    });

    if(eventDay && eventTime && eventType) {
        let event = {
            _id: UUID_V4(),
            username: ctx.message.from.is_bot ? "BOT" : ctx.message.from.username,
            user_id: ctx.message.from.id,
            timestamp: new Date(ctx.message.date),
            details: {
                type: eventType,
                day: eventDay,
                time: eventTime
            }
        };
        return event;
    } else {
        return false;
    }

};

module.exports = eventParser; 
```

---

## Courses:

* [JS/FE PRE-SCHOOL 2022 (JAVASCRIPT)](https://app.rs.school/certificate/da2ojvq5)

* [HTML&CSS. Beginner](https://www.linkedin.com/in/ilyanavumenka/details/featured/1635470770161/single-media-viewer/)

* [Programming basics. Beginner](https://www.linkedin.com/in/ilyanavumenka/details/featured/1635470764865/single-media-viewer/)

* [Basics of JavaScript programming](https://www.linkedin.com/in/ilyanavumenka/details/featured/1635470769396/single-media-viewer/)

* [JavaScript. Beginner level](https://www.linkedin.com/in/ilyanavumenka/details/featured/1635470769400/single-media-viewer/)

* [HTML course](https://www.linkedin.com/in/ilyanavumenka/details/featured/1635470770300/single-media-viewer/)

* [CSS course](https://www.linkedin.com/in/ilyanavumenka/details/featured/1635470769523/single-media-viewer/)

* [JavaScript course](https://www.linkedin.com/in/ilyanavumenka/details/featured/1635470766903/single-media-viewer/)

* [jQuery course](https://www.linkedin.com/in/ilyanavumenka/details/featured/1635470772442/single-media-viewer/)

---

## Languages:

* Belarusian (Native language)
* English (Pre-Intermediate)
* Russian (Native speaker)

---

## Education:
International university "MITSO", software engineer-economist