# Socket and import review

## Fixed files

- `client/src/component/Editorpage.js`
- `client/src/socket.js`

## Changes made

- Kept all React hooks in one import: `useEffect`, `useRef`, and `useState`.
- Combined React Router hooks into one import and corrected `useparams` to `useParams`.
- Restored `navigate`, `copied`, and `setCopied`, which are used later in the component.
- Initialized the socket once per room/user and disconnect it when the page unmounts.
- Corrected Socket.IO options and supplied them to `io()`.
- Uses `http://localhost:5000` if `REACT_APP_BACKEND_URL` is not set.

## Optional environment setting

Create `client/.env` when the backend is not local:

```env
REACT_APP_BACKEND_URL=http://localhost:5000
```

Restart the client development server after editing `.env`.
