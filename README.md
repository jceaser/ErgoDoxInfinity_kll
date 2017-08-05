# My Ergo dox infinity Layout #

A keyboard layout based on [0.3](https://www.overleaf.com/read/zzqbdwqjfwwf#/2477900/) of the [kll-spec](https://github.com/kiibohd/kll-spec) (see the [kll project](https://github.com/kiibohd/kll) for more information) for the [Infinity Ergodox](https://input.club/devices/infinity-ergodox/). Compile with the [KLL Controller](https://github.com/kiibohd/controller).

## Layers ##

Normally these are configured in this order for the left keyboard but on the right the first two layers are swapped meaning you get a default hardware QWERTY when plugged in to the left and a DVORAK when plugged into the right. In either case you daisy chain the other.

0. QWERTY
1. DVORAK
2. Alternate keys
3. mouse - keypad
4. navigation / game layer
5. programing
6. None / Blank
7. System, keyboard specific

## Compile ##
To use this keymap you will need to have a working copy of the kiibohd/controller, however as of 2017-08-01 the master branch does not work correctly for Infinity Ergodox. There is however a workaround that can be followed from [here](https://github.com/kiibohd/controller/issues/204#issuecomment-315766171).

These are the steps from that comment: 

1. `git clone https://github.com/kiibohd/controller`
1. `cd controller/`
1. git checkout [c7fb6d1](https://github.com/kiibohd/controller/commit/c7fb6d1c3be29de1bcb0b9c7201448e66fb2ca33)
1. `cd Keyboards/`
1. `./ergodox.bash`
1. Expect build to fail.
1. `cd ../kll`
1. git checkout [2062be0](https://github.com/kiibohd/controller/commit/2062be08e34430d523b20947e9eb5a3ec3948331)
1. `cd ../Keyboards`
1. `./ergodox.bash`
1. Customize from here and rebuild.

then add this project as an alias to

`ln -s ${base}/ErgoDoxInfinity_kll ${base}/controller/Keyboards/Mine`

----

thomas cherry 2017.