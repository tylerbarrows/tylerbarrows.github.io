---
layout: default
title: Home
permalink: /
nav_order: 1
---

<div style="display: flex; align-items: flex-start; gap: 20px; flex-wrap: wrap;">

  <!-- Figure -->
  <figure style="flex: 0 0 50%; min-width: 200px;align-self: center">
    <!-- <img src="/assets/cfd/IntroGeometryAndMach.png" alt="CFD Results" style="width:100%; border-radius:5px;"> -->
    <img src="/assets/me/cambridgeHalfNov2025.jpeg" alt="Cambridge Half Marathon" style="width:80%; border-radius:22%; display: block; margin: 0 auto;">
    <figcaption style="text-align:center;"><em>Cambridge Half Marathon.</em></figcaption>
  </figure>

  <!-- Text content -->
  <div style="flex: 1; min-width: 250px;">
    <h1 style="text-align: center">About Me</h1>
    <p>
      Hi, I’m Tyler — an engineer with interests in math, physics, and modeling. I currently work as a control engineer at GE Aerospace primarily supporting our demonstrator engine programs. 
    </p>
    <p>
      I've had a lot of success in my career due to my ability to be curious about a problem, conceptualize the problem and identify the relevant physics, and model the situation mathematically. A lot of these skills I learned outside of the classroom and workplace. Soon after the completion of my undergrad degree, I realized I missed learning and took that upon myself to address. This was mostly done through reading math and physics books. I now have a couple lifetimes worth of textbooks in my apartment. 
    </p>
    <p>
      This site is a collection of some of my work, notes, and side projects. These projects are not intended to be complete engineering applications but to demonstrate my curiosity, ability to learn new concepts, and to put some structure behind that. 
    </p>
    <p>
    <!-- Feel free to explore the **Modeling** and **Miscellaneous** sections, or [get in touch](/contact.html). -->
    Feel free to explore the <a href="/modeling/index.html">Modeling</a> and <a href="/miscellaneous/index.html">Miscellaneous</a> sections, or <a href="/contact/index.html">Get in Touch</a>.
    </p>
  </div>

</div>

<div style="display: flex; align-items: flex-start; gap: 20px; flex-wrap: wrap;">

  <!-- Text content -->
  <div style="flex: 1; min-width: 250px;">
    <h1 style="text-align: center">More About Me</h1>
    <p>
      I began my engineering career at BlazeTech and the appeal of BlazeTech was that I would be able to work on a variety of projects. I didn't really know what I wanted to do coming out of college. BlazeTech was an amazing opportunity to learn about a variety of topics and I developed a strong passion for modeling and analysis. I got to improve my design and testing skills too. I enjoy analysis work the most, but value and appreciate that everything comes down to test. At BlazeTech, I used my analysis skills to identify what rotational speeds we needed to test our spin filter at to see the efficiencies we were targeting. I then worked with the team to make our filter design supported running at those speeds. Instead of learning all this on test, I could anticipate some of the challenges through analysis work. Through my strong analysis skills and understanding the importance of test, I create a strong connection between what we model and analyze, and how to test component and systems. 
    </p>
    <p>
      I joined GE in the control system group mainly to learn more about system integration and control seemed like a natural extension of my modeling interest. Before developing any control, you usually need a model. At GE, I learned a lot about system architecture and control theory. I have always prided myself on my range of skills. My depth is in phsyics-based modeling of thermo-fluid dynamics, and I extended this to control theory through GE. I am also very comfortable working in disciplines around this including performance and combustion. When evaluating and designing a control system, it is extremely important to understand the plant. In our current projects at GE, fluid dynamics are more part of the control loop then before, and I have carved out a space between the fluids and control system disciplines. I use my modeling background to ensure that our control system models include all relevant physics, and I use my control background to ensure that the system architecture doesn't require too complex control system solutions. 
    </p>
    <p>
      My greatest strength is that I can see a problem or challenge, identify what needs to be done, identify the skills needed to develop the solution, and then implement that. I thrive in places with a lot of uncertainty and like to think of myself as a bridge from theory to application.
    </p>
  </div>

</div>

<div style="display: flex; align-items: flex-start; gap: 20px; flex-wrap: wrap;">

  <!-- Text content -->
  <div style="flex: 1; min-width: 250px;">
    <h3 style="text-align: center">AI Disclosure</h3>
    <p>
    I did use AI (Claude) in some of these projects. I think it's important to be upfront about that. I think it's also important to clarify how I use AI in my work. I use AI in three different ways: 
    </p>
    <ol>
    <li>Advanced Google:</li>
    <p>
    I've had some luck in using AI to bounce ideas off. The collision detection using the Separating Axis Theorem in my magnet model came from Claude. Claude showed me how that theorem could be the answer to my problem and then I went and learned about that theorem and how to use it on my own. This is susceptible to what Claude thinks is relevant or not, and you have to be careful since sometimes AI just tells you what you want to hear.
    </p>
    <li>Some scripting help:</li>
    <p>
    I am very much against letting AI develop any modeling code without direct involvement from me. If I don't understand the math or the physics being used, I don't use it. I do use AI to help me build scripts to pull data in from an Excel file or to help make my code more robust. In my Magnet Model, Claude helped me build this class function where I can input the magnet properties once and then use that function to pull the properties in rather than having to change the properties in every script. Linear algebra is a little more difficult to use in Python compared to MATLAB and Claude helped me figure out how to write row and column vectors more effectively. All of the actual physics code was written by me, or at least started by me and Claude was used to make it a little more robust to invalid entries.
    </p>
    <li>Proofreading and troubleshooting:</li>
    <p>
    Claude can be helpful in finding errors much more quickly than I am. However, you need to be careful again since AI can confuse itself. This again happened with the magnet model when Claude was telling me that my quaternion time derivative was wrong but it was actually confused about what was rotating with respect to what. 
    </p>
    </ol>
    <p>
    Just like most things, I don't think AI is inherently good or bad, but it's more about how we use it. For me currently, this is not relying on AI to do any of the math or physics for me. I value learning and knowing math and physics, and can't ever outsource that to AI. I hear stories of people building models at work that they don't understand and this can be very dangerous. I don't think this is necessarily new. There are a lot of commercial products out there (MATLAB, CFD) that have built in functions that can be easy to misuse or misunderstand. I do find some value in AI helping me structure and organize myself better. I'm not a software architect expert (far from it) and AI has helped me organize my projects better. However I constantly have to ask myself am I learning anything from this or is the AI doing it for me?
    </p>
  </div>

</div>