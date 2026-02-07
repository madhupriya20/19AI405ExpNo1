<h1>ExpNo 1 :Developing AI Agent with PEAS Description</h1>
<h3>Name: Madhupriya R</h3>
<h3>Register No: 212224040177</h3>


<h3>AIM:</h3>
<br>
<p>To find the PEAS description for the given AI problem and develop an AI agent.</p>
<br>
<h3>Theory</h3>
<h3>Medicine prescribing agent:</h3>
<p>Such this agent prescribes medicine for fever (greater than 98.5 degrees) which we consider here as unhealthy, by the user temperature input, and another environment is rooms in the hospital (two rooms). This agent has to consider two factors one is room location and an unhealthy patient in a random room, the agent has to move from one room to another to check and treat the unhealthy person. The performance of the agent is calculated by incrementing performance and each time after treating in one room again it has to check another room so that the movement causes the agent to reduce its performance. Hence, agents prescribe medicine to unhealthy.</p>
<hr>
<h3>PEAS DESCRIPTION:</h3>
<table>
  <tr>
    <td><strong>Agent Type</strong></td>
    <td><strong>Performance</strong></td>
     <td><strong>Environment</strong></td>
    <td><strong>Actuators</strong></td>
    <td><strong>Sensors</strong></td>
  </tr>
    <tr>
    <td><strong>Medicine prescribing agent</strong></td>
    <td><strong>Treating unhealthy, agent movement</strong></td>
     <td><strong>Rooms, Patient</strong></td>
    <td><strong>Medicine, Treatment</strong></td>
    <td><strong>Location, Temperature of patient</strong></td>
  </tr>
</table>
<hr>
<H3>DESIGN STEPS</H3>
<h3>STEP 1:Identifying the input:</h3>
<p>Temperature from patients, Location.</p>
<h3>STEP 2:Identifying the output:</h3>
<p>Prescribe medicine if the patient in a random has a fever.</p>
<h3>STEP 3:Developing the PEAS description:</h3>
<p>PEAS description is developed by the performance, environment, actuators, and sensors in an agent.</p>
<h3>STEP 4:Implementing the AI agent:</h3>
<p>Treat unhealthy patients in each room. And check for the unhealthy patients in random room</p>
<h3>STEP 5:</h3>
<p>Measure the performance parameters: For each treatment performance incremented, for each movement performance decremented</p>

### Program 
```python
class HealthMonitoringAgent:
    def __init__(self, patient_data):
        self.patient_data = patient_data
        self.alert_count = 0

    def monitor_health(self):
        while True:
            current_health_state = self.sensors.get_health_state()
            action = self.choose_action(current_health_state)
            self.actuators.perform_action(action)

            if action == "No specific action needed":
                break

    def choose_action(self, current_health_state):
        if self.alert_count < 3:
            self.alert_count += 1
            return "Alert healthcare provider: High heart rate detected"
        else:
            return "No specific action needed"


class HealthSensors:
    def get_health_state(self):
        return {
            'heart_rate': 130,
            'blood_pressure': 150,
            'temperature': 38.2
        }


class HealthActuators:
    def perform_action(self, action):
        print(action)


if __name__ == "__main__":
    patient_data = {'patient_id': 123, 'name': 'John Doe', 'age': 35}

    agent = HealthMonitoringAgent(patient_data)
    agent.sensors = HealthSensors()
    agent.actuators = HealthActuators()

    agent.monitor_health()
```
### Output



<img width="544" height="90" alt="Screenshot 2026-02-02 081038" src="https://github.com/user-attachments/assets/3848a85b-28e7-4d35-845f-43976fddacec" />

### Result 
Thus the code is executed successfully.
