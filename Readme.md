# 🧠 Multi‑Agent Fitness & Nutrition Recommendation System

An Agentic AI driven personal fitness assistant that analyzes meals, generates workouts, evaluates your progress, and dynamically chooses tools/agents based on natural language prompts.

Repository: [AgentAI](https://github.com/4RN4B/AgentAI.git) — GitHub name: AgentAI

> Note: This project in this repository is provided as a single notebook file. OpenAI APIs are not used in this copy. No pip install or full project structure is required to view the notebook.

---

## 1. Problem Overview

Most fitness/nutrition tools today are:

-   Static (pre‑defined meal/workout templates)
-   Non‑adaptive (no reasoning over user goals or lifestyle)
-   Require structured input instead of natural language
-   Cannot coordinate multiple tasks (diet → workout → evaluation)
-   Lack autonomy (only respond to direct instructions)

Challenge: Build an intelligent system that behaves more like a coach, not a passive chatbot.

---

## 2. Solution Summary

This project implements an Agentic AI multi‑agent ecosystem where several autonomous agents collaborate:

-   FoodAgent → analyzes meals, calories, micronutrients
-   WorkoutAgent → creates personalized 5‑day training plans
-   EvaluationAgent → scores calorie alignment & workout variety
-   ReminderAgent → hydration & stretching reminders
-   MealAgent → LLM‑powered meal creation
-   Orchestrator → routes tasks to agents (sequential/parallel/loop)
-   LLM Tool Router → interprets natural language and chooses tools

Example prompt:
"Make me a hypertrophy workout, analyze my meals, and remind me to drink water."  
System determines: ["workout", "nutrition", "reminder_water"] and executes the appropriate agents.

---

## 3. System Architecture

High‑level flow:

User Prompt → LLM Tool Router → Selected Agents (FoodAgent, WorkoutAgent, EvaluationAgent, ReminderAgent, MealAgent) → Orchestrator → Results JSON

---

## 4. Agents Explained

-   FoodAgent: reads meals (CSV or free text), estimates calories, computes macros & micros, returns recommendations.
-   WorkoutAgent: generates 5‑day programs by goal; suggests reps, sets, and estimated weights.
-   EvaluationAgent: scores calorie alignment, workout variety, average set volume.
-   ReminderAgent: schedules simple reminders (water/stretch).
-   MealAgent: generates meals via an LLM (not required for local notebook).
-   Orchestrator: supports Sequential, Parallel, and Loop execution styles.

---

## 5. Agentic AI Features

-   Multi‑Agent Collaboration
-   LLM‑Driven Tool Selection (conceptual in the notebook)
-   Context Engineering & Memory (summarization examples)
-   Long‑Running Agents (LoopAgent concept)
-   Tool‑Use with LLM Integration (not active in this notebook copy)

---

## 6. Example Interaction (Notebook)

Example prompts and expected agent routing are shown inside the notebook. Example:  
Input: "evaluate my meals and create a hypertrophy plan"  
Router selects: ["nutrition", "evaluate", "workout"]  
Orchestrator executes and returns a results JSON.

---

## 7. Project Structure (Notebook-focused)

This repository is organized around a single notebook. The notebook documents the conceptual modules:

-   A single notebook file demonstrating agents, orchestrator logic, and sample outputs.
-   Supporting data (if included) is bundled alongside the notebook.

(There is no full package structure required for this copy.)

---

## 8. Future Enhancements

-   Sleep recommendation agent
-   Stress & recovery scoring
-   Habit‑streak agent
-   Cost‑optimized meal planning
-   Video‑based posture/form agent

---

## 9. License

MIT License
