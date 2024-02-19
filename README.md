# `todoist-tui`, a Todoist TUI & CLI App 

## Installation

I'll eventually get around to hosting this on crates.io. For now, you can clone the repo 
and manually build if you have the Rust toolchain installed.

```shell
git clone git@github.com:drewzemke/todoist-tui.git
cd todoist-tui
cargo install --path .
```


## Usage 

Get your API token from [the Todoist web app](https://app.todoist.com/app/settings/integrations/developer) first, then store it:
```shell
todoist-tui set-token <YOUR_API_TOKEN>
```

Sync your data with Todoist's servers:
```shell
todoist-tui sync
```


### TUI Usage

Launch the TUI by invoking the program with no arguments. 
(I'll add more details here at some point!)
```shell
todoist-tui 
```


### CLI Usage

Add some todos to your inbox:
```shell
todoist-tui add "Do a barrel roll!"
todoist-tui add "Use the boost to get through!"
```

List the contents of your inbox:
```shell
todoist-tui list
# [1] "Do a barrel roll!"
# [2] "Use the boost to get through!"
```

Mark a todo complete using its number in the list:
```shell
todoist-tui complete 2
```
