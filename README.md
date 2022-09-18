# sprit

I/O interface between a Raspberry Pi and a Dynamixel XL-320 servo.
Other Dynamixel models may work too, as well as other serial bus
servos such as those from Hiwonder -- haven't tested.

The Sprit is similar to the Poppy Project's Pixl board:

- https://www.poppy-project.org/en/
- https://github.com/poppy-project/pixl/blob/master/circuit_maker/Pixl.PDF

The main differences between the Sprit and Pixl are in the power
subsystem -- the Sprit is optimized for stationary use, while the Pixl
is optimized for mobile use on batteries:

| load      | Sprit                | Pixl                        |
|-----------|----------------------|-----------------------------|
| Pi        | USB                  | 7V barrel jack or batteries |
| 7V servos |                      | 7V barrel jack or batteries |
| 8V servos | 10.5-18V barrel jack |                             |

- Sprit accepts anything from 10.5 to 18V via the barrel jack and
  regulates that down to 8V power for the servos.  Sprit does not
  provide power for the Pi, so the Pi must be powered via USB.
- Pixl accepts 7V from barrel jack or batteries, passes that
  unregulated to the servos, and regulates it down to 5V to power the
  Pi, so the Pi does not need to be plugged into USB power.

## Oshpark prototype v0.2 bare board

<a href="https://oshpark.com/shared_projects/FYFJ6RjU"><img src="https://oshpark.com/packs/media/images/badge-5f4e3bf4bf68f72ff88bd92e0089e9cf.png" alt="Order from OSH Park"></img></a>
