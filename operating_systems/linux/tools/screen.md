# Screen Cheatsheet

This cheatsheet covers the basic commands and shortcuts for the Screen command in Linux. Screen is a powerful tool that allows you to run multiple terminal sessions within a single console and detach/reattach them at any time.

## Basic Commands

| Command      | Description                                 |
| ------------ | ------------------------------------------- |
| screen       | Start a new Screen session.                 |
| screen -r    | Reattach to a detached Screen session.      |
| screen -ls   | List all available Screen sessions.         |
| screen -d    | Detach a running Screen session.            |
| screen -D    | Detach and logout a running Screen session. |
| Ctrl + A + D | Detach a running Screen session.            |
| exit         | Exit the current Screen session.            |

## Session Management

| Command      | Description                                   |
| ------------ | --------------------------------------------- |
| Ctrl + A + C | Create a new Screen window.                   |
| Ctrl + A + N | Switch to the next Screen window.             |
| Ctrl + A + P | Switch to the previous Screen window.         |
| Ctrl + A + " | List all available Screen windows.            |
| Ctrl + A + S | Split the current Screen window horizontally. |
| Ctrl + A +   | Split the current Screen window vertically.   |
| Ctrl + A + X | Remove the current Screen region.             |

## Other Commands

| Command      | Description                  |
| ------------ | ---------------------------- |
| Ctrl + A + ? | Display the help screen.     |
| Ctrl + A + Z | Suspend a Screen session.    |
| Ctrl + A + : | Enter Screen command prompt. |

## Additional Resources

For more information about using Screen, consult the official Screen documentation:

- [GNU Screen Official Documentation](https://www.gnu.org/software/screen/manual/)
