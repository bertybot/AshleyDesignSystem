- Start Date: 2022-08-05
- RFC PR: (leave this empty)
- Design System Issue: (leave this empty)

# Overhaul Design System Color Tokens

## Summary

Color tokens are a way for UX, Creative and Dev to speak the same language in regards to color when creating pages. Color tokens are an extremely important foundation to any design system
and people understanding and using the color tokens correctly is important to the success of the system.
Right now the Color tokens are vague and hard to use because no one at Ashley created them. I am suggesting that UX, Dev and Creative collaborate to create a better color token system more akin to our actual brand, and one that will be easier for our teams to collaborate on and understand. 

## Motivation

If no one understands how or when to use certain color tokens and we instead use color tokens arbitrarily. The whole point of having color tokens will be pointless.

Some heavily sought features that will not be possible without a well defined and understood color token system.
- Dynamic Themes
    - Right now we have already seen people just start to the token for the color they want instead of the token needed for it's use. This practice will make doing dynamic themes completely impossible since colors won't be organized by their actual use.
- Figma Integration
    - We have already begun to have problems using the color tokens in figma which should be a feature out of the box. This wastes Dev and UXs time since we constantly have to reverse engineer what colors to use from the wires. 
- Easy Brand Color Updates
    - Like the Theme argument colors being used arbitrarily makes it hard to update colors and have the changes reflect uniformly throughout the site.

My main point is that we need to collaborate together to make system that works and that we understand. The current one was made by a completely outside team with no consultation on our teams needs or our brand as a whole, and if the color tokens aren't used correctly a lot of critical features wanted for Apollo will be impossible

## Detailed design

### Technical Background

[Please Refer to This article on creating a DS language](https://xd.adobe.com/ideas/principles/web-design/how-to-develop-design-language/)

My main point is that for the success of the Ashley Design system, the design language of the Ashley Design System should reflect not only the brand of Ashley, but the people working on it. Doing this will allow us to use and collaborate much more effectively. Therefore we should come up with one and not use an outsourced one.

Also please refer to the Material Design System article [on creating color themes](https://material.io/design/color/the-color-system.html#color-theme-creation)
### Implementation

My suggestion for the new Color language is more similar to what we had before EPAM.

The new Design Tokens Should have two things.

- Semantic
    - The names of the design tokens should very sufficiently explain their use just from their name and not require referencing outside documentation to understand their use. This makes the design system easier to work with and communicate with. It also relieves doubt, and ensures more consistency in our code. You won't have to question if you are using the right color while coding the colors. The colors themselves explain what they do and it is very obvious when they are being used wrong.
- Reflect Our Brand and our teams
    - Our current system was completely stolen from IBM carbon. A tech website is way different than a furniture website and therefore we shouldn't be using tokens from a tech website and instead creating tokens by auditing our current brand.
    - Also our teams need to come up with it. This ensures that we all understand it and use it correctly.

My suggestion for the new color tokens.

- *background*
    - The background color is used for the background of the site it is a relatively simple token that sufficiently explains what it is for but, also makes sure it is not used wrong.
- *surface & surface-{variant}*
    - Surface colors are neutral colors on which we put basic page content. This name semantically lets you know that this color is for surfaces on which you put content.
    - With this I also suggest surface-{variant} 100-500 for the light grays we like to use throughout the site.
- *primary*
    - Primary color. This color denotes a highly important item on the page and is the highest of visual hierarchy on the page. The name primary sufficiently explains the importance of the color way more than the current which is interactive-01.
- *secondary*
    - This color denotes secondary actions on the page and is slightly lower in primary in visual hierarchy. Right now the difference between primary and secondary is hard to decipher in dev since primary is interactive-01 and secondary is interactive-02
- *error, success, warning*
    - just call the status colors by their name it reduces a ton of confusion.
- *on-surface, on-primary, on-secondary*
    - these colors are for the content such as text/icons that go on top of these tokens. The name denotes they go on top of another color. This scheme makes creating themes a breeze since all we need to do is ensure that these colors have enough contrast to the new token colors and we are done. Right now when to use which text color is or icon color is extremely vague. 

Please remember that these are not suggestions for the actual colors but, what we call certain colors based on their use. 

With this we are also heavily reducing the amount of tokens too. This is to reduce the cognitive load of the current tokens and make it easier to understand as teams start to grasp the basics. More tokens can be added once need arises but, right now just add the tokens we need. Starting with a ton is confusing especially since a lot of the team is new to working with design systems. For example, right now with all the reduction of the use of orange their are 18 tokens that are the same color of Black, and with the lack of Figma integration figuring out which one to use is a nightmare.

## How we teach this

Having created this as a team should already up the general knowledge on this subject a ton but, Updated storybook documentation and better collaboration between UX and dev will also help.

## Drawbacks

- Ton of work to refactor all the components again to a new color token system
- on colors can be limiting on the pallette since every primary token can only have one and they always need to have enough contrast for every variant.
- Color Pallette itself will be a bit more limiting

## Alternatives

Sticking with our current system. I am expecting almost this same level of rework if we try to implement themes with the current system. 

Also there is just still a ton of confusion on the actual design token colors since EPAM made two sets, but also only setup Figma tokens for one. This has caused a ton of confusion, frustration and wasted time and will need to be resolved at some point regardless.

## Unresolved questions

Need input from teams outside of dev on what their suggestions for the color token names are. 
