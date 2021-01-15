# Nodes are not visible in the flow-library

If you have created a new node and it wont show up in your flows-library in Node-Blue the next tip could help you. 



- Check the package.json file.

  Make sure you'r node name appears in the package.json file in the "nodes" folder.
  Local path: ~/homegear/node-blue/nodes/

  In this folder should be some folders named after the categorys e.g. "timers".

  In this "timers" folder should be a package.json file.
  If you open the file, this is what it should look like:

  ```.json
  {
    "name": "timers",
    "keywords": [
      "node-blue",
      "homegear",
      "timer",
      "date"
    ],
    "node-blue": {
      "local": false,
      "maxThreadCounts": {
        "clock": 1,
        "delay": 10,
        "impulse": 1,
        "interval": 1,
        "off-delay": 1,
        "on-delay": 1,
        "ramp-to": 1,
        "rate-limiter": 1,
        "slow-pwm": 1,
        "sun-position": 1,
        "timer": 1,
        "weekly-program": 1,
        "timer2": 1
      },
      "nodes": {
        "clock": "clock.so",
        "delay": "delay.so",
        "impulse": "impulse.so",
        "interval": "interval.so",
        "off-delay": "off-delay.so",
        "on-delay": "on-delay.so",
        "ramp-to": "ramp-to.so",
        "rate-limiter": "rate-limiter.so",
        "slow-pwm": "slow-pwm.so",
        "sun-position": "sun-position.so",
        "timer": "timer.so",
        "weekly-program": "weekly-program.so",
        "timer2": "timer2.so"
      }
    },
    "version": "1.0.0"
  }
  ```

  Make sure every node you have created shows up in this file.
  Every category folder contains an package.json file, it depends on your'r choosen category where you'r node should be written in. 