# Words-Booster-iOS-TestTask
### Coding challenge for iOS Engineers.

Write a simple application that allows users to see a list of animal categories and read interesting facts about them. You should provide your solution as a link to a public repository on any git hosting service you prefer: GitHub, GitLab, Bitbucket. Please make commits of logical units to evaluate your progress and add comments as you see fit.

## Functional Requirements

First of all, on app launching the content should start to load from the link which you can find in the [Resources](#resources) section.

Content stored in JSON format and has the following structure:
```
[
  {
    "title": “Some title",
    "description": “Some description",
    "image": “image url",
    "order": 1,
    "status": “paid/free",
    "content": [
        {
          "fact": “Some fact",
          "image": “image url"
        }
    ]
  }
]
```

### Application Screens
#### Animal Categories List 
On this screen, users can see a list of animal categories. Please, provide a loading state if the content has not loaded yet. When the content is loaded the list appears. All items should be sorted by the order. Each item view consists of following elements:
  - Image
  - Category name
  - Category description
  - Status(**free**/**paid**). This means that you need to provide 2 states for free and paid categories. Also in a case when field content is empty then provide one extra state(for example **coming_soon**).

Scenarios on [Animal Categories List](#animal-categories-list):
  - Tap on the **free** item -> The navigation to the [Facts Screen](#facts-screen) happens.
  - Tap on the **paid** item -> The alert with title **Watch Ad to continue** and **Cancel**, **Show Ad** buttons should be shown. By tapping on **Show Ad** we just show loader for 2 seconds and then navigation to [Facts Screen](#facts-screen) is happening. By tapping on **Cancel** we just hide alert.
  - Tap on **coming_soon** item -> The alert with button **Ok** and appropriate title is shown.

You can find sample of design in [Resources](#resources) and [Design Example](#design-example) sections.

#### Facts Screen  
This screen consists of:
  - Navigation bar with the **Back** button and the title of the category.
  - Horizontal list of fact items that should be implemented in a paging way. Only one item has to be shown on screen at the moment. 
  - Each item consists of the **Image**, **Text**, **Next** and **Previous** buttons.

Scenarios on [Facts Screen](#facts-screen):
  - Tap on the **Back** button -> Navigate to [Animal Categories List](#animal-categories-list)
  - Tap on **Next** button or **Swipe** forward -> move to next fact
  - Tap on **Previous** button or **Swipe** backward -> move to previous fact

You can find sample of design in [Resources](#resources) and [Design Example](#design-example) sections.

## Technical Requirements

- Swift is required.
- MVVM architectural pattern is preferred.
- SwiftUI is preferred.
- Combine is preferred.

## Design Example

Here is an example how application might look like, but the final decision is up to you.

- [Сategories List Example](categories_list.png)
- [Facts Screen Example](facts.png)

## Resources
- [JSON Content Link](https://drive.google.com/uc?export=download&id=12L7OflAsIxPOF47ssRdKyjXoWbUrq4V5)
- [Figma Link](https://www.figma.com/file/tCZyyMoGAuHiOnY6zSg65A/Words-Booster-Test-Task-iOS?node-id=0%3A1)

## P.S.
If something is unclear, feel free to ask any question to our **Recruitment Team**
