# caregiver_recomm

## Usage

```python
from caregiver_recomm import Recommender

recomm = Recommender()
recomm.dispatch(speaker_id, evt)
```

### Recommender(evt_dim=4)

- **evt_dim**: Event dimensions, default `4`
- **mock**: Simulate the user interaction, default `False`
- **server_config**: Remote server configuration, default `None`
  - **client_id**: client id
  - **url**: server url

### dispatch(speaker_id, evt)

- **speacker_id**:
- **evt**: numpy array or python list

### EMA Tables Used
- reward_data: Information of all prompts sent to the phone are stored in this table
	This table holds the following: empathid,TimeSent,suid,TimeReceived,Response,Question,QuestionType,QuestionName,Uploaded
- ema_storing_data: Information pertaining only to recommendation messages sent are stored in this table
	This table holds the following: time,event_vct,stats_vct,action,reward,action_vct,uploaded
- ema_settings: Used to dynamically change prompts and answer choices 
- ema_data: Used to retrieve prompt answer