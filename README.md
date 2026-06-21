# Build Environment Base for Termux APK

This repository contains the compressed build environment for building the Termux APK project.

## Contents

| File | Size | Original Size | Description |
|------|------|--------------|-------------|
| `android-sdk.tar.gz` | 112 MB | 288 MB | Android SDK (build-tools 150MB + platforms 139MB) |
| `gradle-cache.tar.gz` | 667 MB | 1.1 GB | Gradle dependency cache |

**Total compressed: 779 MB** | **Original: ~1.4 GB**

## Usage

Extract to the desired location:

```bash
# Extract SDK
tar -xzf android-sdk.tar.gz

# Extract Gradle cache
tar -xzf gradle-cache.tar.gz
```

The extracted directories contain:
- `android-sdk/` — Android SDK with build-tools and platforms
- `gradle-cache/` — Gradle caches directory

### Setting up ANDROID_HOME

```bash
export ANDROID_HOME=/path/to/android-sdk
```

### Using Gradle cache

Copy the contents to `~/.gradle/caches/` or set as Gradle cache directory.
