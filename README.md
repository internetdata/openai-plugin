# [<img src="https://s3.internetdata.io/internetdata-public/brand/mark.svg" alt="InternetData" height="28"/>](https://internetdata.io/) InternetData Plugin for ChatGPT and Codex

[![version](https://img.shields.io/github/package-json/v/internetdata/openai-plugin?filename=plugin.json)](CHANGELOG.md)
[![license](https://img.shields.io/github/license/internetdata/openai-plugin)](LICENSE)

The official [InternetData](https://internetdata.io) plugin for [ChatGPT](https://chatgpt.com) and [Codex](https://developers.openai.com/codex).

InternetData publishes IP and ASN databases: geolocation, anonymity, ownership and network data, as gzipped CSV and as MMDB. With this plugin you can ask about any of them: which ones your organization holds, what is inside each, sample rows, sizes and build dates, whether a copy you downloaded is intact, and what happened to a download that failed.

## Getting Started

In Codex:

```console
codex plugin marketplace add internetdata/openai-plugin
codex plugin add internetdata@internetdata
codex mcp login internetdata
```

The last line signs you in with your InternetData account, where you pick the API key Codex should use. Codex never sees the key: our MCP server uses it on your behalf. The Codex CLI, its IDE extension and Codex in the ChatGPT desktop app read the same configuration, so one install covers all three. Any account can look into every database. The Open ones, such as Tor IP and ASN, are licensed to every organization from the start and are free under CC BY-SA 4.0; a checksum or a download of the rest needs a license.

To disconnect Codex, run `codex mcp logout internetdata`, or remove it under Connected applications at https://app.internetdata.io/settings/account/sessions. Access ends within about a minute.

## What's in it

- The InternetData MCP server at `https://mcp.internetdata.io/mcp`, with four read-only tools: `list_databases`, `database_metadata`, `database_checksum` and `list_downloads`.
- Two skills that say how to use them well:
  - `database-files` answers which databases you hold, how big they are, whether your copy is intact and why a download failed.
  - `analyze-database` explains a database's columns and sample rows, and in Codex analyzes a downloaded copy.

## Try it

- "Which IP databases are we licensed for, and when were they last built?"
- "What columns does tor_ip_v1 have? Show me a few sample rows."
- "Does the checksum of my vpn_ip_v1.csv.gz match the published one?"
- "Our download failed last night. What happened?"

## What it sends

The plugin runs nothing on your machine. Codex sends the database ids you ask about to `https://mcp.internetdata.io/mcp`, which calls the InternetData API with the key you picked and returns the answer. Each request is logged against that key as any API call is. Our privacy policy is at https://internetdata.io/privacy, and questions go to support@internetdata.io.

## Other Libraries

There are official InternetData client libraries available for many languages including PHP, Python, Go, Java, and Ruby. See our GitHub at https://github.com/internetdata for more.

## About InternetData

Geolocation, anonymity, ownership and network databases for IP addresses and AS numbers, licensed as files you download and query yourself.

[<img src="https://s3.internetdata.io/internetdata-public/brand/mark.svg" alt="InternetData" height="64"/>](https://internetdata.io/)

## License

This project is licensed under the [MIT License](LICENSE).
