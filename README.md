# CalcuPico
CalcuPico a Raspberry Pi Pico powered mod to a Casio fx-85GT CW scientific calculator, replacing the solar panel with an OLED display.  
It uses the calculator's own buttons to control the UI, allowing the calculator to remain fully operational when the Pico is disconnected from power.

## Available apps
- **main.py**  
A simple app launcher.
- **snake.py**  
The iconic game of Snake.
- **wifimanager.py (Pico W series only)**  
Manage the Pico's WiFi connection.
- **wikipedia.py (Pico W series only)**  
Browse Wikipedia using the free, publicly available MediaWiki API.

## Planned apps
- **appstore.py (Pico W series only)**  
Download apps to CalcuPico without a computer.
- **settings.py**  
Easy to use settings app, this would replace `wifimanager.py` and enable a few extra features to be customized.

## Build a CalcuPico
See the [build guide](/buildguide/guide.md) for information on how to build your own CalcuPico.

## SDK overview

### Display
```python
init_display()
show("Hello")
multi_line("Line 1", "Line 2")
```

### Buttons
```python
get_button()        # returns 'UP', 'DOWN', etc.
should_exit()       # checks if BACK was pressed
clear_exit_flag()
```

### Menus
```python
run_menu_app("Title", ["Option 1", "Option 2"], [func1, func2])
```

### WiFi (Pico W series only)
```python
connect_wifi()
disconnect_wifi()
is_wifi_connected()
```

### Keyboard
```python
text = show_keyboard()
```
