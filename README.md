# dsh-multi-lang-ui-locale-fix

Patched version of [dsh-multi-lang-ui](https://github.com/asd13006/dsh-multi-lang-ui) that fixes `locale` service injection for DeepSeek Harness 0.1.2-rc.x.

Adds these languages to the DSH web UI:
- Traditional Chinese
- Japanese
- Korean
- French
- German
- Spanish

## Install

```powershell
dsh plugin --profile web add github:shinzarou-eng/dsh-multi-lang-ui-locale-fix
```

## What changed

```diff
-    const inject = [];
+    const inject = ["locale"];
```

This is required because DSH 0.1.2-rc.x only injects the `locale` service into client plugins that declare it.

## License

MIT
