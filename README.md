# @/read

For reading user input from stdin. Similar to the `readline` builtin's `question()` method, but with a
few more features.

## Usage

```typescript
import read from "@astronautlabs/read";
try {
  const result = await read(options)
} catch (err) {
  console.error(err);
}
```

## Options

Every option is optional.

* `prompt` What to write to stdout before reading input.
* `silent` Don't echo the output as the user types it.
* `replace` Replace silenced characters with the supplied character value.
* `timeout` Number of ms to wait for user input before giving up.
* `default` The default value if the user enters nothing.
* `edit` Allow the user to edit the default value.
* `terminal` Treat the output as a TTY, whether it is or not.
* `input` Readable stream to get input data from. (default `process.stdin`)
* `output` Writable stream to write prompts to. (default: `process.stdout`)

If silent is true, and the input is a TTY, then read will set raw
mode, and read character by character.

## Contributing

Patches welcome.
