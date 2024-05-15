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
    "ABS": "",
    "ActiveSafetySysNote": "",
    "AdaptiveCruiseControl": "",
    "AdaptiveDrivingBeam": "",
    "AdaptiveHeadlights": "",
    "AdditionalErrorText": "",
    "AirBagLocCurtain": "1st and 2nd Rows",
    "AirBagLocFront": "1st Row (Driver and Passenger)",
    "AirBagLocKnee": "",
    "AirBagLocSeatCushion": "",
    "AirBagLocSide": "1st Row (Driver and Passenger)",
    "AutoReverseSystem": "",
    "AutomaticPedestrianAlertingSound": "",
    "AxleConfiguration": "",
    "Axles": "",
    "BasePrice": "",
    "BatteryA": "",
    "BatteryA_to": "",
    "BatteryCells": "",
    "BatteryInfo": "",
    "BatteryKWh": "",
    "BatteryKWh_to": "",
    "BatteryModules": "",
    "BatteryPacks": "",
    "BatteryType": "",
    "BatteryV": "",
    "BatteryV_to": "",
    "BedLengthIN": "",
    "BedType": "Not Applicable",
    "BlindSpotIntervention": "",
    "BlindSpotMon": "",
    "BodyCabType": "Not Applicable",
    "BodyClass": "Coupe",
    "BrakeSystemDesc": "",
    "BrakeSystemType": "",
    "BusFloorConfigType": "Not Applicable",
    "BusLength": "",
    "BusType": "Not Applicable",
    "CAN_AACN": "",
    "CIB": "",
    "CashForClunkers": "",
    "ChargerLevel": "",
    "ChargerPowerKW": "",
    "CoolingType": "",
    "CurbWeightLB": "",
    "CustomMotorcycleType": "Not Applicable",
    "DaytimeRunningLight": "",
    "DestinationMarket": "",
    "DisplacementCC": "2998.832712",
    "DisplacementCI": "183",
    "DisplacementL": "2.998832712",
    "Doors": "2",
    "DriveType": "",
    "DriverAssist": "",
    "DynamicBrakeSupport": "",
    "EDR": "",
    "ESC": "",
    "EVDriveUnit": "",
    "ElectrificationLevel": "",
    "EngineConfiguration": "V-Shaped",
    "EngineCycles": "",
    "EngineCylinders": "6",
    "EngineHP": "240",
    "EngineHP_to": "",
    "EngineKW": "",
    "EngineManufacturer": "",
    "EngineModel": "J30A4",
    "EntertainmentSystem": "",
    "ErrorCode": "0",
    "ErrorText": "0 - VIN decoded clean. Check Digit (9th position) is correct",
    "ForwardCollisionWarning": "",
    "FuelInjectionType": "",
    "FuelTypePrimary": "Gasoline",
    "FuelTypeSecondary": "",
    "GCWR": "",
    "GCWR_to": "",
    "GVWR": "Class 1C: 4,001 - 5,000 lb (1,814 - 2,268 kg)",
    "GVWR_to": "Class 1: 6,000 lb or less (2,722 kg or less)",
    "KeylessIgnition": "",
    "LaneCenteringAssistance": "",
    "LaneDepartureWarning": "",
    "LaneKeepSystem": "",
    "LowerBeamHeadlampLightSource": "",
    "Make": "HONDA",
    "MakeID": "474",
    "Manufacturer": "AMERICAN HONDA MOTOR CO., INC.",
    "ManufacturerId": "988",
    "Model": "Accord",
    "ModelID": "1861",
    "ModelYear": "2003",
    "MotorcycleChassisType": "Not Applicable",
    "MotorcycleSuspensionType": "Not Applicable",
    "NCSABodyType": "",
    "NCSAMake": "",
    "NCSAMapExcApprovedBy": "",
    "NCSAMapExcApprovedOn": "",
    "NCSAMappingException": "",
    "NCSAModel": "",
    "NCSANote": "",
    "NonLandUse": "",
    "Note": "",
    "OtherBusInfo": "",
    "OtherEngineInfo": "",
    "OtherMotorcycleInfo": "",
    "OtherRestraintSystemInfo": "Seat Belt (Rr center position)",
    "OtherTrailerInfo": "",
    "ParkAssist": "",
    "PedestrianAutomaticEmergencyBraking": "",
    "PlantCity": "MARYSVILLE",
    "PlantCompanyName": "",
    "PlantCountry": "UNITED STATES (USA)",
    "PlantState": "OHIO",
    "PossibleValues": "",
    "Pretensioner": "",
    "RearAutomaticEmergencyBraking": "",
    "RearCrossTrafficAlert": "",
    "RearVisibilitySystem": "",
    "SAEAutomationLevel": "",
    "SAEAutomationLevel_to": "",
    "SeatBeltsAll": "Manual",
    "SeatRows": "",
    "Seats": "",
    "SemiautomaticHeadlampBeamSwitching": "",
    "Series": "",
    "Series2": "",
    "SteeringLocation": "",
    "SuggestedVIN": "",
    "TPMS": "",
    "TopSpeedMPH": "",
    "TrackWidth": "",
    "TractionControl": "",
    "TrailerBodyType": "Not Applicable",
    "TrailerLength": "",
    "TrailerType": "Not Applicable",
    "TransmissionSpeeds": "5",
    "TransmissionStyle": "Automatic",
    "Trim": "EX-V6",
    "Trim2": "",
    "Turbo": "",
    "VIN": "1HGCM82633A004352",
    "ValveTrainDesign": "Single Overhead Cam (SOHC)",
    "VehicleDescriptor": "1HGCM826*3A",
    "VehicleType": "PASSENGER CAR",
    "WheelBaseLong": "",
    "WheelBaseShort": "",
    "WheelBaseType": "",
    "WheelSizeFront": "",
    "WheelSizeRear": "",
    "Wheels": "",
    "Windows": ""
  }
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