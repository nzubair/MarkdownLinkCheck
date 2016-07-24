MarkdownLinkCheck
=================

This is a simple PowerShell module to check links correctness in your markdown files.
It supports both absolute and relative links.
The primary scenario that it targets is verifing markdown docs hosted on GitHub.

The heavy lifting of parsing markdown is done by [markdig](https://github.com/lunet-io/markdig).

This is a very early work.
Markdig.dll committed directly to this repo to make build process simpler.
It should be done more elegantly in the future.

Usage
-----

To check all markdown links in your project, run these commands in the root of your repo

```powershell
> Import-Module MarkdownLinkCheck
> Get-BrokenMarkdownLink
```

You can pass path as a parameter

```powershell
> Get-BrokenMarkdownLink -Path .\docs
```

If you want to use the module in CI, you may find useful ability to throw exception,
if any broken links are found

```powershell
> Get-BrokenMarkdownLink -Throw
```

