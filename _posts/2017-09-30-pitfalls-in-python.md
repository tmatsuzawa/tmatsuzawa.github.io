---
layout: post
section-type: post
title: Notes on Jupyter Notebook Extensions
category: documentation
tags: [ 'Python' ]
---

<p> This is a personal note on Python. </p>
<p> As a learning physicist, I have programmed in several languages. My first language was C, which I actually think that it was a right language for me to understand what programming actually means.
 Most of my friends in the U.S. told me that their first language was Python. I feel that Python is very intuitive, and allows concise coding compared to other languages.
 It makes sense that many universities use Python to introduce programming to students, and companies such us Quora choose Python to build their platforms.
 However; I am actually satisfied with C as my first exposure to programming since C requires you to think what it is like to talk to computers.
 Frankly speaking, programming is writing a script which gets compiled to a form a machine can actually operate using memory.
 C requires you to define all variables, initialize them, code with a lot of brackets/parentheses, give a script to a compiler, and execute the compiled execution file.
 Phew... Python does not let you do that. </p>

<p> Java was my second language, where I picked up the idea of object-oriented programming. This was also about the time when I learned about an integrated development environment (IDE).
Java is not horrible to learn for people with background in C. So I picked up instantly. C++ and C# are nothing to fear at this point. After playing with command prompt (Windows) and terminal (Mac),
I picked up basics of shell scripts as well as unix commands.
</p>

<p>
As I advanced in my undergraduate education, I had several projects during my internship at Fermilab, and research experience at universities. Some required C and Java.
Often, those projects were developed by original languages, but they were nothing to fear. If you have basics in a couple of languages (C and possibly Java for me), they can be easily picked up.
So I picked up some trivial skills such as how to run NEURON, LAMMPS, and G4beamline. I wonder if I will code for these simulators in the future.
During the period, I picked up how to use Matlab and a little bit of Mathematica. I have more experience in Matlab. I think it is a very helpful software, and simultaneously agree with popular criticism
that it is buggy. I feel they are getting better every year, and I personally encountered a very bothering bug once. Otherwise, I had no problem with Matlab.
</p>

<p> Anyways, this is a personal post about Python. There are many pitfalls for programmers like me with background in C. I intend to post some useful tips for myself.
Some tips are old, basic, and certainly not useful to experienced programmers. I do this for myself. I pick up things whenever need arises. :)
</p>

<h4> Substitution/Copying </h4>
<p>
dict1={}
dict1["a"]=1
dict1["b"]=2
print dict1

dict2=dict1
print dict1,dict2

dict1["a"]=10
print dict1,dict2

var1=1
var2=var1

print var1,var2

var2=10
print var1,var2
</p>
<p> This returns...
</p>

<p>
{'a': 1, 'b': 2}
{'a': 1, 'b': 2} {'a': 1, 'b': 2}
{'a': 10, 'b': 2} {'a': 10, 'b': 2}
1 1
1 10
</p>

<p> This is insane if I were coding in C. This is a common pitfall. Copying a list, a dictionary etc. cannot be done by substituting a variable to a new variable with empty values.
Those lists or dictionaries are linked. i.e.- Copying like this sets a reference to the original list/dictionary, and changes to the new list/dictionary affects to the original.
</p>