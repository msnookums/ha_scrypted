# Scrypted Custom Component for Home Assistant

The Scrypted Custom Component for Home Assistant adds support for Scrypted NVR cards.

## Scrypted Setup

First, retrieve a token so Home Assistant can access Scrypted.

1. Open the Terminal in the Sidebar in Scrypted.
2. Run `npx scrypted login`.
3. Log in with your Scrypted credentials for your user token.

Example:

```
koush@Koushik-MacStudio nvr-electron % npx scrypted login
username: koush
password: ********
login successful. token: 28d12b0b97cd99c3f0808cb7a78d08ef
```

## Home Assistant Setup

1. Install this repository using HACS.
2. Edit `configuration.yaml` and add the following (adjust local IP as necessary):

```yaml
scrypted:
    host: 192.168.2.124:10443
    token: 28d12b0b97cd99c3f0808cb7a78d08ef

# This section is optional. Add Scrypted to the drawer within the HA dashboard for quick access.
panel_iframe:
    router:
    title: "Scrypted"
    icon: mdi:memory
    url: "/api/scrypted/"
```
