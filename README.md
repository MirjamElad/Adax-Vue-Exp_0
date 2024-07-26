# ADAX for Vue, a simple test app:

**NB**: [Consult the code and play with the app here: ⚡️](https://stackblitz.com/~/github.com/MirjamElad/Adax-Vue-Exp_0)

![image](https://github.com/user-attachments/assets/1639cfdc-9808-45de-8737-502efd01f2d1)

The example app allows FANS to vote for either Blue or Red. Notice when voting for either the results panel on top does show the updated score. At the bottom, both "FANS" areas show their respective mood with an emoji. If it's a tie both moods are neutral 😐. Otherwise, the winning team displays 😃 and the losing one 🤬. Click/Vote to see the results pannel update immediately. On the other hand, the "FANS" areas only updates if there is a "change of mood".

![image](https://github.com/user-attachments/assets/e9187244-7396-4d6b-94fa-fc7b2cea9142)


## Code overview:

**State** _(in: "./src/state.ts")_: The app's state/data and the functions to read/query or write/mutate it. This file also contains the app's rules!

**App** _(in: "./src/App.vue")_: The app entry point where component are imported and rendered.

**Result Panel** _(in: "./src/components/ResultPanel.vue")_: Result Panel continuously displays current score.

**Fans Group** _(in: "./src/components/FansGroup.vue")_: Two instances of this component are shown in the App. One for each group/team (i.e. Red & Blue). Each allows for voting for the given group/team and shows the mood of that team. Note that this component only re-renders when applicable (i.e. when the mood changes) 

**NB**: [Consult the code and play with the app here: ⚡️](https://stackblitz.com/~/github.com/MirjamElad/Adax-Vue-Exp_0)
