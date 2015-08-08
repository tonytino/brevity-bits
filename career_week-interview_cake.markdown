# Parker Phinney ([Guest Speaker](http://madebyparker.com))

[Interview Cake](https://www.interviewcake.com). Interview questions and guidance.

## Coding Interviews

*Typically about 45-60 minutes.*

*Always pseudocode first!*

*Get comfortable with Big-O Analysis.*

### Main Takeaways

1. **Use descriptive variable names.** You shouldn't ever *need* to leave comments, but they are still worth considering. Variable names should essentially be *embedded comments*. Code should communicate the procedure, variable names offer an opportunity to communicate why (why you're doing what you're doing).

**Bad Example:**

difference = price1 - price2

- difference is implicit based on the code, making it redundant and not helpful.

**Improved:**

profit = sellPrice - buyPrice

**Additional Example:**

usernamesToIpAddress = {"monkey" => "100.00.00:1337"}

- profit explains why you're using the function

- code shows what type of math is being done, the procedure

- variables in function are explicit about what they represent

2. **Treat the problem solving process as three distinct steps:**

    1. Design the algorithm (pseudocode)

    2. Write code as quickly as possible (just get the logic down)

    3. Debug the code (look for obvious/noted silly mistakes)

    *Focus on getting the whole procedure down first (your approach to an algorithm), and when done, go back to look for errors (leave a symbol where you think there may be an error, like "is it a minus b, or b minus a?").*

    *Don't worry too much about edge cases where your solution might not work. Solve the problem as it exists currently.*

3. **Coding interviews are a trail coworkering session.**

### Being asked to write a function that does something in particular.

- Important to think out loud and involve in the interviewer (if you're going down the wrong path, they might not know why and won't correct you).

- You want your interviewer to remain focused and not think about other stuff while you're working, so keep them engaged and show how well you communicate.

- Pitch your idea (like how you want to tackle the problem) before taking a specific approach; they might give you a suggestion for optimizing.

- Always announce what you're about to do before you do it (helps them follow along, catch rabbit holes, shows communication skills).

- Do not worry about what public functions are available. Tell them you're going to invent one for the sake of the problem (e.g. let's pretend we have a push method that will add this variable to this array).

- Engineers aren't like finance/marketing folk; they're not manipulative and may accidentally give you hints when you check-in on your progress (much more likely to accidently help you). So, you could ask "Does what I'm suggesting make sense?" or "How do you feel about that?" (open-ended question), which may lead to them saying something like "Yeah, that makes sense, but you may benefit from trying it from this angle instead".

- It's better to use hints interviewers freely give rather than follow your own train of thought. You don't lose points for taking in hints - in fact, you lose points for ignoring their suggestions and talking over them (or acting like you don't need hints and already know everything). They will understand if you lose your train of thought because of interruptions; it is a high-stress situation after all.

- **Coding interviews are a trail coworkering session.** They want to know what it's like to work with you, they're *not* testing your knowledge. They're on your team!!! Act like *friends*. Remember, personalities get jobs, skills and experience gets interviews.

- Never pretend to understand what interviewers tell you or suggest (like hints). It will eventually become clear that you pretended to understand and they will think you're deceptive.

- Someone who is a great communicator will have a huge advantage over someone who knows a tremendous amount but can't communicate their thoughts. If you get further on a challenge than someone who communicates really well, the interviewer may think you just guessed right or something.

- Communication skills, energy, and enthusiasm are **important** factors, but they will not get you the job if you really struggle on challenges. Match their personality to some extent (if they're a chill person, act chill).

- Remember that whatever skills you put on your resume are fair-game for being tested on during your interview.

- It's good to be able to speak with clarity without being to verbose. Explain complex things briefly (imagine explaining it to a child).

- Whenever you have an on-site interview, expect it to last anywhere from an hour to all-day.

- It's fair to ask what concepts to expect to cover during a coding interview.

- You *usually* get to chose what language you want to write in.

### Tips for writing code on a whiteboard.

1. Always start on the top-left of the board. **Maximize your space.**

2. Always leave a blank line between each line so you can make amendments later.

3. [Said he'd come back to this.]

4. Position yourself so you're not giving your audience your back the entire time. You should try to be as close to your interviewer as possible. If they step back from the board to think, do so also and ask something like "What do you think about that/___?". Mirror body language.

5. Avoid creating a vibe where you're being tested - you want the interviewer to feel like they're on your team.

### Common JavaScript Trivia Questions

- What is a closure?

- Hoisting

- Object Model

- Scope (why you var or not use var)


### Other

- When it comes to Big-O Notation (time required versus memory required), time efficiency is usually more important than memory.

- Order of Big-O Notation:
    1. O(1)

    2. O(log n)

    3. O(n)

    4. O(n log n)

    5. O(n^2)

    *Scale matters more than anything else here. In other words, focus on reducing your miles cost, not your inches cost. The former has a much more significant impact.*

- Bring copies of your resume if you can remember to.

- In general, companies don't really care about what you wear to the interview. Dress comfortably, confidently, and ___. Matt's approach.

### You ARE a Software Engineer already.

1. Imagine your dreams as if they are already truths. *You should think about yourself as a Software Engineer, not as a recent DBC grad that is learning to code still.*

2. Speak as if they are already truths. *You should tell employers that you ARE a Software Engineer with X skills.*

3. Act as if they are already truths. *You should code like you know what you are doing. In five years from now, you still will feel like a rookie.*

*Perceive yourself as you will be in a year from now. In other words, in a year from now, you will be a Software Engineer that still won't know everything there is to know (languages, practices, frameworks, etc.), so why discount yourself now? You are just as qualified as you will be then, you just don't treat yourself that way.*