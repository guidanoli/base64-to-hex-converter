# Base64 to Hexadecimal Converter

Converts strings in Base64 to Hexadecimal inside JSON files.

## Example

Consider the following JSON file called `data.json`.

```json
{
  "mostRecentMachineHash": {
    "data": "BAAAhWHqhD6t35WDLbQjCNThk04glwBqEGfmh27rkoA="
  },
  "mostRecentVouchersEpochRootHash": {
    "data": "XhaRbdkr3XQD9FDIl/N8MDNG7z9LrT8YmigcNvqWnMY="
  },
  "mostRecentNoticesEpochRootHash": {
    "data": "WJfJG6VyF4ndZkW5Z8/UGfd8ALPov88EcFpOyu1wZ9Q="
  },
  "processedInputs": [
    {
      "mostRecentMachineHash": {
        "data": "VT/WlH6kqOvLt7/e3gOrAQriU7Lgq8QtZD0yh4jeAjc="
      },
      "voucherHashesInEpoch": {
        "targetHash": {
          "data": "S0oviQGm0hoFsu01ead/1odUJQO8b09Q5ZGBa6E0wEM="
        },
        "rootHash": {
          "data": "XhaRbdkr3XQD9FDIl/N8MDNG7z9LrT8YmigcNvqWnMY="
        }
      },
      "reports": [
        {
          "payload": "jcIadw=="
        }
      ]
    }
  ]
}
```

If we run `python -m b64to16 data.json`, we get the following output.

```json
{
  "mostRecentMachineHash": {
    "data": "0x0400008561ea843eaddf95832db42308d4e1934e2097006a1067e6876eeb9280"
  },
  "mostRecentVouchersEpochRootHash": {
    "data": "0x5e16916dd92bdd7403f450c897f37c303346ef3f4bad3f189a281c36fa969cc6"
  },
  "mostRecentNoticesEpochRootHash": {
    "data": "0x5897c91ba5721789dd6645b967cfd419f77c00b3e8bfcf04705a4ecaed7067d4"
  },
  "processedInputs": [
    {
      "mostRecentMachineHash": {
        "data": "0x553fd6947ea4a8ebcbb7bfdede03ab010ae253b2e0abc42d643d328788de0237"
      },
      "voucherHashesInEpoch": {
        "targetHash": {
          "data": "0x4b4a2f8901a6d21a05b2ed3579a77fd687542503bc6f4f50e591816ba134c043"
        },
        "rootHash": {
          "data": "0x5e16916dd92bdd7403f450c897f37c303346ef3f4bad3f189a281c36fa969cc6"
        }
      },
      "reports": [
        {
          "payload": "0x8dc21a77"
        }
      ]
    }
  ]
}
```

We can also stream the JSON input through standard input, like `cat data.json | python -m b64to16`.

## Help

Run `python -m b64to16 -h`
