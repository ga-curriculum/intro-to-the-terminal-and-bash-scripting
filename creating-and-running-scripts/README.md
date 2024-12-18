<h1>
  <span class="headline">Intro to the Terminal and Bash Scripting</span>
  <span class="subhead">Creating and Running Scripts</span>
</h1>

**Learning objective:** By the end of this lesson, students will be able to construct basic Bash scripts, make them executable, and explain their purpose in automating tasks.

## What is scripting?

In simple terms, a script is a set of instructions that your computer follows to complete a task. Instead of manually typing each command, you put all the commands in a file, and the computer runs them for you—just like following a recipe.

<br>

<div class="activity guided-walkthrough">
  <h2 class="title">Creating and running a script</h2>
  <span class="minutes">15 min</span>
</div>

Let's try out a simple example of creating and running a script file.

### Create a new script file

Use the `touch` command to create a new file:

```bash
touch explainer_script.sh
```

### Make the Script Executable

By default, new files you create might not have permission to run as programs. To fix this, you need to change the file’s permission settings so your system recognizes it as something it can “execute” or run like a program.

`chmod` stands for “change mode,” and the `+x` option gives the file “execute” permission. Without this step, your computer won’t know that `explainer_script.sh` is meant to be run.

```bash
chmod +x explainer_script.sh
```

After running this command, the `explainer_script.sh` file becomes runnable, allowing you to execute it directly from the terminal.

### Add instructions to the script

Open `explainer_script.sh` in your code editor and paste the following:

```sh
#!/bin/bash

# This script explains what it means to "run a script" in simple terms.

echo "What does it mean to 'run a script'?"

echo "
A script is a set of instructions written in a programming language that tells a computer what to do.
When we say 'run a script,' we mean that we are asking the computer to follow these instructions step by step.

Here's a simple example:
Imagine you have a recipe for making a cake. The recipe has a list of ingredients and step-by-step instructions.
Running a script is like following the recipe to make the cake.

In the world of computers, scripts can do many things, such as:
- Automating repetitive tasks (like cleaning up files or backing up data)
- Setting up software (like installing programs or configuring settings)
- Processing data (like analyzing text or numbers)

When you run a script, the computer reads the instructions and performs the tasks specified in the script.
It's a way to make the computer do things automatically, without needing to do each step manually.

For example, a script to greet you might look like this:
#!/bin/bash
echo 'Hello, World!'

When you run this script, the computer will display the message 'Hello, World!' on the screen.

In summary, running a script means telling the computer to execute a series of predefined instructions to accomplish a task.
"

# End of script

```

### Run the script

To see the script in action:

```bash
./explainer_script.sh
```

The terminal will display the text inside your script, just as if you typed all those commands manually.

### Add More Interactivity

Let’s make the script a bit more interactive. For example, you can prompt the user for their name and then print a personalized message.

Open the `explainer_script.sh` file in your code editor.

Add the following lines at the end of the file:

```sh
echo "What's your name?"
read user_name
echo "Nice to meet you, $user_name!"
```

Save the file, and then run the script again:

```bash
./explainer_script.sh
```

When prompted, type your name and press **Enter**. The script will then greet you personally! This simple interaction shows how scripts can do more than just display static text—they can also respond to user input.

### Why do we use scripts?

Scripts aren’t just for personal use—you can also share them with your colleagues, teams, or entire organizations.

In a professional setting, you might:

- Store scripts in a shared code repository (like GitHub or GitLab), so everyone on the team can access and run them.
- Include scripts as part of a project’s setup instructions, ensuring that each team member’s environment is consistent and up-to-date.
- Use scripts to automate deployment or testing processes, making it easier for developers, designers, and managers to collaborate without manually performing each step.
- Create internal “toolkits” of scripts that help with common tasks, reducing the learning curve for new hires

By understanding how to create, run, and share scripts, you’re setting the stage for smoother collaboration, faster workflows, and a more scalable approach to software development.
