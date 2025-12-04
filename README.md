# Action: Setup Butler

A GitHub Action to install Itch.io's Butler on an Ubuntu GitHub Actions runner.

NOTE: Butler recently changed their CI domain name. Update to v2 if your builds are failing.

## Usage

This action will provide access to the butler binary on your runner's path. You can then reference that binary in other workflow steps.

```yml
- name: Setup Butler
  uses: solarlabyrinth/action-setup-butler@v2
  with:
    key: ${{ secrets.BUTLER_API_KEY }}

- name: Upload Game
  run: butler push ./build user/game:channel
```
