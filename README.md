VIN Decoder API
============

VIN Decoder is a simple tool for decoding vehicle identification numbers. It returns the make, model, and more of the vehicle.

![Build Status](https://img.shields.io/badge/build-passing-green)
![Code Climate](https://img.shields.io/badge/maintainability-B-purple)
![Prod Ready](https://img.shields.io/badge/production-ready-blue)

This is a Javascript Wrapper for the [VIN Decoder API](https://apiverve.com/marketplace/api/vindecoder)

---

## Installation
	npm install @apiverve/vindecoder --save

---

## Configuration

Before using the vindecoder API client, you have to setup your account and obtain your API Key.  
You can get it by signing up at [https://apiverve.com](https://apiverve.com)

---

## Usage

The VIN Decoder API documentation is found here: [https://docs.apiverve.com/api/vindecoder](https://docs.apiverve.com/api/vindecoder).  
You can find parameters, example responses, and status codes documented here.

### Setup

```
var vindecoderAPI = require('@apiverve/vindecoder');
var api = new vindecoderAPI({
    api_key: [YOUR_API_KEY],
    secure: true //(Optional, defaults to true)
});
```

---


### Perform Request
Using the API client, you can perform requests to the API.

###### Define Query

```
var query = {
  vin: "1HGCM82633A004352"
};
```

###### Simple Request (using Callback)

```
api.execute(query, function (error, data) {
    if (error) {
        return console.error(error);
    } else {
        console.log(data);
    }
});
```

###### Example Response

```
{
  "status": "ok",
  "error": null,
  "data": {
    "make": "HONDA",
    "manufacturer": "AMERICAN HONDA MOTOR CO., INC.",
    "model": "Accord",
    "options": {
      "abs": "",
      "activesafetysysnote": "",
      "adaptivecruisecontrol": "",
      "adaptivedrivingbeam": "",
      "adaptiveheadlights": "",
      "additionalerrortext": "",
      "airbagloccurtain": "1st and 2nd Rows",
      "airbaglocfront": "1st Row (Driver and Passenger)",
      "airbaglocknee": "",
      "airbaglocseatcushion": "",
      "airbaglocside": "1st Row (Driver and Passenger)",
      "automaticpedestrianalertingsound": "",
      "autoreversesystem": "",
      "axleconfiguration": "",
      "axles": "",
      "baseprice": "",
      "batterya": "",
      "batterya_to": "",
      "batterycells": "",
      "batteryinfo": "",
      "batterykwh": "",
      "batterykwh_to": "",
      "batterymodules": "",
      "batterypacks": "",
      "batterytype": "",
      "batteryv": "",
      "batteryv_to": "",
      "bedlengthin": "",
      "bedtype": "Not Applicable",
      "blindspotintervention": "",
      "blindspotmon": "",
      "bodycabtype": "Not Applicable",
      "bodyclass": "Coupe",
      "brakesystemdesc": "",
      "brakesystemtype": "",
      "busfloorconfigtype": "Not Applicable",
      "buslength": "",
      "bustype": "Not Applicable",
      "can_aacn": "",
      "cashforclunkers": "",
      "chargerlevel": "",
      "chargerpowerkw": "",
      "cib": "",
      "coolingtype": "",
      "curbweightlb": "",
      "custommotorcycletype": "Not Applicable",
      "daytimerunninglight": "",
      "destinationmarket": "",
      "displacementcc": "2998.832712",
      "displacementci": "183",
      "displacementl": "2.998832712",
      "doors": "2",
      "driverassist": "",
      "drivetype": "",
      "dynamicbrakesupport": "",
      "edr": "",
      "electrificationlevel": "",
      "engineconfiguration": "V-Shaped",
      "enginecycles": "",
      "enginecylinders": "6",
      "enginehp": "240",
      "enginehp_to": "",
      "enginekw": "",
      "enginemanufacturer": "",
      "enginemodel": "J30A4",
      "entertainmentsystem": "",
      "errorcode": "0",
      "errortext": "0 - VIN decoded clean. Check Digit (9th position) is correct",
      "esc": "",
      "evdriveunit": "",
      "forwardcollisionwarning": "",
      "fuelinjectiontype": "",
      "fueltypeprimary": "Gasoline",
      "fueltypesecondary": "",
      "gcwr": "",
      "gcwr_to": "",
      "gvwr": "Class 1C: 4,001 - 5,000 lb (1,814 - 2,268 kg)",
      "gvwr_to": "Class 1: 6,000 lb or less (2,722 kg or less)",
      "keylessignition": "",
      "lanecenteringassistance": "",
      "lanedeparturewarning": "",
      "lanekeepsystem": "",
      "lowerbeamheadlamplightsource": "",
      "makeid": "474",
      "manufacturerid": "988",
      "modelid": "1861",
      "motorcyclechassistype": "Not Applicable",
      "motorcyclesuspensiontype": "Not Applicable",
      "ncsabodytype": "",
      "ncsamake": "",
      "ncsamapexcapprovedby": "",
      "ncsamapexcapprovedon": "",
      "ncsamappingexception": "",
      "ncsamodel": "",
      "ncsanote": "",
      "nonlanduse": "",
      "note": "",
      "otherbusinfo": "",
      "otherengineinfo": "",
      "othermotorcycleinfo": "",
      "otherrestraintsysteminfo": "Seat Belt (Rr center position)",
      "othertrailerinfo": "",
      "parkassist": "",
      "pedestrianautomaticemergencybraking": "",
      "plantcity": "MARYSVILLE",
      "plantcompanyname": "",
      "plantcountry": "UNITED STATES (USA)",
      "plantstate": "OHIO",
      "possiblevalues": "",
      "pretensioner": "",
      "rearautomaticemergencybraking": "",
      "rearcrosstrafficalert": "",
      "rearvisibilitysystem": "",
      "saeautomationlevel": "",
      "saeautomationlevel_to": "",
      "seatbeltsall": "Manual",
      "seatrows": "",
      "seats": "",
      "semiautomaticheadlampbeamswitching": "",
      "series": "",
      "series2": "",
      "steeringlocation": "",
      "suggestedvin": "",
      "topspeedmph": "",
      "tpms": "",
      "trackwidth": "",
      "tractioncontrol": "",
      "trailerbodytype": "Not Applicable",
      "trailerlength": "",
      "trailertype": "Not Applicable",
      "transmissionspeeds": "5",
      "transmissionstyle": "Automatic",
      "trim": "EX-V6",
      "trim2": "",
      "turbo": "",
      "valvetraindesign": "Single Overhead Cam (SOHC)",
      "vehicledescriptor": "1HGCM826*3A",
      "vehicletype": "PASSENGER CAR",
      "wheelbaselong": "",
      "wheelbaseshort": "",
      "wheelbasetype": "",
      "wheels": "",
      "wheelsizefront": "",
      "wheelsizerear": "",
      "windows": ""
    },
    "trim": "EX-V6",
    "vin": "1HGCM82633A004352",
    "year": "2003"
  },
  "code": 200
}
```

---

## Customer Support

Need any assistance? [Get in touch with Customer Support](https://apiverve.com/contact).

---

## Updates
Stay up to date by following [@apiverveHQ](https://twitter.com/apiverveHQ) on Twitter.

---

## Legal

All usage of the APIVerve website, API, and services is subject to the [APIVerve Terms of Service](https://apiverve.com/terms) and all legal documents and agreements.

---

## License
Licensed under the The MIT License (MIT)

Copyright (&copy;) 2024 APIVerve, and Evlar LLC

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.