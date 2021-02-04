---
description: Course taken in autumn 2020 at ETH during Master studies.
---

# Physical-Based Simulations in Computer Graphics

## Overview

As a 5 credit course, it was a rather small course, yet I loved it. It consisted of [lectures](physical-based-simulation.md#lecture-topics), [exercises ](physical-based-simulation.md#exercises)and a very cool [project](physical-based-simulation.md#project). I have attented it, while I was working part time for Puzzle and did the Semester Thesis continuing the [Inverse Terrain Simulation](../../projects/inverse-terrain-simulation/) project.

### Material

Slides, exercises, old exams and some project files are in the **Course Folder** that is archived on my Study Volume. I also took **Notes** and wrote **Topic Overviews,** that are with my other physical study material. The **Project Repository** can be found on the [GitLab of ETH ](https://gitlab.ethz.ch/halucas/pbs20_solarsystem)and also in the Course Folder.

### Verdict

In hindsight, it was a very cool course. I tried out some things and could improve my studying greatly. Following are my insights:

* Many watched **live lectures were wasted**, as I was not attentive, have not understood previous needed knowledge and it went much too fast.
* **Rewatching the recordings later** proved to be much more useful, as I could pause, rewind a section and give myself much more time to let the topic sink
* **Taking notes**, as I have always done before, is still a good method, to let me take time to understand the concepts and have a **reference material to learn** with afterwards
* **Quality of the notes** are not on the level I want, should be less a copying of the slides and more a **summary in my own words**. However, this consumes more precious time.
* The **topic overviews** I mapped together have greatly helped to give me a big picture of the course. Must do in courses to come.
* I have not worked in a team on a programming project before. This experience was very valuable.
* **Solving earlier exams** was, in this case, crucial as only one previous written exam existed and assistants noted that this exam will be similar in style.
* **Journaling using GitBook** and taking time to **lay out the study plan** is very important to adapt to the course and study in an optimal way.

## Lecture Topics

Due to Covid-19, the lecture where hold on Zoom and recorded. The recordings turned out to be very useful. Worth noting, one of the lecturers, Vinicius, took great effort to include many dumb jokes.

1. **Time integration**
2. **Rigid Bodies**
   * Kinematics & Dynamics
   * Collision Response
   * Collision Detection
3. **Deformable Objects**
   * MassSpringSystems
   * Continuums Mechanics
   * Finite Element Method
4. **Fluids**
   * Eulerian - Fractional Step Method
   * Lagrangian - SPH
   * Hybrid - FLIP

## Exercises

Consisted of four programming exercises. Very interesting and provided basics for the Project, but not so important for the exam. The official exercise repository can be found [here](https://gitlab.ethz.ch/cglsim/pbs20).

1. Time Integration Schemes
2. Rigid Bodies: Collision Response, Broad & Narrow Collision Detection
3. Fluid
4. Soft Body

## Project

All details can be found in the [**N-Body Gravitational Simulation**](../../projects/finished-projects/solar-system-simulation.md) project entry.

Together with Tamara and Tatiana, we first wanted to simulate a solar system, a rigid body system, with gravitational forces and then add fracture to it, to simulate planets that crash into each other. However, it turned out this is much too ambitious. After the milestone presentation and the feedback of the assistans, we changed to a N-Body Gravitational Simulation with the goal to simulate as many particles as possible to simulate the motion within a galaxy. We managed to feasibly simulate **100k particles**. 

## References

* **Official**
  * [Course Page](https://cgl.ethz.ch/teaching/simulation20/home.php)
  * [Moodle Page](https://moodle-app2.let.ethz.ch/course/view.php?id=13417)
  * [Exercise Repository](https://gitlab.ethz.ch/cglsim/pbs20)
* [Project Repository](https://gitlab.ethz.ch/halucas/pbs20_solarsystem)
* **Further References**
  * [https://jdickinsongames.wordpress.com/2015/01/22/numerical-integration-in-games-development-2/](https://jdickinsongames.wordpress.com/2015/01/22/numerical-integration-in-games-development-2/)
  * Some good introductions \(like quaternions\): 3blue1brown
  * God damn, neidisch: [https://eater.net/](https://eater.net/)
  * [blue1brown Quaternions](https://www.youtube.com/watch?v=zjMuIxRvygQ])
  * [https://eater.net/quaternions](https://eater.net/quaternions)
  * [Basic Physics](https://physics.info/)
  * [Applied Partial Differential Equations](https://www.springer.com/de/book/9783319124926)
  * [Impulse Collision Respons](https://www.cs.cmu.edu/%7Ebaraff/sigcourse/notesd2.pdf)
  * [Fluids](https://www.karlsims.com/fluid-flow.html)

## Log

### 29.09.2020

See if I keep this log. It seems taking notes while/after the lecture the way I want, is not realistic. The tempo is to fast, atleast for the last lecture. Going to just mark needed space, maybe do notes for some lecture, but generally postpone this to the learning phase.

I really look forward to the mini-project. I have a nice idea in mind and hope that my sturdy group members Tamara aka Dämsel and Tatiana aka TatiSchnati will accept my humble epic suggestion of doing Rigid Body of a Solar System with Fracture. Meaning, we gonna blow up some planets. However, the project is not yet of my concern.

I am very ambitious and I don't want the graphics drama to repeat, where I wanted too much and was very disappointed of my failure and incompetence. See, my grade was still good, I just expected much more from me. So, first, I have a team of three, second, I intend to do a project where not the most difficult methods are involved. Meaning, some rather easy one, and then if it's going good, I extend it. So the planet system is a rigid body system with gravitation. That should be doable. I can try to make some nice renderings or similar to make it look good. Then, the fracture is a great plus.

To further improve the process I started this log. Just to think and analyse problems.

I want to do more in this course, but experience says that I will need maximum time to do the minimum, next to all my other projects. I probably need to focus more on one and finish that... For now, doing the exercises and thoroughly understanding them will do the job. An additional thing is looking for resources and linking them here.

### 1.12.2020

Starting to think about how to properly study this stuff. It's not that much. The course is only 5 credits. Yet, the matter is not easy at all. There are some concepts and math parts that really are hard to intuitively understand. I also think that some of the slides are not sooo good, because they skip some basic explanations, or just do not have enough information on it. I will definitely work with the recorded lectures. But, this will probably take too much time. I need to make an estimation of time effort for watching all of them again and taking notes.

There are 11 lectures, lasting 90 minutes atmost. For taking notes, I think I need to double that, just to be sure. Resulting in 33 hours or 4 days working 8h. Does not even sound so bad. Realistically it needs even more days, as I will not work 8h per day. But one week for note taking. One week buffer, code and exercises. Sounds good. I can do that.

I think I will already start in December, just because I have time then. Trying out to really study in advance and before the actual exam, just repeating some of the stuff. Or no. I split the weeks and I will do the second week just before the exam. Like this, I can really take advantage of my notes. I should be able to remeMber. Maybe add some smaller repetitions in between? Yes, that's the plan. Let's summarize.

1. Watch lectures and make notes during one week at beginning of learning phase
2. Repeat regularly
3. Repeat, do exercises, look at code during roughly one week before the actual exam.

### 20.1.2021

So, I am through with the **notes**, only need to fill gaps in them. Which will be the next step. After this, I will do an **Topic Overview-Sheet**, a big picture of all chapters/keywords of the subject in a mind-map manner. Then, I will look at the example exam questions to get a sense for what is asked in the exam. Then, **identify** the hard parts and parts I need to really know and just **repeat** repeat and fill gaps and go where it hurts. Also at one point, look at the **exercises** and don't forget the **forum**.

**Wed 27.1**  
Finish note gaps  
Overview Mind Map  
Identify/Rank importance of topics

**Thu 28.1**  
Exam Questions  
Exercises

**Fri 29.1 -  Tue 2.2**  
Repeat & Repeat

### 4.2.2021

The exam is done and it went pretty good. Was able to solve almost everything and even though the questions weren't easy, it was very fair. Nothing unexpected, but a bit challenging. I am content. In particular with my study approach. Which was somehow different, as it was the only course, however much better than usually. I suppose, I will have a grade of atleast 5, which is super awesome. Now, I will wrap up everything, finish and polish this GitBook entry, archive all the files and put away my handwritten notes to the other study stuff. Will keep positive in mind and maybe/hopefully I will take up the project again and do some nice renderings.

