# BME: MC Assignment 1 (SENDER)

## Pin Configuration

| Designator | Direction | Mode        | Label        | Comment                |
|------------|-----------|-------------|--------------|------------------------|
| PA5        | output    | push / pull | LD2          | Onboard LED green      |
| PC0        | input     | n/a         | COM_LINE_IN  | Icommunication Input   |
| PC1        | output    | open drain  | COM_LINE_OUT | commnication OD output |
| PC2        | output    | push / pull | USR_OUT_A    | generic                |
| PC3        | output    | push / pull | USR_OUT_B    | generic                |
| PC13       | output    | Interrupt   | B1           | Onboard push button    |

# Pre compile settings


- main.c line 35:  `#define ARTIFICIAL_LOAD`   
*comment this out to fully  get rid of busy waiting*

- main.c line 36: `#define IS_OPENDRAIN`  
*comment this out to use direct communication line*  
Opendrain : Pin PC1 as output  
Direct : Pin PC2 as output


- main.c around line 99: `volatile uint32_t cmp_delay = 10;`  
*Adjust busy waiting compare value*