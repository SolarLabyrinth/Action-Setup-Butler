# Action: Setup Butler

A GitHub Action to install Itch.io's Butler on a GitHub Actions runner.

> Note: Only supported on Ubuntu runners.

## Usage

This action will provide access to the butler binary on your runner's path. You can then reference that binary in other workflow steps.

```yml
- name: Setup Butler
  uses: SolarLabyrinth/Action-Setup-Butler@v1
  with:
    key: ${{ secrets.BUTLER_API_KEY }}

- name: Upload Game
  run: butler push ./build user/game:channel
```
