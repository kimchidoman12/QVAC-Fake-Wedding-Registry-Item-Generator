# QVAC Fake Wedding Registry Item Generator

Type a couple's hobby or personality trait and an on-device AI suggests an oddly specific fake registry item for it, with a deterministic absurdity meter.

## Run

```bash
npm install
npm start
```

Then open http://localhost:29420

## QVAC SDK version

`@qvac/sdk` ^0.19.0 (see `package.json`).

## How it works

Built on [Tether's QVAC SDK](https://www.npmjs.com/package/@qvac/sdk) — all inference runs on-device, no cloud call, no API key. The app loads `LLAMA_3_2_1B_INST_Q4_0` locally with `loadModel()`, generates with `completion()` (streamed via `tokenStream`), and releases the model with `unloadModel()` on shutdown.

## License

MIT
