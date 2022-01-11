# Connect to the CPC

The board interface is the MX4, so it requires a MX4 board or adapter to connect to the edge or centronics expansion connector in the Amstrad.

# I/O port configuration

The DIP switches 1 and 2 allow to select 4 different I/O port address ranges for the Ports A and B, the DIP switch 3 is reserved for future use.

|    DIP 1   |    DIP 2    |     Port A    |     Port B     |
|------------|-------------|---------------|----------------|
|    OFF     |    OFF      |      &F880    |      &F881     |
|    ON      |    OFF      |      &F882    |      &F883     |
|    OFF     |    ON       |      &F884    |      &F885     |
|    ON      |    ON       |      &F886    |      &F887     |

# Usage

When you write to a port, the corresponding pins are set permanently to the written value, and a positive pulse is generated in the OUT CLK signal.

When you read from a port, you get the current levels at the port pins, and a positive pulse is generated in the IN CLK signal.

# Specs

Each port has a 20 pin header, with 8 input pins, 8 output pins, IN CLK, OUT CLK, GND and +5V.

The board has a total of 16 input pins and 16 output pins.

You can connect up to 4 boards configured at different address in the MX4 board, to get a total of 64 input pins and 64 output pins.