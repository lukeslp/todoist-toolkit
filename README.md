# Todoist Toolkit

Command-line toolkit for managing your Todoist tasks from the terminal.

## Installation

```bash
pip install todoist-toolkit
```

## Setup

Get your API token from [Todoist Settings](https://todoist.com/app/settings/integrations/developer):

```bash
export TODOIST_API_KEY="your-api-key-here"
```

Add to `~/.bashrc` or `~/.zshrc` for persistence:

```bash
echo 'export TODOIST_API_KEY="your-api-key"' >> ~/.bashrc
```

## Usage

```bash
# List tasks
todoist tasks
todoist tasks -p "Work"              # Filter by project

# Projects
todoist projects

# Add tasks
todoist add "Buy groceries"
todoist add "Meeting" -d "tomorrow 3pm" -P 4   # High priority, with due date

# Complete tasks
todoist complete TASK_ID

# Delete tasks
todoist delete TASK_ID

# View task details
todoist get TASK_ID

# Update tasks
todoist update TASK_ID --content "New task name"
```

## Priority Levels

| CLI Flag | Todoist UI | API Value |
|----------|------------|-----------|
| `-P 4` | P1 (Highest) | 4 |
| `-P 3` | P2 | 3 |
| `-P 2` | P3 | 2 |
| `-P 1` | P4 (Normal) | 1 (default) |

## Command Aliases

- `tasks` = `ls`, `list`
- `projects` = `proj`
- `add` = `new`, `create`
- `complete` = `done`, `close`, `finish`
- `delete` = `rm`, `remove`
- `get` = `show`, `view`
- `update` = `edit`, `modify`

## License

MIT License - see LICENSE file for details.

## Author

Luke Steuber - [lukesteuber.com](https://lukesteuber.com)
