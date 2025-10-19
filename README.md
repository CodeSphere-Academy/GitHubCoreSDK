# GitHubCoreSDK

A lightweight XCFramework that exposes a simple API to retrieve a GitHub URL.

**Module**: `GithubCore`

## Install (Xcode)

- Drag `GithubCore.xcframework` into your Xcode project’s Project Navigator.
- In the add dialog, select your app target and ensure “Copy items if needed” is checked.
- Go to your app target → `General` → `Frameworks, Libraries, and Embedded Content` and set `GithubCore.xcframework` to `Embed & Sign`.

## Usage

```swift
import GithubCore

let urlString = GithubCore().getUrl()
print(urlString) // e.g., "https://github.com/…"

let githubUsers = try await GithubCore().getGithubUsers()
```

`getUrl()` returns a `String` containing the GitHub URL provided by the framework.
