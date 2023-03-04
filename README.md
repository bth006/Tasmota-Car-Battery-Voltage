# Tasmota-Car-Battery-Voltage




## Rules
Rule1 puts esp into deep sleep
Rule1 ON DIMMER#Boot DO RuleTimer1 60 ENDON ON Rules#Timer=1 DO DeepSleepTime 600 ENDON

to see rule    enter rule1
to disable rule     rule1 0
to disable rule with mqtt     cmnd/tasmota_507B4C/Rule1 0  (use persistent)

## ADC
Voltage divider 47k and 4k7
AdcParam1 6,0,8091,0,28600



## Module Parameters

GPIO3 ADC Range


## HA YAML
`name: "TasCar voltage"  
       state_topic: "tele/tasmota_507B4C/SENSOR"
       value_template: "{{ value_json.ANALOG.Range1 }}"
       unit_of_measurement: 'mV'`


