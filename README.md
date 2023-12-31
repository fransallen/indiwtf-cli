# Indiwtf CLI

Will your website be blocked by Kominfo? Let's check!

Indiwtf CLI is a tiny command-line tool written in Go that allows you to check if your website is blocked in Indonesia. It uses the [Indiwtf API](https://indiwtf.com/api) to check the accessibility status of the website in Indonesian Internet network.

You can access the web version by visiting [indiwtf.com](https://indiwtf.com). Indiwtf is also available in a [Telegram Bot](https://github.com/fransallen/indiwtf-telegram-bot) version.

## Usage

Run `indiwtf` with one or more domains:

```sh
indiwtf [domain1] [domain2] ...
```

## Examples

Check the accessibility status of a single website:

```sh
indiwtf example.com
```

Check the accessibility status of multiple websites:

```sh
indiwtf puredns.org github.com reddit.com
```

## API Token

Indiwtf CLI requires an API token to check website accessibility. You can store the API token securely in a configuration file located at `~/.indiwtf/config.json`. The program will prompt you to enter the token if it's not found in the configuration file.

To obtain an API token, please visit [indiwtf.com/pricing](https://indiwtf.com/pricing).

## Installation

Indiwtf CLI available as prebuilt binary, you can download and place it under `/usr/local/bin` folder, run:

```sh
sudo wget -O /usr/local/bin/indiwtf \
  https://github.com/fransallen/indiwtf-cli/raw/main/indiwtf
sudo chmod +x /usr/local/bin/indiwtf
```

## Uninstall

To remove Indiwtf CLI and its configuration files, follow these steps:

1. Remove the **indiwtf** binary:

```sh
sudo rm /usr/local/bin/indiwtf
```

Remove the configuration directory and file:

```sh
rm -rf ~/.indiwtf
```

## Features

- Check the accessibility status of a website based on the resolved IP address.
- Resolve IP address for a given hostname using a custom DNS server in Indonesia.
- Supports checking multiple websites in a single run.

## Development

You will need Go (version 1.16 or above).

Clone the repository:

```sh
git clone https://github.com/fransallen/indiwtf-cli.git
cd indiwtf-cli
```

To build the binary, run:

```sh
CGO_ENABLED=0 go build -o indiwtf main.go
```

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

## Acknowledgments

This project was inspired by the need to quickly check if websites are blocked in Indonesia.

## Contributing

Contributions are welcome! If you find any issues or want to add new features, please open an issue or submit a pull request.
