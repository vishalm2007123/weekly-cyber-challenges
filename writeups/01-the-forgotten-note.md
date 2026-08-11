# Writeup — Challenge #01: The Forgotten Note

## Intended skills

- Basic file inspection
- Metadata analysis
- Base64 decoding

## Step 1: Inspect the file

Start by identifying the file:

```bash
file forgotten_note.png
```

Then inspect its metadata:

```bash
exiftool forgotten_note.png
```

Look for an unusual metadata field containing an encoded value.

## Step 2: Decode the value

The hidden value is Base64 encoded:

```text
d2Vla2x5Q1RGe2ZpcnN0X3N0ZXBfaW50b19jeWJlcn0=
```

Decode it with:

```bash
echo 'd2Vla2x5Q1RGe2ZpcnN0X3N0ZXBfaW50b19jeWJlcn0=' | base64 -d
```

The result is:

```text
weeklyCTF{first_step_into_cyber}
```

## Flag

`weeklyCTF{first_step_into_cyber}`

