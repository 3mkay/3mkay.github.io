---
title: Trello Checklist Estimate Totals
layout: post
published: true
permalink: article/trello-checklist-totals
excerpt: Display the total 'Scrum for Trello' estimates within checklists
comments: true
---
When performing [checkstimation](/thesaurus/checkstimation/) in Trello, your less likely to split the card into manageable list items and spend time estimating when you know you've got to then add them all up by hand. One solution is to drag this to your bookmark bar, and give it a click once your lists are split and estimated:

<a href="javascript:var%20%24lists%3D%24(%22.checklist%22)%3B%24.each(%24lists,function(key,value)%7Bvar%20%24lName%3D%24(value).find(%22.checklist-title%20h3%22)%3Bvar%20%24lNameInput%3D%24(value).find(%22.checklist-title%20input%22)%3Bvar%20%24items%3D%24(value).find(%22.check-item-text%22)%3Bvar%20%24tot%3D0%3B%24.each(%24items,function(key,value)%7Bvar%20%24itemText%3D%24(value).find(%22.current%22)%3Bvar%20%24itemEst%3D%24itemText%5B0%5D.innerText.match(/%5C(%5Cd%2B%5C.%3F%5Cd*%5C)/g)%3Bif(%24itemEst)%7B%24itemEst%3Dnew%20Number(%24itemEst%5B0%5D.replace(%22(%22,%27%27).replace(%22)%22,%27%27))%3Bif(!isNaN(%24itemEst))%7B%24tot%2B%3D%24itemEst%3B%7D%7D%7D)%3B%24lNameUp%3D%24lName%5B0%5D.innerText.match(/%5E%5B%5E%5C(%5D*/i)%3B%24lNameUp%2B%3D%27%20(%27%2B%24tot%2B%27)%27%3B%24lName%5B0%5D.innerText%3D%24lNameUp%3B%24lNameInput.val(%24lNameUp)%3B%7D)%3B">Checklist sum</a>