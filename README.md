# What is Cava?
Cava is an audio visualizer that can display music visualizations on the terminal, making it more engaging and interactive.

# How to install it?
To install it, follow these steps:

- Update & Upgrade Package in Termux
```bash
$ apt update && apt upgrade
```

- Install 3 packages
```bash
$ apt install cava mpv pulseaudio
```

# How to configure it?
To configure, follow these steps:
<details>
	<summary>Configure Cava</summary>
	Find the text and change it as below:
	
  ```
  ; method = pulse
  ; source = 1
  ```
configuration is available at  `~/.config/cava/config`
</details>

<details>
	<summary>Custom Alias in Shell <b>(Optional)</b></summary>
	Add a special "alias" in the shell to run mpv and play songs to make it easier.
	
  ```
  alias playmusic="mpv --ao=pulse"
  ```
	
 If using bash as shell, add special "aliases" in  `~/.bashrc`  and if using zsh as shell, add them in  `~/.zshrc`  as well.

 After adding a custom "alias", it is necessary to re-login the shell or restart the Termux application.
</details>

# How to try it?
After everything is installed and configured, follow these steps:

- Open the first session in the terminal and run `mpv` to play the desired song.

 ```bash
 $ playmusic /path/to/your_music.mp3
 ```
If you didn't add a special "alias", you need to run it like this:

 ```bash
 $ mpv --ao=pulse /path/to/your_music.mp3
 ```

- Create a new session and run cava

```bash
$ cava
```
