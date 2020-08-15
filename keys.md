# op-1 keys

### tape mode

| cmd                      | desc                                                                                                                                       |
| ---                      | ---                                                                                                                                        |
| `shift + help`           | set date - time                                                                                                                            |
| `shift + tempo`          | detune notes - cents                                                                                                                       |
| `shift + tape`           | erase tape                                                                                                                                 |
| `shift + synth`          | undo edits and revert to the preset                                                                                                        |
| `shift + drum`           | undo edits and revert to the preset                                                                                                        |
| `shift + mixer`          | signal flow screen                                                                                                                         |
| `blue (default)`         | explore the tape in bits of 1/24 seconds                                                                                                   |
| `blue (while playing)`   | scrub through tape                                                                                                                         |
| `blue (while recording)` | change pitch                                                                                                                               |
| `shift + blue`           | slide a take                                                                                                                               |
| `green`                  | slide loop out                                                                                                                             |
| `shift + green`          | slide loop in                                                                                                                              |
| `white`                  | change tape speed like +1, +2, +3                                                                                                          |
| `shift + white`          | change tape speed in percentages                                                                                                           |
| `orange`                 | record level                                                                                                                               |
| `shift + orange`         | sensitive record level (change in tiny bits)                                                                                               |
| `t1-4`                   | select track                                                                                                                               |
| `shift + t1-4`           | mute/reactivate track                                                                                                                      |
| `< >`                    | rewind / forward                                                                                                                           |
| `play + < >`             | fast rewind / forward                                                                                                                      |
| `shift + < >`            | jump from bar to bar                                                                                                                       |
| `stop + <`               | jump to the very beginning of the tape.                                                                                                    |
| `stop + >`               | jump to the end of the last take on the tape, if there are multiple tracks overlapping, this will go to the longest one of the last takes. |
| `shift + play`           | reverse playback                                                                                                                           |
| `rec (hold)`             | stand ready for recording (press a key)                                                                                                    |
| `shift + rec`            | stand ready for tape roll (press play to go)                                                                                               |
| `split`                  | a take to pieces                                                                                                                           |
| `shift + split`          | join takes (joins the next closest take on either side of the active one)                                                                  |
| `lift`                   | cut or delete a take                                                                                                                       |
| `shift + lift`           | advanced lift - lift all tracks into memory.                                                                                               |
| `region lift`            | use the loop in and out points to define the part you want to lift.                                                                        |
| `drop`                   | paste a take (tape moves each time to the end of a dropped take)                                                                           |
| `sequencer`              | open/turn-off sequencer                                                                                                                    |
| `shift + sequencer`      | select sequencer mode                                                                                                                      |
| `(1) loop in`            | sets the loop in point of the tape.                                                                                                        |
| `(2) loop out`           | this sets the loop out point.                                                                                                              |
| `(3) loop toggle`        | toggles loop on and off, remembers the in and out of the previous loop                                                                     |
| `(3) (when playing)`     | recreates the previous loop                                                                                                                |
| `shift + loop toggle`    | loop current take.                                                                                                                         |
| `(4) break`              | stops the tape. if a loop is active it will continue in the background to keep the break in time.                                          |
| `(5) reverse`            | change direction of the tape.                                                                                                              |
| `(6) chop`               | a tempo locked repeat type of effect.                                                                                                      |
| `(7)-(8) memo 1-2`       | memorize any parameter in tape or mixer for instant recall.                                                                                |

### in synth (t2)

| cmd     | desc      |
| ---     | ---       |
| `shift` | play mode |

### in drum mode engine (t1)

| cmd              | desc                           |
| ---              | ---                            |
| `blue`           | pitch                          |
| `shift + blue`   | direction                      |
| `green`          | in point                       |
| `shift + green`  | fine tune in point, sensitive  |
| `white`          | out point                      |
| `shift + white`  | fine tune out point, sensitive |
| `orange`         | play mode                      |
| `shift + orange` | level                          |

### in drum mode dynamic envelope (t2)

| cmd      | desc           |
| ---      | ---            |
| `blue`   | attack level   |
| `green`  | mid-part level |
| `white`  | release level  |
| `orange` | adjust region  |

### in synth and drum mode

| cmd             | desc                                                        |
| ---             | ---                                                         |
| `1-8`           | instant access keys to sounds                               |
| `shift + synth` | undo edits and tweaks (done with t1-4)                      |
| `shift + 1-8`   | change the sound attached to the instant access key         |
| `shift + t1-4`  | change the modules of the sound without changing the sound. |
| `< >`           | octave shift                                                |

> for example, shift + t1 will change the synth engine but it will keep the tweaks and edits you made on the sound, contrary to shift + 1, which will change the sound itself by selecting a sound from one of the synth engines thus making you lose all the tweaks and edits you made.

### in mixer mode

| cmd             | desc               |
| ---             | ---                |
| `shift + mixer` | signal flow screen |

--------------

sourced from an [operator-1.com thread](https://www.operator-1.com/index.php?p=/discussion/2271/all-key-combinations-and-functions-of-op-1)
