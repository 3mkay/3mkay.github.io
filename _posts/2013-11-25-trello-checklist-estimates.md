---
title: Trello Checklist Estimate Totals
layout: post
published: true
permalink: article/trello-checklist-totals
excerpt: Display the total 'Scrum for Trello' estimates within checklists
comments: true
tags: Trello Estimation Tools
---
When performing [checkstimation](/thesaurus/checkstimation/) in Trello, you're less likely to split the card into manageable list items and spend time estimating when you know you've got to then add them all up by hand. One solution is to drag this to your bookmark bar, and give it a click once your lists are split and estimated:

<a href="javascript:(function()%7Bvar%20%24lists%3D%24(%22.checklist%22)%3B%24.each(%24lists%2C%20function(%20key%2C%20value%20)%20%7Bvar%20%24lName%20%3D%20%24(value).find(%22.checklist-title%20h3%22)%3Bvar%20%24lNameInput%20%3D%20%24(value).find(%22.checklist-title%20input%22)%3Bvar%20%24items%20%3D%20%24(value).find(%22.checklist-item%22)%3Bvar%20%24tot%20%3D%200%3B%24.each(%24items%2C%20function(key%2C%20value)%20%7Bvar%20%24itemText%20%3D%20%24(value).find(%22.checklist-item-details-text%22)%3Bvar%20%24itemEst%20%3D%20%24itemText%5B0%5D.innerText.match(%2F%5C(%5Cd%2B%5C.%3F%5Cd*%5C)%2Fg)%3Bif%20(%24itemEst)%20%7B%24itemEst%20%3D%20new%20Number(%24itemEst%5B0%5D.replace(%22(%22%2C%20'').replace(%22)%22%2C%20''))%3Bif%20(!isNaN(%24itemEst))%20%7B%24tot%20%2B%3D%20%24itemEst%3B%7D%7D%7D)%3B%24lNameUp%20%3D%20%24lName%5B0%5D.innerText.match(%2F%5E%5B%5E%5C(%5D*%2Fi)%3B%24lNameUp%20%2B%3D%20'%20('%20%2B%20%24tot%20%2B%20')'%3B%24lName%5B0%5D.innerText%20%3D%20%24lNameUp%3B%24lNameInput.val(%24lNameUp)%3B%7D)%7D)()">Checklist sum</a>

You can see a more readable version of the code on [this gist](https://gist.github.com/3mkay/7645300)