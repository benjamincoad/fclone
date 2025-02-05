# fclone - File Clone Utility

A streamlined command-line tool for copying files while preserving metadata. Designed for quick and reliable file operations with built-in error handling.

## Features

- 📄 Copy files with optional renaming
- 📂 Automatic destination directory creation
- 🔄 Preserves file metadata and timestamps
- ⚠️ Built-in error handling for common scenarios
- 🛡️ Safe operation with existence checks

## Installation

```bash
# Clone the repository
git clone https://github.com/benjamincoad/fclone.git

# Make the script executable
chmod +x fclone
```

## Usage

```bash
# Basic file clone
./fclone source.txt /destination/folder/

# Clone with new name
./fclone source.txt /destination/folder/ --name new_name.txt

# Full command format
./fclone SOURCE DESTINATION [--name NEW_NAME]
```

## Command Line Options

- `source`: Source file to clone
- `destination`: Destination folder
- `-n, --name`: New name for the cloned file (optional)

## Examples

```bash
# Clone a file to another directory
./fclone document.pdf ~/Documents/backup/

# Clone and rename
./fclone image.jpg ~/Pictures/ --name vacation_photo.jpg

# Clone to new directory (creates directories automatically)
./fclone config.json ~/projects/new_project/config/
```

## Error Handling

fclone includes robust error handling for common scenarios:
- Source file not found
- Destination file already exists
- Permission errors
- Invalid paths

## Use Cases

- Backup creation
- File organization
- Project setup
- Content management
- File distribution

## Technical Details

- Uses `shutil.copy2` to preserve metadata
- Creates destination directories automatically
- Validates paths before operations
- Returns meaningful error messages

## License

MIT License - feel free to use and modify as needed!

## Contributing

Contributions are welcome! Feel free to submit issues and pull requests.
