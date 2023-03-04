# Tasmota-Car-Battery-Voltage




## Rules
Rule1 puts esp into deep sleep<br>
Rule1 ON DIMMER#Boot DO RuleTimer1 60 ENDON ON Rules#Timer=1 DO DeepSleepTime 600 ENDON<br>

to see rule    enter rule1<br>
to disable rule     rule1 0<br>
to disable rule with mqtt     cmnd/tasmota_507B4C/Rule1 0  (use persistent)<br>

## ADC
Voltage divider 47k and 4k7<br>
AdcParam1 6,0,8091,0,28600<br>



## Module Parameters

GPIO3 ADC Range


## HA YAML
name: "TasCar voltage"<br>
       state_topic: "tele/tasmota_507B4C/SENSOR"<br>
       value_template: "{{ value_json.ANALOG.Range1 }}"<br>
       unit_of_measurement: 'mV'<br>


