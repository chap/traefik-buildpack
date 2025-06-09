# Traefik Heroku Buildpack

This buildpack installs [Traefik](https://traefik.io/) on Heroku. It's designed to work with Heroku's classic buildpack API.

## Usage

Add the buildpack to your Heroku app:

```bash
heroku buildpacks:add https://github.com/yourusername/traefik-buildpack
```

## Configuration

The buildpack will:
1. Install Traefik v2.10.4
2. Set up a basic configuration in `.traefik/traefik.yml`
3. Configure Traefik to run as the web process

### Environment Variables

- `PORT`: The port Traefik will listen on (defaults to 8080)

## Custom Configuration

You can customize Traefik's configuration by modifying the `.traefik/traefik.yml` file in your application. The buildpack will use this configuration file when starting Traefik.

## License

MIT