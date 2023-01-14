# RGD - Rates General Docuemnt for the CDM Plugin

More information about the CDM can be found on the [CDM WEBSITE](https://vats.im/cdm)

<br>

# How Do I Submit My Request?

Create an Issue with your .txt file URL.

<br>

# Which Is The Format?

  `AIRPORT:A:ArrRwyList:NotArrRwyList:D:DepRwyList:NotDepRwyList:DependentRwyList:Rate_RateLvo`

    - ArrRwyList -> Comma-separated list of runways (If more than 1, it will use if one, other or all selected). Enter * to disregard.

    - NotArrRwyList -> Comma-separated list of runways. Enter * to disregard.

    - DepRwyList -> Comma-separated list of runways (If more than 1, it will use if one, other or all selected). Enter * to disregard.

    - NotDepRwyList -> Comma-separated list of runways. Enter * to disregard.

    - DependentRwyList -> Comma-separated list of runways (it will use the same sequence order for runways selected here). Enter * to disregard.

    - Rate_RateLvo -> Normal Rate and LVO Rate. If more than one departure runways, you can define more than one rate separated by comma.


  ## Examples:

    - `LEPA:A:24L:*:D:24R,24L:*:24L,24R:30_12` (1 arr runway, 1 dep runway, 24R/L as dependant. 1 rate defined for all departures).

    - `LEPA:A:24L:24R:D:24R,24L:*:*:30_12,20_7` (1 arr runway, 1 non-arrival runway, 2 dep runway, dep runways as independant, different rates defined for both dep runways).

    - `LEPA:A:*:*:D:*:*:*:30_12` (All departures would have the same rate, doesn't matter the selected runways).

  ## Internal Checks:
  
  A line will be "activated" based on:

   - Runway assigned to the plane.

   - Runways selected in Euroscope's Runway selector dialog.
   
<br>

  ## Important points
  - **Order of the configurations/rates is important (first line more important than last).**
  - **AIRPORTS NOT DEFINED, WILL NOT BE CONSIDERED A CDM AIRPORT.**
  - **Examples can be found in the givenfiles.**
  
  
  <br>
  <br>
  
  
**Feel free to check examples already submitted before send the request.**
