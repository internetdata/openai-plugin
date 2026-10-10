# [<img src="https://s3.internetdata.io/internetdata-public/brand/mark.svg" alt="InternetData" height="28"/>](https://internetdata.io/) InternetData Plugin for ChatGPT and Codex

[![version](https://img.shields.io/github/package-json/v/internetdata/openai-plugin?filename=plugin.json)](CHANGELOG.md)
[![license](https://img.shields.io/github/license/internetdata/openai-plugin)](LICENSE)

The official [InternetData](https://internetdata.io) plugin for [ChatGPT](https://chatgpt.com) and [Codex](https://developers.openai.com/codex).

## Getting Started

In Codex:

```console
codex plugin marketplace add internetdata/openai-plugin
codex plugin add internetdata@internetdata
codex mcp login internetdata
```

The last line signs you in with your InternetData account, where you pick the API key Codex should use. Codex never sees the key: our MCP server uses it on your behalf. The Codex CLI, its IDE extension and Codex in the ChatGPT desktop app read the same configuration, so one install covers all three.

To disconnect Codex, run `codex mcp logout internetdata`, or remove it under Connected applications at https://app.internetdata.io/settings/account/sessions. Access ends within about a minute.

## What's in it

- The InternetData MCP server at `https://mcp.internetdata.io/mcp`.

## What it sends

The plugin runs nothing on your machine. Codex sends what you ask about to `https://mcp.internetdata.io/mcp`, which calls the InternetData API with the key you picked and returns the answer. Each request is logged against that key as any API call is. Our privacy policy is at https://internetdata.io/privacy, and questions go to support@internetdata.io.

## Other Libraries

There are official InternetData client libraries available for many languages including PHP, Python, Go, Java, and Ruby. See our GitHub at https://github.com/internetdata for more.

## About InternetData

Geolocation, anonymity, ownership and network databases for IP addresses and AS numbers, licensed as files you download and query yourself.

[<img src="https://s3.internetdata.io/internetdata-public/brand/mark.svg" alt="InternetData" height="64"/>](https://internetdata.io/)

## License

This project is licensed under the [MIT License](LICENSE).
