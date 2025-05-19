.. rlc-doc documentation master file, created by
   sphinx-quickstart on Sun May 11 18:38:45 2025.
   You can adapt this file completely to your liking, but it should at least
   contain the root `toctree` directive.

Rulebook Documentation
======================

**Rulebook** is a *statically-checked imperative language* that turns **interactive behaviour**—reinforcement-learning environments, video-games, or in general `complex interactive subsystems <./the_inversion_of_control_problem.html#complex-interactive-subsystems>`_—into something you can **query, replay, fuzz, and formally verify**.

`4hammer (our flagship demo) <./4hammer.md>`_ shows Rulebook in action.

**Why Rulebook?**

* `Capture every run <./language_tour.html#spin-functions-implications>`_ – automatically store, load, print, replay, and mutate both state *and* execution traces.
* **Push-button testing** – drop in standard `fuzzers <./language_tour.html#automatic-testing>`_, formal `proofs <./language_tour.html#finite-interactive-programs>`_, or `reinforcement-learning agents <./language_tour.html#reinforcement-learning>`_.
* `Self-configuring UIs <./language_tour.html#self-configuring-uis>`_ – the UI introspects your program graph and adapts its controls on the fly.
* `Remote execution <./language_tour.html#remote-execution>`_ – ship interactive logic across the network with a zero-boilerplate RPC layer.
* Solve the `interactive inversion-of-control problem <./the_inversion_of_control_problem.html>`_ at the language level—no more interactive spaghetti.

**Under the hood**

Rulebook’s defining idea is the notion of `Action functions with SPIN properties <./language_tour.html#action-functions>`_, which make all of the above possible.

**Integration**

Rulebook compiles to **one shared library (or WebAssembly module)** with a C-compatible ABI and generated bindings for `C, C++, C#, Python, and Godot Script <./language_tour.html#compatibility>`_. Use it the way SQL complements those languages—drop it in wherever **interactive logic** is the hard part.

`Zero mallocs <./language_tour.html#performance>`_ unless explicitly requested by the user.


.. toctree::
   :maxdepth: 1
   :caption: Concepts:

   language_tour.md
   the_inversion_of_control_problem.md
   project_rationale.md

.. toctree::
   :maxdepth: 1
   :caption: Tools

   rlc.md 
   building.md 
   interoperating.md


.. toctree::
   :maxdepth: 1
   :caption: Reinforcement Learning Docs:

   tutorial.md
   gym_tutorial.md
   

UI, Controller and Gameplay Programming
########################################

`UI, controller <https://en.wikipedia.org/wiki/Model%E2%80%93view%E2%80%93controller>`_ and gameplay programming are among the sections that benefit the most from using Rulebook. Beside automatically `fuzz <./language_tour.html#automatic-testing>`_ , `prove correct <./language_tour.html#finite-interactive-programs>`_ and `run reinforcement learning on <./language_tour.html#reinforcement-learning>`_ your program, write  `self-configuring UIs <./language_tour.html#self-configuring-uis>`_ , Rulebook automatically provides a sharp division between UI concerns and Controllers or Gameplay.


.. toctree::
   :maxdepth: 3
   :caption: UIs, Controllers, Gameplay:

   ui_gameplay.md 
   4hammer.md


.. toctree::
   :maxdepth: 3
   :caption: References:

   language-reference.md 
   stdlib/index.rst



