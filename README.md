# Discord Bot - Roster Management

This is a Discord bot designed to manage a simple roster of players. The bot allows server members to add, remove, view, and clear players from a roster.

## Features
- **Add Players**: Add a new player to the roster.
- **Remove Players**: Remove an existing player from the roster.
- **View Roster**: Display the current roster, including player count.
- **Clear Roster**: Clear the entire roster.
- Persistent storage of the roster using a JSON file.

## Setup and Installation

### Prerequisites
- Python 3.7+
- `discord.py` library

### Installation Steps

1. **Clone the Repository**:
   ```bash
   git clone https://github.com/your-username/discord-bot-roster.git
   cd discord-bot-roster
   ```

2. **Install Dependencies**:
   Install the required libraries by running:
   ```bash
   pip install discord.py
   ```

3. **Create the `roster.json` File**:
   If the file doesn't exist, it will be created automatically when the bot starts. Alternatively, create it manually:
   ```bash
   echo [] > roster.json
   ```

4. **Add Your Bot Token**:
   Replace `YOUR_BOT_TOKEN` in the `main.py` file with your Discord bot token:
   ```python
   bot.run('YOUR_BOT_TOKEN')
   ```
   You can get your bot token from the [Discord Developer Portal](https://discord.com/developers/applications).

5. **Run the Bot**:
   Start the bot by running:
   ```bash
   python main.py
   ```

## Commands

### `!add <player_name>`
Adds a player to the roster.
- Example: `!add John`
- Response: `Added John to the roster!`

### `!remove <player_name>`
Removes a player from the roster.
- Example: `!remove John`
- Response: `Removed John from the roster!`

### `!roster`
Displays the current roster and the number of players.
- Example:
  ```
  Current Roster:
  1. John
  2. Jane

  Total players: 2/10
  ```

### `!clear`
Clears the entire roster.
- Response: `Roster has been cleared!`

## File Structure
```
.
├── main.py        # Main bot script
├── roster.json    # Stores the roster data
├── README.md      # Project documentation
```

## Notes
- The roster size is limited to **10 players**. You can change this limit by modifying the `ROSTER_SIZE` constant in `main.py`.
- Ensure the `roster.json` file is in the same directory as `main.py`.

## Contributing
If you'd like to contribute, feel free to fork the repository and submit a pull request.

## License
This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

---

### Disclaimer
Remember to keep your bot token private! Never share it publicly or commit it to version control.

