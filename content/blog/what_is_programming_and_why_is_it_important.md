+++
author = "Caleb Faught"
categories = ["Programming", "Ruby"]
date = "2016-05-30"
description = "Brief overview of what programming even is, and breaking down some of the abstract ideas."
featured = "pic3.jpeg"
featuredalt = "jQuery code in code editor"
featuredpath = "date"
linktitle = ""
title = "What is Programming and Why is it Important"
type = "post"

+++

### What is Programming?

Before I get too deep into the details on the topic of programming, I want to talk a little bit about what programming is, what it is not, and why it is important in todays world. Programming is how we humans communicate specific instructions on how to do something to a computer. Programming is the tool that developers use to flesh out ideas for solving a problem. Unfortunately, computers require a very specific form of communication called a programming language. Ruby, Python, and Javascript are good examples of what we call 'High-Level' languages that humans can read and write with relative ease. Computers, however, do not directly know what to do with a high-level language; they must interpret or compile the instructions down to what is called machine code. Machine code is the closest step up from binary, the 1's and 0's that computers really understand and operate on. An example of a compiled language is C, this type of language has the advantage of removing the middle step of translation everytime the program runs like an interpreted language does.

Programming is just the tool for instructing the computer in the broader field of computer science. The main comcept that needs to be understood in this field is problem solving. Everything else is just reasoning through what problems a computer can solve efficiently. We call the solutions to certain problems an 'Algorithm' which is basically a recipe for do something. Generally, we start thinking of an algorithm in what is called 'Psuedocode' that is English that can be easily translated into a programming language later.

Here is an example of psuedocode describing the algorithm for finding the whole square root of a number (if it exists):


```
set variable num1 equal to user input
set variable counter equal to 1

while counter less than num1 do the following:
   if counter times counter is equal to num1
     stop and return counter to the user
   else
     increment counter by 1 and repeat go back to line 4
if counter times counter is not equal to num1
   return to user "No whole square for this number."
```

 This example is not perfect, but it is easy to see what it is doing, it starts with a number that the user wants to find the square root of, then it starts counting from 1 and multiplies each number by itself until the result equals the number given by the user; if no square root is found, the user is told there is "No whole square root."

Since Ruby is a high-level language, it reads very similarily to pseudocode. Here is a translation of our algorithm in Ruby:

```
puts "Enter a number to find the whole square root: "
num1 = gets.chomp.to_i
counter = 1

while counter < num1 do
	if counter * counter == num1
		puts counter
		break
	else
		counter += 1
	end
end
if counter * counter != num1
	puts "No whole square root found."
end
```

There are some optomizations to be made to this algorithm, but it gets the point across of how programmers use a programming language to outline a set of instructions for the computer to follow.

### Why is this Important?

As you can see programming is not magic, it is just very detailed instructions. Programming is becoming increasingly important for even non-programmers. For example, we are surrounded by computers today; there's even computers in appliances now. What if someone works at a job that deals with computers and sees that a certain part of their job is repetitive (that could be automated) and this task takes away a lot of time from another part of their job? If that person knew the basics of a scripting language, they could potentially write a program to do that task in a fraction of the time it would take them doing it by hand. A good example of this is data entry and reporting. As said before, the basic building block of programming is problem solving. Therefore, the practice of writing programs for everyday repetitive things also builds an individual's ability to think about problems and come up with solutions.

Then there are those that just enjoy solving puzzles and problems and have discovered that there is a career in doing exactly that; and that is how people end up as software developers. These individuals are needed to create the ever growing need for software that the general public uses on a day to day basis.

## Where to go From Here?
If you are interested in learning more about programming, check out my [tutorials](../../itemized/) section.
