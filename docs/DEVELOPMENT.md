# Development notes

## Layout

- `public/`: browser markup, styles, and interaction code.
- `src/server.mjs`: loopback HTTP server and JSON routes.
- `src/planner.mjs`: input validation, activity filtering, and planning.
- `src/model.mjs` and `src/model-config.mjs`: model configuration and CPU ranking.
- `src/discovery.mjs`: optional discovery adapter, disabled in the application.
- `data/activities.json`: activity catalog.
- `tests/`: Node.js tests.
- `scripts/`: setup and verification utilities.

The default port is 4317. Set `PORT` to an integer between 1024 and 65535 to change it. The server binds to `127.0.0.1` and checks the request host and origin.

`GET /api/status` reports readiness and mode. `POST /api/plan` accepts a JSON planning request. The browser client contains the request format used by the interface.

The configured model is the quantized ONNX export of all-MiniLM-L6-v2 from Xenova, pinned to revision `751bff37182d3f1213fa05d7196b954e230abad9`. Model weights and installed dependencies are not committed.

Files in `evidence/` and the retained manifests originate from the source repository. They describe upstream observations, not new validation of this copy. Some historical references point to Markdown or license files excluded from this copy. Model setup may download external model documentation separately.
