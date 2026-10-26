# Zamma for Claude

Zamma is a project and task management app. This plugin connects Claude to your Zamma workspace, so you can ask about your work in your own words and have Claude update it: what is due this week, what is overdue, where a task stands, who is on a board.

Claude works with your permissions. It sees only the projects, departments and tasks you can open in Zamma, and a change Zamma would refuse you is refused here too.

## What you can do

- Search the workspace: tasks, projects, departments, road map steps, people and comments.
- See the tasks assigned to you, narrowed to this week, to what is overdue, or to a priority.
- Read a task in full: status, section, priority, due date, labels, assignees and description.
- Create projects, tasks, sections, labels, road map steps and milestones.
- Update tasks: rename them, set their status, priority, due date, labels and description, move them to another section, assign them, comment on them and mark them completed.
- Plan the road map: rename and move steps and milestones.
- Change a member's role on a board.

Deleting projects, steps and milestones, inviting people and removing them from a board stay in the Zamma app: Claude cannot do them.

## Installing

In Claude Code:

```
/plugin install zamma --marketplace ZammaApp/zamma
```

On Claude Code before 2.1.275, add the marketplace first, then install:

```
/plugin marketplace add ZammaApp/zamma
/plugin install zamma@zamma
```

## Connecting

You need a Zamma account. The first time Claude uses Zamma, it opens Zamma's sign-in page in your browser:

1. Sign in to Zamma with the code Zamma emails you, or with your company's login.
2. Choose the workspace, and whether Claude may only read or may also make changes.
3. Press **Allow**.

When Claude may make changes, it asks you before each one.

To disconnect, open **Ask AI ▸ Connect AI tools** in Zamma and press **Disconnect** next to the connection. Claude loses access at its next request.

## Example requests

- "What's due for me this week?"
- "Which of my tasks are overdue?"
- "Add a task to the Website project to review the launch plan, due Friday."
- "Move WEB-12 to In progress and tell the team in a comment."

## What this plugin runs and sends

The plugin runs nothing on your computer. It adds one remote MCP server, Zamma's, at `https://api.zamma.dev/mcp`, and Claude connects to nothing else through it. Claude sends that server your requests to Zamma's tools, such as a search or a new task, and the server answers with your workspace's data. Signing in uses OAuth on `https://api.zamma.dev`. No token or password is stored in the plugin.

## Help and policies

- Help: [zamma.dev/support](https://zamma.dev/support), or write to hello@zamma.dev
- Privacy policy: [zamma.dev/privacy](https://zamma.dev/privacy)
- Terms of service: [zamma.dev/terms](https://zamma.dev/terms)
