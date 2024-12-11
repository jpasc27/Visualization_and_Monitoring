# S30XL Visualization and Monitoring

To run (via Kieran's instructions):

This is the script we will actually run to launch our dummy frames. This file basically declares our virtual server to produce our dummy frames and opens PyDM window to manage them. Run:

```bash
python3 scripts/TsTop.py
```

A GUI window should open. To start launching your dummy frames, select the frame rate you would like from Run Rate and then switch the Run State to Running. In the terminal you launched ```TsTop.py```, you should now see output. These are outputs from the TsDaqDataReceiver process function!

As a good proof of concept, Kieran wanted to try and replicate charge linearization in Rogue and create a GUI to show these values. To run the following code, you need to download and import ```BitVector```. He constructed a PyDM GUI to go along with TsDaqDataReceiver.py called ```emulator_readout.ui```. To run the GUI, in one terminal window run the ```TsTop.py``` script that generates our dummy frames to activate our data receiver. Make sure to turn on the frame generator by switching the mode to running. In another terminal, open the GUI using the command:
```bash
pydm emulator_readout.ui
``` 

This will load the GUI after a few seconds, and if the frame generator is active, you should see it come to life. 
