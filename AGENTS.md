# Project Rules & Terminal Command Approval Guidelines

These permanent working rules govern all actions and terminal command executions for this Android Ludo Game project.

## 1. Terminal Command Execution Rules
- **Do not ask for approval for small or routine commands**: Run normal, safe, necessary CMD/terminal commands directly without interrupting the workflow.
- **Auto-approved routine commands include**:
  - Navigation and inspection: `cd`, `dir`, `ls`, `Get-ChildItem`, `git status`, `git diff`, `git log`.
  - Toolchain checks: `java -version`, `javac -version`, `adb devices`, `adb shell ...`.
  - Build actions: Gradle tasks such as `./gradlew assembleDebug`, `./gradlew compileDebugJavaWithJavac`, `./gradlew tasks`.
  - Deployment & Execution: Installing debug APK (`adb install -r ...`), launching app intents (`adb shell am start ...`), inspecting focus/logs (`adb logcat`, `dumpsys`).
- **Prompt for user approval ONLY for risky or high-impact operations**:
  - Deleting project files or folders.
  - Overwriting existing important files without prior alignment.
  - Changing project architecture, package structures, or converting to other technologies/frameworks.
  - Installing, uninstalling, or updating major dependencies, libraries, or system toolchains.
  - Modifying important system-wide settings or environment variables outside the active session.
  - Destructive Git operations (e.g., `git reset --hard`, `git clean -fd`, `git push --force`, deleting branches).

## 2. Explanation Requirement for Risky Actions
- If a command is potentially destructive or has significant consequences, explain why before running it and wait for explicit user approval.

## 3. Error Handling and Integrity Rules
- If any command fails, report the exact error and investigate root cause.
- Do not make unauthorized code changes or configuration changes to "hotfix" issues without user permission.
- Maintain the original native Android Java architecture.

