# Task Manager Application (Context API + useReducer)

A Task Manager app built with React's Context API and useReducer hook for global state management.

## Features

- Add new tasks via input field
- Mark tasks as complete/incomplete (checkbox toggle)
- Edit task text inline
- Delete individual tasks
- Clear all tasks at once
- Live summary showing total and completed task count
- Responsive design with hover effects and completed-task styling

## Tech Stack

- React (Vite)
- Context API (global state)
- useReducer (state logic)
- Plain CSS

## Project Structure

```
src/
  context/
    TaskContext.jsx     -> Context + Provider setup
  reducer/
    taskReducer.js       -> Action types + reducer logic
  components/
    TaskInput.jsx         -> Add task form
    TaskList.jsx           -> Renders all tasks
    TaskItem.jsx            -> Single task (edit/delete/toggle)
    TaskSummary.jsx          -> Total/completed count + clear all
  App.jsx
  App.css
```

## How State Flows

1. `TaskProvider` wraps the whole app and creates state via `useReducer`
2. Any component calls `useTaskContext()` to access `state` and `dispatch`
3. Components dispatch actions (e.g. `{ type: "ADD_TASK", payload: "..." }`)
4. The reducer (`taskReducer.js`) processes the action and returns new state
5. All components re-render automatically with updated state — no prop drilling

## How to Run Locally

```bash
npm install
npm run dev
```

## Live Link
[deploy karne ke baad yahan link daalna]