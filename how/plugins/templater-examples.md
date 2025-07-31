# previous/next day

In my template-daily-note I use the [Templater](https://silentvoid13.github.io/Templater/) plugin to dynamically create links to the next and previous day. 

## template input
- Previous day: `[[<% tp.date.now("yyyy-MM-DD ddd", -1) %>]]`
- Next day: `[[<% tp.date.now("yyyy-MM-DD ddd", 1) %>]]`

## output on 2025-07-30
- Previous day: [[2025-07-29 Tue]]
- Next day: [[2025-07-31 Thu]]


# insert custom text block using hotkey

You can use your favorite text blocks to create templates which can be inserted with custom hotkeys. 

This can save you a lot of time and let you focus on what's relevant for you 🥳


## define template

As an example, let's create a file template-python with the text of an empty python code block and store it inside our <a href="../setup.md#templates-define-folder-location">dedicated folder to hold templates</a>. 

<img src="../../pics/template-python.png" width="300">


## define hotkey

To configure a hotkey for this new template

<img src="../../pics/templater-configure-hotkeys.png" width="400">

- define hotkey
<img src="../../pics/templater-define-hotkey.png" width="400">

## applying template

```python

```

Using the hotkey `Ctrl + Shift + P` I just inserted the empty code block above. 


```python
# Parrot sketch example
class Parrot:
    def __init__(self):
        self.dead = True

    def speak(self):
        if self.dead:
            return "This parrot is no more!"

polly = Parrot()
print("Polly says:", polly.speak())
```

### sample output

<img src="../../pics/templater-python-example.png" width="400">


