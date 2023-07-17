# Drew's Rust Todoist Client / TUI App 
Woo! 

---

## Just my notes and task tracking, please ignore

### e2e flows -- positive scenarios
- [x] add a todo when user data (namely, inbox id) is already stored
- [x] add a todo when user data doesn't exist (so we need to get it!)
- [x] set the api token
- [ ] complete a todo

### negative scenarios
- [x] missing api token
- [ ] cannot reach server
- [ ] server returns error
- [ ] invalid api token (may be covered by the above)

### refactors
- [x] refactor tests to be more modular (specifically for mocking)
- [ ] move stuff out of `main.rs` and into `cli.rs` or something

### other todos
- [x] add stricter clippy, including `unwrap` (replace `unwraps` with allowed `expects` in tests)
- [ ] better test organization

---

## Abstraction Ideas

### `SyncClient`
- responsible for making/returning requests
- owns sync url
- encapsulates reqwest logic

### `FileManager`
- owns data and config locations
- resposible for reading/writing from both locations
