# P1: USB-C 3.3 V power board

Plug in any USB-C charger or laptop. The board gives 5 V and 3.3 V on a
4-pin header, with a power LED. My first board: the whole flow from
schematic to a soldered, tested board.

## Requirements

| Requirement | Value |
|---|---|
| Input | USB-C, 5 V, power only (the board is a "sink": it takes power, no data) |
| Outputs | 5 V (passed through) and 3.3 V from an LDO, on a 1×4 header: 5V, 3V3, GND, GND |
| 3.3 V current limit | *To do: calculated in Session 3* |
| Indicators and tests | One power LED. Test points on VBUS, 3V3 and GND |
| Board | 2 layers, bottom layer = solid ground. Parts 0805 or larger, for hand soldering |

## 3.3 V regulator: AP2112K-3.3TRG1 (Diodes Inc., SOT-25)

| From the datasheet | Value |
|---|---|
| Pins | 1 VIN, 2 GND, 3 EN, 4 NC, 5 VOUT |
| Input / output capacitors | 1 µF each, X5R or X7R |
| θJA (SOT-25) | 184 °C/W |
| Dropout at 600 mA | 250 mV typical, 400 mV max |

## Status

- [x] Requirements written
- [ ] Library parts made (symbol, footprint, part numbers)
- [ ] Schematic (0 errors)
- [ ] Placement and routing
- [ ] DRC and DFM checked
- [ ] Ordered
- [ ] Soldered and tested
