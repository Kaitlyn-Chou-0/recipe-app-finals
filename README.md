# What's for Dinner

This is a full-stack GenAI web app that transforms photos of ingredients into personalized recipes through a multi-step agentic pipeline — featuring chained API calls, custom system prompts, structured output schemas, and human-in-the-loop editing. 

All you have to do is just take a photo of your ingredients, and you'll receive a recipe based on the ingredients you have. I also added additional features that allows for a customizable experience, such as cuisine preferences, which meal of the day and serving size. 



Work Flow of App
┌─────────────────────────────────────────────────────────────────────-┐
│                        WHAT'S FOR DINNER                             │
│                                                                      │
│  ┌─────────────-─┐    ┌──────────────┐    ┌───────────────────────┐  │
│  │  IMAGE INPUT  │───▶│   AGENT 1    │───▶│  INGREDIENT INVENTORY │  │
│  │  User uploads │    │  Inventory   │    │  Parsed JSON output   │  │
│  │  photo(s) +   │    │  Expert      │    │                       │  │
│  │  optional     │    │              │    │  User can add,        │  │
│  │  descriptions │    │  Custom      │    │  delete, or edit      │  │
│  └──────────────-┘    │  system      │    │  ingredients before   │  │
│                       │  prompt +    │    │  proceeding           │  │
│                       │  JSON schema │    │                       │  │
│                       └──────────────┘    └───────────┬───────────┘  │
│                                                       │              │
│                                                       ▼              │
│  ┌──────────────┐    ┌──────────────┐    ┌───────────────────────┐   │
│  │    OUTPUT    │◀───│   AGENT 2    │◀───│  USER PREFERENCES     │   │
│  │              │    │ Nutritionist │    │  Serving size,        │   │
│  │  Recipe +    │    │  & Recipe    │    │  cuisine preference,  │   │
│  │  Cooking     │    │  Developer   │    │  dietary restrictions │   │
│  │  Instructions│    │              │    │                       │   │
│  │  + Nutrition │    │  Custom      │    │  If unspecified →     │   │
│  │  Info        │    │  system      │    │  agent selects        │   │
│  │              │    │  prompt +    │    │  autonomously         │   │
│  └──────────────┘    │  JSON schema │    └───────────────────────┘   │
│                      └──────────────┘                                │
└─────────────────────────────────────────────────────────────────────-┘

A small story on how the app name was chosen, growing up me and my sister loved this family comedy called Everybody Loves Raymond, and at the end of every episode, there would be a snapshot of a dinnertime table with the headline "What's for dinner". My sister reminded me of our fond show while discussing my app, and she inspired me to name my app after our favorite segment of the show.



All files are covered by the MIT license, see [LICENSE.txt](LICENSE.txt).
