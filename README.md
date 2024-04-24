# Blue_Tech_Cyberpunk Home Assistant Theme
> Forked Cyberpunk 2077 Theme by @flejz >> Blue_Tech_Cyberpunk by @rgsaura

![Screenshot 2024-04-24 at 12 29 48](https://github.com/rgsaura/Blue_Tech_Cyberpunk/assets/16281075/4068cf93-4572-4794-8281-d4506556e463)
![Captura 2024-04-24 a las 12 30 08](https://github.com/rgsaura/Blue_Tech_Cyberpunk/assets/16281075/a875873b-66c6-4bd9-adeb-b10c51ec2ece)


---

> The Cyberpunk 2077 Theme by @flejz

## Reference GUI

![Reference](https://raw.githubusercontent.com/flejz/hass-cyberpunk-2077-theme/master/docs/reference.png)

## Screenshots

### Overview

![Theme - Overview](https://raw.githubusercontent.com/flejz/hass-cyberpunk-2077-theme/master/docs/theme-overview.png)

### Logbook

![Theme - Logbook](https://raw.githubusercontent.com/flejz/hass-cyberpunk-2077-theme/master/docs/theme-logbook.png)

### Developer Tools

![Theme - Developer Tools](https://raw.githubusercontent.com/flejz/hass-cyberpunk-2077-theme/master/docs/theme-developer-tools.png)

### Configuration

![Theme - Configuration](https://raw.githubusercontent.com/flejz/hass-cyberpunk-2077-theme/master/docs/theme-configuration.png)

### Profile

![Theme - Profile](https://raw.githubusercontent.com/flejz/hass-cyberpunk-2077-theme/master/docs/theme-profile.png)

## Font

Optionally you can add the [Rajdhani](https://fonts.google.com/specimen/Rajdhani) font as a stylesheet resource to have yet a closer experience:

`https://fonts.googleapis.com/css2?family=Rajdhani:wght@500&display=swap`

![Theme - Overview with font](https://raw.githubusercontent.com/flejz/hass-cyberpunk-2077-theme/master/docs/theme-overview-with-font.png)

## Cyberdeck Mode - card-mod

In case you have [card-mod](https://github.com/thomasloven/lovelace-card-mod) this is what you gonna get instead:

![Theme - Cyber Overview](https://raw.githubusercontent.com/flejz/hass-cyberpunk-2077-theme/master/docs/theme-overview-card-mod.png)


You can reflect the `ha-card` state by using `jinja2` templating  by adding the following `card_mod` snippet to your card:

```css
# light entity example

- type: light
  entity: light.01234
  name: Desk
  card_mod:
    style: |
      ha-card {
        {% if is_state(config.entity, 'on') %}
        background-color: var(--cyan-color);
        {% endif %}
      }
```

Then when the entity is on (light in this example) you would see this nice overlay:

![Theme - State Overlay](https://raw.githubusercontent.com/flejz/hass-cyberpunk-2077-theme/master/docs/theme-state-overlay.png)

> PS: note that state may vary depending on your card. In that case you would just have to adapt `{% if is_state(config.entity, 'on') %}` accordingly.

## Installation

Add the following code to your `configuration.yaml` file (reboot required).

```yaml
frontend:
  ... # your configuration.
  themes: !include_dir_merge_named themes
  ... # your configuration.
```

### HACS

1. Go to the Community Store.
2. Search for `Cyberpunk 2077`.
3. Navigate to `Cyberpunk 2077` theme.
4. Press `Install`.

### Manual

Clone this repository in your existing (or create it) `themes/` folder.

```bash
cd themes/
git clone https://github.com/flejz/hass-cyberpunk-2077-theme.git
```

Or using submodules:

```bash
cd themes/
git submodule add https://github.com/flejz/hass-cyberpunk-2077-theme.git
```
