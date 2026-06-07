# Mini Git — CLI Version Control System

A command-line version control system built from scratch in Java 17, mirroring core Git internals with content-addressable storage.

## Features
- `init` — initialize a new repository
- `add` — stage files for commit
- `commit` — snapshot staged changes with a message
- `log` — view commit history
- `diff` — compare file changes between commits
- SHA-1 hashing for blobs, trees, and commit objects
- Branching model with HEAD pointer management
- Commit graph traversal

## Tech Stack
`Java 17` `File I/O` `SHA-1 Hashing` `OOP` `SOLID Principles`

## Project Structure

```
src/
└── main/
    └── java/
        └── vcs/
            ├── Main.java
            ├── commands/
            │   ├── InitCommand.java
            │   ├── AddCommand.java
            │   ├── CommitCommand.java
            │   ├── LogCommand.java
            │   └── DiffCommand.java
            ├── storage/
            │   └── ObjectStore.java
            └── model/
                ├── Blob.java
                ├── Tree.java
                └── Commit.java
```

## How to Run
```bash
javac -d out src/main/java/vcs/**/*.java src/main/java/vcs/*.java
java -cp out vcs.Main init
java -cp out vcs.Main add README.md
java -cp out vcs.Main commit -m "first commit"
java -cp out vcs.Main log
```

## Concepts Demonstrated
- Content-addressable storage using SHA-1
- File I/O for persistent object storage
- SOLID principles with separated parsing, storage, execution layers
- Branching model with HEAD pointer
- Commit graph traversal
