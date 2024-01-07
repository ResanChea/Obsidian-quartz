---
{"dg-publish":true,"permalink":"/action-aids-child-sponsorship/"}
---

# ActionAid’s Child Sponsorship

- Child Sponsorship (CS) is part of the [[ActionAid\|ActionAid]]’s funding program to connect children of a community with the sponsor/funder who is pledging to improve their livelihood.
    - Aim: to be the catalyst of social change

# Process of Child Sponsorship Program

- The types of communicative material in the CS program
    1. Child Sponsorship Report: are measurements of what Actionaid does.
        - how their money is spent and send to sponsor
        - impact, result,
    2. Soft Story Report send to sponsor
    - Child corner: what benefits kids in the society got from the program
    1. facts and figure report: 5w1h
    2. Gift Fund Report: funder want to add more money over their monthly payments
        - equally distribute in society in events or things that help everyone at once
        - no jealousy
- SK: Sahakom is the system filled with CM, PU, background
    - Before it was NK: African word meaning Chain Link, represent the connection between children
    - SK: 45 countries voted for it to be a Khmer word
    - record all info of children, photo, report, plan. It's a database of all things related to the child program.

# Partern Orgs
- 005 Pursat: BCV, RFCD
- 006 Kampot: CWDC
- 010 Kompong Thom
- 013 Koh Kong
- 020 Udor Meanchey


# Funding Mechanism

- Foreign Affiliates (FA): are the countries which sends monthly funds to our CS program. Currently there are 5
    - [[Italy\|Italy]]
    - Greece
    - [[UK\|UK]]
    - [[Australia\|Australia]]
    - Ireland
- Currently there is 7,240 children with links to FA(s)
- Child Messages are collected twice a year
    - There p1 and p2: 6 months each (3-8, 9-2)
    - 4 months to collect, 2 months to translate
- How they raise funds in FA countries
    - Racing events, marathon, concerts, and fundraising in other countries that brings money in as charity to ActionAid.

# Approach

- Actionaid became transformed from a service providing organization (Charity) to HRBA (Human rights based approach) to help families make money for themselves
    - helps parents or families
    - child is the connection to sponsor
    - teaching parents to plants
    - to teach them what they are entitled to, where they can get it, who to tell
    - empower people living in poverty

# Child Message (CM)

- Sincerely, with love, warm wishes,
    - name of child should be on the bottom right of the page
- Bottom Left: (Translated by ____)
- There should be a title of each Child Message
- Title
    - First Message: Welcome to Cambodia
    - Standard & Goodbye:
        - Sending loves from Cambodia
        - Greetings from Cambodia
- Greeting phrase for each country
    - Italy: Dear ___
    - UK, Australia, Greece, Ireland: Dear sponsor
- Don’t(s)
    - Don’t mention something sensitive to sponsor
        - That brings trouble to the org
        - Actionaid is not about policing domestic issues
        - It goes both ways, from sponsor to child as well
            - Give child more advantage
    - No asking for more: actionaid isn't a charity

[[ActionAid's Child Messages\|ActionAid's Child Messages]]

# Useful Notes to Self

- Inform or send absent forms to bong Pros/Dyna
- Inform telegram if you’re late
- Don’t put any full names in the CM(s)

[Daily CM Translation Tracking 2022](https://docs.google.com/spreadsheets/d/1Hec4p5rt2Qb0fNwFiPq56d9pB0iWV0ylMVi-48iyI_o/edit?usp=sharing)

# Renaming

```bash
for filename in *.jpg
do text=$(tesseract "$filename" stdout | grep "LRP")
	cp "$filename" renamed/"$text".jpg
done

## | cut -f2 -d":"| to only pick the second field to rename
##	cut -c  == means skip the first and move to the second character
## head -1 is used to only output the first line, isn't needed in this case
for filename in *.png
do text=$(tesseract "$filename" stdout | grep "KH" | awk '{print $2} | cut -c 2-)
cp "$filename" renamed/"$text".png
done
```
{ #db4b92}


- Feedbacks
    - Rachana:
        - Used the wrong gender pronoun x2
        - Welcome to Cambodia instead of Welcomes to Cambodia
            - Only use Welcome when its their first message
        - Random capitalized letters
        - Crop is not a verb, its a noun
        - Fishery is not a very, Fishing is a verb
    
    The locals are harvesting rice yields