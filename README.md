# connect-github

Upload a local file to the root of a GitHub repository. Set these environment
variables before running:

- `GITHUB_USERNAME`: the repository owner
- `GITHUB_REPOSITORY`: the repository name
- `GITHUB_TOKEN`: a token with permission to write repository contents

For example, in Command Prompt (`cmd.exe`):

```bat
set GITHUB_USERNAME=your-username
set GITHUB_REPOSITORY=your-repository
set GITHUB_TOKEN=your-token
cargo run -- .\file.txt
```

Or in PowerShell:

```powershell
$env:GITHUB_USERNAME = "your-username"
$env:GITHUB_REPOSITORY = "your-repository"
$env:GITHUB_TOKEN = "your-token"
cargo run -- .\file.txt
```

The file is uploaded using its local filename. If a file with that name already
exists at the repository root, the upload updates it.
