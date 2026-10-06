# Teaching with the Smart Classroom Lab

## Slide mapping

| Website view | Source slides | Suggested demonstration |
| --- | --- | --- |
| Classroom | 5–9 | Add three students, raise temperature to 30 °C, inspect sensor and actuator roles. |
| Network | 5, 11, 13 | Send a reading, disconnect, send two more, then reconnect. |
| Data processing | 10 | Compare the batch mean before and after validation, then aggregate. |
| Edge & cloud | 12 | Compare an 8 ms local decision with a cloud round trip, then test an outage. |
| Five V’s | 16–18 | Change each control and ask which aspect of the data has changed. |
| Check yourself | 14, 18 | Ask students to choose and explain their answer before revealing feedback. |

## Classroom

Automatic rules switch lights on when the room is occupied. Cooling runs only when the room is occupied and the temperature exceeds 27 °C. Disabling automatic rules turns these two automated outputs off. The lamp has a separate manual smart-plug control.

The presence sensor reports presence, not a head count. The student slider supplies simulated presence. The aircon is an actuator. Not every individual device has all four capabilities to the same degree.

A cloud cooling command demonstrates a manual override. Changing a classroom input reapplies the automatic rule. Cloud connectivity and local automatic control are separate concepts.

## Network

Temperature uses Zigbee and occupancy uses BLE in this example. The gateway forwards an internet message to the platform using HTTPS/TLS. Real IoT designs may use MQTT/TLS or other suitable protocols. The smart plug uses a Wi-Fi router path directly.

Readings are buffered when students click “Send a reading” during an outage. On reconnection the example reports uploading the buffered messages and clears its count. An offline cloud command cannot reach the actuator. Classroom local rules remain available.

The diagram continuously animates illustrative packet traffic. The send controls produce explicit simulated messages in the event log.

## Data processing

The six readings are 26, 25, 20,000, 24, 27 and 25 °C in an intentionally scrambled time order. The teaching validation range is −10 to 60 °C. Validation flags and excludes the impossible 20,000 °C record from output.

After validation the mean is **25.4 °C**. Aggregation sends one batch mean rather than five individual records. Sorting by timestamp has no effect on the mean. The source slide’s sensor ordering example is broader than this demonstration of time ordering.

## Edge and cloud

Local total response is **8 ms**. Cloud total response is **network round trip + 20 ms**. The deadline is **10 ms**. These values illustrate the source slide’s factory example and are not measured product specifications. Both animations slow time by the same factor of 40. Internet settings are captured when a run begins.

Actual safety-critical machinery requires appropriate engineered and validated safety systems; this page illustrates computation location only.

## Five V’s

- **Volume:** four sensors per room, one reading per minute, 100 bytes per record. One room for one day gives 5,760 records. The blocks represent proportional accumulated records, not a fixed definition of “big.”
- **Variety:** numeric records and occupancy events are structured. Images and audio are unstructured content with possible structured metadata. Neither camera nor audio capture occurs.
- **Velocity:** processor capacity is 30 readings/second. An arrival rate above 30 builds a queue. Below 30 drains an existing queue. Simulation advances only when this view is selected and motion is running.
- **Veracity:** representative sensors read 28 °C and sensors beside a vent read 22 °C. Moving all five sensors to the vent produces a 6 °C underestimate. Range validation cannot catch this plausible placement bias.
- **Value:** cooling is scheduled for eight hot hours but the room is occupied for four. Occupancy-based control avoids four unnecessary operating hours. Operating time avoided is not a measured energy saving.

## Quiz answers

1. Device
2. Gateway
3. Platform
4. Volume
5. Variety
6. Velocity
7. Veracity
8. Value

## Accessibility and use

Controls use native buttons, labels and range inputs. Students can use the keyboard. A skip link leads to the main content. Reduced-motion preferences start animations paused; students can explicitly resume them. All experiments can be reset. The network diagram scrolls horizontally on small screens rather than shrinking labels until they become unreadable.

## Scaffolded lesson sequence

Default guided mode reduces visible text and controls. It presents 20 steps across the five experiments before the quiz. Each step asks students to watch or try one change, then explains the observed result. “Next step” unlocks after the activity. “Previous” lets students revisit a step. Full explanations remain in free exploration mode.

Suggested teaching pattern: read the short instruction aloud, ask students to predict what will change, press the action button, then discuss the result before proceeding. Use the pause button to stop moving packets or a response comparison. Keep free exploration for students who are ready to test their own scenarios.
