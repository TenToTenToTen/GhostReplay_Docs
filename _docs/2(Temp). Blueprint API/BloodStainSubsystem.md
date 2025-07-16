---
title: BloodStainSubsystem
category: 2. Blueprint API
order: 1
---

## Start Recording
<img src="../../images/StartRecording.png" width="300" />	

#### Description

>If the group is already recording, join the group <br>
Record Component is Attached to the Target Actor

#### Inputs

| Type | Name | Description |
|------|------|-------------|
| UBloodStainSubsystem* | Target | The subsystem that controls recording |
| AActor* | Target Actor | The actor to record |
| FRecordOptions (Optional) | Options | Optional recording options |
| FName (Optional) | Group Name | Optional group name for organizing recordings |

#### Outputs

| Type | Name | Description |
|------|------|-------------|
| bool | Return Value | whether the recording start is successful |

<br>




## Start Recording With Actors
<img src="../../images/StartRecordingWithActors.png" width="300" />	

#### Description

>If the group is already recording, join the group <br>
Record Component is Attached to the Target Actor

#### Inputs

| Type | Name | Description |
|------|------|-------------|
| UBloodStainSubsystem* | Target | The subsystem that controls recording |
| TArray<AActor*> | Target Actors | The actors to record |
| FRecordOptions (Optional) | Options | Optional recording options |
| FName (Optional) | Group Name | Optional group name for organizing recordings |

#### Outputs

| Type | Name | Description |
|------|------|-------------|
| bool | Return Value | whether the recording start is successful |

<br>





## Stop Recording
<img src="../../images/StopRecording.png" width="300" />

#### Description

>Stop Recording Group


#### Inputs

| Type | Name | Description |
|------|------|-------------|
| UBloodStainSubsystem* | Target | The subsystem that controls recording |
| FName (Optional) | Group Name | Optional group name for organizing recordings |
| bool | Save Recording Data | if false, do not save |

<br>






## Stop Recording RecordComponent
<img src="../../images/StopRecordingRecordComponent.png" width="300" />

#### Description

>Stop recording actor.<br>
Group don't stop recording. if you want to stop recording group, use `UBloodStainSubsystem::StopRecord`


#### Inputs

| Type | Name | Description |
|------|------|-------------|
| UBloodStainSubsystem* | Target | The subsystem that controls recording |
| URecordComponent | Record Component | Target Record Component |
| bool | Save Recording Data | if false, do not save |

<br>




## Start Replay From File
<img src="../../images/StartReplayFromFile.png" width="300" />

#### Inputs

| Type | Name | Description |
|------|------|-------------|
| UBloodStainSubsystem* | Target | The subsystem that controls recording |
| FString | File Name | File Name |
| FString | Level Name | Level Name |
| FBloodStainPlaybackOptions (Optional) | In Playback Options | Optional playback options |


#### Outputs

| Type | Name | Description |
|------|------|-------------|
| FGuid | Out Guid | Replaying Group Key |
| bool | return value | whether the start replay is successful |

<br>


## Start Replay by BloodStain
<img src="../../images/StartReplaybyBloodStain.png" width="300" />

#### Inputs

| Type | Name | Description |
|------|------|-------------|
| UBloodStainSubsystem* | Target | The subsystem that controls recording |
| ABloodStainActor* | Blood Stain Actor | BloodStain Actor |


#### Outputs

| Type | Name | Description |
|------|------|-------------|
| FGuid | Out Guid | Replaying Group Key |
| bool | return value | whether the start replay is successful |

<br>



## Stop Replay
<img src="../../images/StopReplay.png" width="300" />

#### Inputs

| Type | Name | Description |
|------|------|-------------|
| UBloodStainSubsystem* | Target | The subsystem that controls recording |
| FGuid | Playback Key | Target Playback Key |

<br>



## Stop Replay playComponent
<img src="../../images/StopReplayplayComponent.png" width="300" />

#### Description

>This don't stop All Actors Playback. if you want to stop All of them, use `UBloodStainSubsystem::StopReplay`


#### Inputs

| Type | Name | Description |
|------|------|-------------|
| UBloodStainSubsystem* | Target | The subsystem that controls recording |
| AGhostActor* | Ghost Actor | Target Playback GhostActor |

<br>



<!-- <br><br><br><br><br><br><br>

# 테스트

#### Parameters
- **Target** (`UBloodStainSubsystem*`): The subsystem that manages the recording
- **Target Actor** (`AActor*`): The actor to be recorded
- **Options** (`FRecordOptions`, *optional*): Additional record settings
- **Group Name** (`FName`, *optional*): Name of the recording group


| Name | Type | Description |
|------|------|-------------|
| Target | UBloodStainSubsystem* | The subsystem that controls recording |
| Target Actor | AActor* | The actor to record |
| Options | FRecordOptions (Optional) | Optional recording options |
| Group Name | FName (Optional) | Optional group name for organizing recordings |


#### Returns
- **Return Value** (`bool`): `true` if recording started successfully, otherwise `false`.
- **Out Guid** (`FGuid`): The key identifying the replay group that started.


### Start Recording

Starts recording a specific actor in the scene.  
If the specified group is already recording, the actor is added to that group.  
Attaches a `RecordComponent` to the target actor to begin tracking.

Use `StopRecording` to finish and optionally save the recorded data. -->