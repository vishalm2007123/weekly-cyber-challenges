# 🧩 Writeup — Challenge #02: The Wrong Cipher

## Step 1 — Decode the visible message

The file begins with:

```text
Wkh ildj lv klgghq lq wkh oljkw.
```

This is a Caesar cipher. Shifting each letter back by 3 produces:

```text
The flag is hidden in the light.
```

That is a clue, not the final flag.

## Step 2 — Inspect invisible data

The hint and quote suggest looking at information that is easy to overlook.

Running:

```bash
cat -A message.txt
```

reveals trailing spaces and tabs at the ends of the transmission lines.

For this challenge:

- space = `0`
- tab = `1`
- 8 whitespace characters = 1 byte

Extracting those bits and converting the bytes to text gives:

```text
weeklyCTF{caesar_was_here}
```

## 🚩 Flag

```text
weeklyCTF{caesar_was_here}
```

