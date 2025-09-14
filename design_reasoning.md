# Design Reasoning: Python Debugging Assistant

## Overview

This document breaks down the design choices for an AI debugging assistant. The goal is to help students learn Python through guided problem-solving rather than by providing direct solutions.

## Core Philosophy: Teaching to Fish, Not Giving the Fish

The prompt is built on a single principle: **empowering students to become independent debuggers**. Instead of fixing their code, the assistant guides them to discover solutions on their own. This approach builds lasting skills.

## Answering the Key Design Questions

### 1. What tone should the AI use?

**My Choice: A Friendly Teaching Assistant**

I wanted the AI to feel like a helpful TA in a computer lab—approachable and collaborative, not a stern professor or a know-it-all peer.

*   **Conversational**: It uses "let's" and "we" to make debugging feel like a team effort.
*   **Encouraging**: Bugs are treated as learning opportunities, not failures.
*   **Patient**: It never makes a student feel inadequate for making a mistake.
*   **Enthusiastic**: It shows excitement for the learning process itself.

**Why This Matters**: Debugging can be frustrating. A supportive tone is crucial for keeping students motivated when they might otherwise give up.

### 2. How much should the AI reveal versus guide?

**My Choice: 80% Guidance, 20% Direct Help**

Striking the right balance here was the most challenging part.

**Guidance (80%)**
*   Ask questions that lead to discoveries, like, "What do you expect this line to do?"
*   Suggest debugging techniques, such as, "Try adding print statements here to see the value."
*   Help develop systematic, critical thinking.

**Direct Help (20%)**
*   Offered only when a student is completely stuck.
*   Points to general areas of concern, not exact fixes.
*   Always follows up with "why" questions to ensure understanding.

I chose not to make it 90-10 because sometimes a gentle push is necessary to prevent genuine frustration and keep the learning process moving forward.

### 3. How should the assistant handle different skill levels?

**My Approach: Let the Code Tell the Story**

Instead of asking about a student's skill level, the AI infers it from their code.

**For Beginners** (Identified by simple code, basic syntax):
*   Uses everyday language and avoids jargon.
*   Focuses on one problem at a time.
*   Explains fundamental concepts clearly.
*   Frequently suggests using print statements to track variables.

**For Advanced Students** (Identified by complex logic, better practices):
*   Uses appropriate technical terms.
*   Asks about design choices and algorithmic efficiency.
*   Challenges them with potential edge cases.
*   Discusses best practices and alternative approaches.

For instance, a beginner might be asked, "What type of data is this variable storing?" while an advanced student might hear, "How might this approach perform with larger datasets?"

## Why This Design Works

### 1. It's Based on Proven Teaching Methods
I drew from established educational strategies:
*   **Socratic Method**: Fostering learning through guided questioning.
*   **Zone of Proximal Development**: Providing just enough assistance to enable progress.
*   **Growth Mindset**: Emphasizing the process of learning over just "getting it right."

### 2. It Builds Metacognitive Skills
Questions like, "What did you expect to happen, and what actually happened?" encourage students to reflect on their own thought processes. This makes them better long-term problem-solvers.

### 3. It Encourages Experimentation
By suggesting print statements and testing different approaches, the assistant teaches that debugging is an active, iterative process, not a magical fix.

## Design Choices I'm Proud Of

**The Question-First Structure**
Instead of stating, "Your loop is wrong," the AI prompts, "What happens each time this loop runs?" This forces active engagement and critical thinking.

**Specific Example Phrases**
I included concrete examples of helpful hints. This prevents the AI from being too vague ("Something is wrong here") or too direct ("Change line 5 to X").

**Focus on Process Over Product**
The ultimate goal isn't just to fix one bug; it's to teach a systematic approach for finding and resolving any bug in the future.

## What Success Looks Like

Students who use this assistant should gradually begin to:
*   Ask better debugging questions on their own.
*   Show more confidence when their code breaks.
*   Develop systematic approaches to debugging (e.g., check inputs, add prints, test small pieces).
*   Understand the "why" behind a fix, not just the "what."

## The Human Element

Programming can feel isolating when you're stuck. This prompt aims to recreate the feeling of having a patient friend by your side—one who believes you can figure it out but is there to offer a hint when you need it.

---

*This approach treats debugging as a learnable skill, not a mysterious art. Every programmer goes through this learning process; the AI just makes it a little less lonely.*
