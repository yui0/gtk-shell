# Gtk shell

It's an example how to have a desktop shell client for Weston, based on a real
toolkit.

The idea is that this client, or any other based on any toolkit, can
interchangeably be used with a single desktop plugin like the [weston desktop
plugin](https://github.com/tiagovignatti/weston-desktop-plugin). Therefore,
one compositor, with a single desktop plugin can be used as a foundation for
building different shell UIs based on different graphics toolkits.

## License

You are free to get this code and use to build real GTK+ shell clients as you
wish. All you have to do is add the MIT license on your project, maintaining
the [copyright](https://github.com/tiagovignatti/gtk-shell/blob/master/LICENSE) in there.

## More

http://vignatti.wordpress.com/2013/03/05/ui-customization-on-wayland/

## Installation

```
$ sh autogen.sh
$ make
# mv shell/weston-gtk-shell /usr/libexec
```

Add following lines to weston.ini.
```
[core]
modules=shell-helper.so,xwayland.so

[shell]
client=/usr/libexec/weston-gtk-shell
```
