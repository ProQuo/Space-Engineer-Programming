# Space-Engineer-Programming
small snippets of code for use in the online sandbox game, Space Engineers

=======================================================================================================================================
All terminal blocks have the following properties: Interface name: this name is the name of the block in code, it can differ from the name as displayed in the building screen. E.g. Antenna interface name is IMyRadioAntenna - you need to use this interface if you want to get all antennas.

Parent: this is parent of the block (all blocks have IMyTerminalBlock as parent), this can be used for getting type of blocks instead of concrete block type. E.g. if you want to get all lights in grid you will use IMyLightingBlock, if you want only Interior Light you can use IMyInteriorLight.

Field: this is read only field available for block e.g. for IMyBeacon you can get Radius property. Based on this property you can increase/decrease radius of beacon.

Actions: these are all available actions for block with their names in game, so if you want to increase broadcast radius for antenna, you need to execute DecreaseRadius action for block.

=======================================================================================================================================

Antenna

Interface name: IMyRadioAntenna
Parent: IMyFunctionalBlock
Fields: float Radius

Actions OnOff -> Toggle block On/Off
OnOff_On -> Toggle block On
OnOff_Off -> Toggle block Off
IncreaseRadius -> Increase Broadcast radius
DecreaseRadius -> Decrease Broadcast radius

=======================================================================================================================================

Arc Furnace

Interface name: IMyRefinery
Parent: IMyProductionBlock
Parent: IMyFunctionalBlock
Fields: bool UseConveyorSystem

Actions OnOff -> Toggle block On/Off
OnOff_On -> Toggle block On
OnOff_Off -> Toggle block Off
UseConveyor -> Use Conveyor System On/Off

=======================================================================================================================================

Artificial Mass

Interface name: IMyVirtualMass
Parent: IMyFunctionalBlock
Fields: None

Actions OnOff -> Toggle block On/Off
OnOff_On -> Toggle block On
OnOff_Off -> Toggle block Off

=======================================================================================================================================

Assembler

Interface name: IMyAssembler
Parent: IMyProductionBlock
Parent: IMyFunctionalBlock
Fields: bool UseConveyorSystem

Actions OnOff -> Toggle block On/Off
OnOff_On -> Toggle block On
OnOff_Off -> Toggle block Off
UseConveyor -> Use Conveyor System On/Off

=======================================================================================================================================

Battery

Interface name: IMyBatteryBlock
Parent: IMyFunctionalBlock
Fields: bool HasCapacityRemaining

Actions OnOff -> Toggle block On/Off
OnOff_On -> Toggle block On
OnOff_Off -> Toggle block Off
Recharge -> Recharge On/Off

=======================================================================================================================================

Beacon

Interface name: IMyBeacon
Parent: IMyFunctionalBlock
Fields: float Radius

Actions OnOff -> Toggle block On/Off
OnOff_On -> Toggle block On
OnOff_Off -> Toggle block Off
IncreaseRadius -> Increase Broadcast radius
DecreaseRadius -> Decrease Broadcast radius

=======================================================================================================================================

Button Panel
----------------------

Interface name: IMyButtonPanel
Fields: bool AnyoneCanUse

Actions AnyoneCanUse -> Anyone Can Use On/Off

=======================================================================================================================================

Camera
----------------------

Interface name: IMyCameraBlock
Parent: IMyFunctionalBlock
Fields: None

Actions OnOff -> Toggle block On/Off
OnOff_On -> Toggle block On
OnOff_Off -> Toggle block Off
View -> View

=======================================================================================================================================

Cockpit
----------------------

Interface name: IMyCockpit
Parent: IMyShipController
Fields: 
bool ControlWheels
bool ControlThrusters
bool HandBrake 
bool DampenersOverride

Actions ControlThrusters -> Control thrusters On/Off
ControlWheels -> Control wheels On/Off
HandBrake -> Handbrake On/Off
DampenersOverride -> Inertia dampeners On/Off

=======================================================================================================================================

Collector
----------------------

Interface name: IMyCollector
Parent: IMyFunctionalBlock
Fields: bool UseConveyorSystem

Actions OnOff -> Toggle block On/Off
OnOff_On -> Toggle block On
OnOff_Off -> Toggle block Off
UseConveyor -> Use Conveyor System On/Off

=======================================================================================================================================

Connector
----------------------

Interface name: IMyShipConnector
Parent: IMyFunctionalBlock
Fields: 
bool ThrowOut 
bool CollectAll 
bool IsLocked

Actions OnOff -> Toggle block On/Off
OnOff_On -> Toggle block On
OnOff_Off -> Toggle block Off
ThrowOut -> Throw Out On/Off
CollectAll -> Collect All On/Off
SwitchLock -> Switch lock

=======================================================================================================================================

Control Panel
----------------------

Interface name: IMyControlPanel
Fields: None
Actions: None

=======================================================================================================================================

Control Station
----------------------

Interface name: IMyCockpit
Parent: IMyShipController
Fields: 
bool ControlWheels
bool ControlThrusters
bool HandBrake 
bool DampenersOverride

Actions ControlThrusters -> Control thrusters On/Off
ControlWheels -> Control wheels On/Off
HandBrake -> Handbrake On/Off
DampenersOverride -> Inertia dampeners On/Off

=======================================================================================================================================

Door
----------------------

Interface name: IMyDoor
Parent: IMyFunctionalBlock
Fields: bool Open

Actions OnOff -> Toggle block On/Off
OnOff_On -> Toggle block On
OnOff_Off -> Toggle block Off
Open -> Open/Closed
Open_On -> Open
Open_Off -> Closed

=======================================================================================================================================

Drill
----------------------

Interface name: IMyShipDrill
Parent: IMyFunctionalBlock
Fields: bool UseConveyorSystem

Actions OnOff -> Toggle block On/Off
OnOff_On -> Toggle block On
OnOff_Off -> Toggle block Off
UseConveyor -> Use Conveyor System On/Off

=======================================================================================================================================

Flight Seat
----------------------

Interface name: IMyCockpit
Parent: IMyShipController
Fields: 
bool ControlWheels
bool ControlThrusters
bool HandBrake 
bool DampenersOverride

Actions ControlThrusters -> Control thrusters On/Off
ControlWheels -> Control wheels On/Off
HandBrake -> Handbrake On/Off
DampenersOverride -> Inertia dampeners On/Off

=======================================================================================================================================

Gatling Turret
----------------------

Interface name: IMyLargeGatlingTurret
Parent: IMyLargeConveyorTurretBase
Parent: IMyLargeTurretBase
Parent: IMyFunctionalBlock
Fields: 
bool UseConveyorSystem 
bool CanControl
float Range

Actions OnOff -> Toggle block On/Off
OnOff_On -> Toggle block On
OnOff_Off -> Toggle block Off
Control -> Control
IncreaseRange -> Increase Radius
DecreaseRange -> Decrease Radius
UseConveyor -> Use Conveyor System On/Off

=======================================================================================================================================

Gravity Generator
----------------------

Interface name: IMyGravityGenerator
Parent: IMyGravityGeneratorBase
Parent: IMyFunctionalBlock
Fields: 
float FieldWidth 
float FieldHeight 
float FieldDepth 
float Gravity

Actions OnOff -> Toggle block On/Off
OnOff_On -> Toggle block On
OnOff_Off -> Toggle block Off
IncreaseWidth -> Increase Field width
DecreaseWidth -> Decrease Field width
IncreaseHeight -> Increase Field height
DecreaseHeight -> Decrease Field height
IncreaseDepth -> Increase Field depth
DecreaseDepth -> Decrease Field depth
IncreaseGravity -> Increase Acceleration
DecreaseGravity -> Decrease Acceleration

=======================================================================================================================================

Grinder
----------------------

Interface name: IMyShipGrinder
Parent: IMyShipToolBase
Parent: IMyFunctionalBlock
Fields: None

Actions OnOff -> Toggle block On/Off
OnOff_On -> Toggle block On
OnOff_Off -> Toggle block Off
UseConveyor -> Use Conveyor System On/Off

=======================================================================================================================================

Gyroscope
----------------------

Interface name: IMyGyro
Parent: IMyFunctionalBlock
Fields: 
float GyroPower 
bool GyroOverride 
float Yaw 
float Pitch 
float Roll

Actions
OnOff -> Toggle block On/Off
OnOff_On -> Toggle block On
OnOff_Off -> Toggle block Off
IncreasePower -> Increase Power
DecreasePower -> Decrease Power
Override -> Override controls On/Off
IncreaseYaw -> Increase Yaw override
DecreaseYaw -> Decrease Yaw override
IncreasePitch -> Increase Pitch override
DecreasePitch -> Decrease Pitch override
IncreaseRoll -> Increase Roll override
DecreaseRoll -> Decrease Roll override

=======================================================================================================================================

Interior Light
----------------------

Interface name: IMyInteriorLight
Parent: IMyLightingBlock
Parent: IMyFunctionalBlock
Fields:
float Radius
float Intensity
float BlinkIntervalSeconds
float BlinkLenght
float BlinkOffset

Actions
OnOff -> Toggle block On/Off
OnOff_On -> Toggle block On
OnOff_Off -> Toggle block Off
IncreaseRadius -> Increase Radius
DecreaseRadius -> Decrease Radius
IncreaseBlink Interval -> Increase Blink Interval
DecreaseBlink Interval -> Decrease Blink Interval
IncreaseBlink Lenght -> Increase Blink Length
DecreaseBlink Lenght -> Decrease Blink Length
IncreaseBlink Offset -> Increase Blink Offset
DecreaseBlink Offset -> Decrease Blink Offset

=======================================================================================================================================

Interior Turret
----------------------

Interface name: IMyLargeInteriorTurret
Parent: IMyLargeTurretBase
Parent: IMyFunctionalBlock
Fields:
bool CanControl
float Range

Actions
OnOff -> Toggle block On/Off
OnOff_On -> Toggle block On
OnOff_Off -> Toggle block Off
Control -> Control
IncreaseRange -> Increase Radius
DecreaseRange -> Decrease Radius

=======================================================================================================================================

Landing Gear
----------------------

Interface name: IMyLandingGear
Parent: IMyFunctionalBlock
Fields:
float BreakForce

Actions
OnOff -> Toggle block On/Off
OnOff_On -> Toggle block On
OnOff_Off -> Toggle block Off
Lock -> Lock
Unlock -> Unlock
SwitchLock -> Switch lock
Autolock -> Autolock On/Off
IncreaseBreakForce -> Increase Break Force
DecreaseBreakForce -> Decrease Break Force

=======================================================================================================================================

Small Cargo Container
----------------------

Interface name: IMyCargoContainer
Fields: None
Actions: None

=======================================================================================================================================

Medium Cargo Container
----------------------

Interface name: IMyCargoContainer
Fields: None
Actions:None

=======================================================================================================================================

Large Cargo Container
----------------------

Interface name: IMyCargoContainer
Fields: None
Actions: None

=======================================================================================================================================

Small Reactor
----------------------

Interface name: IMyReactor
Parent: IMyFunctionalBlock
Fields:
bool UseConveyorSystem

Actions
OnOff -> Toggle block On/Off
OnOff_On -> Toggle block On
OnOff_Off -> Toggle block Off
UseConveyor -> Use Conveyor System On/Off

=======================================================================================================================================

Large Reactor
----------------------

Interface name: IMyReactor
Parent: IMyFunctionalBlock
Fields: bool UseConveyorSystem

Actions
OnOff -> Toggle block On/Off
OnOff_On -> Toggle block On
OnOff_Off -> Toggle block Off
UseConveyor -> Use Conveyor System On/Off

=======================================================================================================================================

Small Thruster
----------------------

Interface name: IMyThrust
Parent: IMyFunctionalBlock
Fields: float ThrustOverride

Actions
OnOff -> Toggle block On/Off
OnOff_On -> Toggle block On
OnOff_Off -> Toggle block Off
IncreaseOverride -> Increase Thrust override
DecreaseOverride -> Decrease Thrust override

=======================================================================================================================================

Large Thruster
----------------------

Interface name: IMyThrust
Parent: IMyFunctionalBlock
Fields: float ThrustOverride

Actions
OnOff -> Toggle block On/Off
OnOff_On -> Toggle block On
OnOff_Off -> Toggle block Off
IncreaseOverride -> Increase Thrust override
DecreaseOverride -> Decrease Thrust override

=======================================================================================================================================

Medical Room
----------------------

Interface name: IMyMedicalRoom
Parent: IMyFunctionalBlock
Fields: None

Actions
OnOff -> Toggle block On/Off
OnOff_On -> Toggle block On
OnOff_Off -> Toggle block Off

=======================================================================================================================================

Merge Block
----------------------

Interface name: IMyShipMergeBlock
Parent: IMyFunctionalBlock
Fields: None

Actions
OnOff -> Toggle block On/Off
OnOff_On -> Toggle block On
OnOff_Off -> Toggle block Off

=======================================================================================================================================

Missile Turret
----------------------

Interface name: IMyLargeMissileTurret
Parent: IMyLargeConveyorTurretBase
Parent: IMyLargeTurretBase
Parent: IMyFunctionalBlock
Fields:
bool UseConveyorSystem 
bool CanControl
float Range

Actions
OnOff -> Toggle block On/Off
OnOff_On -> Toggle block On
OnOff_Off -> Toggle block Off
Control -> Control
IncreaseRange -> Increase Radius
DecreaseRange -> Decrease Radius
UseConveyor -> Use Conveyor System On/Off

=======================================================================================================================================

Ore Detector
----------------------

Interface name: IMyOreDetector
Parent: IMyFunctionalBlock
Fields:
float Range 
bool BroadcastUsingAntennas

Actions
OnOff -> Toggle block On/Off
OnOff_On -> Toggle block On
OnOff_Off -> Toggle block Off

=======================================================================================================================================

Passenger Seat
----------------------

Interface name: IMyCockpit
Parent: IMyShipController
Fields:
bool ControlWheels
bool ControlThrusters
bool HandBrake 
bool DampenersOverride

Actions
ControlThrusters -> Control thrusters On/Off
ControlWheels -> Control wheels On/Off
HandBrake -> Handbrake On/Off
DampenersOverride -> Inertia dampeners On/Off

=======================================================================================================================================

Piston
----------------------

Interface name: IMyPistonBase
Parent: IMyFunctionalBlock
Fields:
float Velocity 
float MinLimit 
float MaxLimit

Actions
OnOff -> Toggle block On/Off
OnOff_On -> Toggle block On
OnOff_Off -> Toggle block Off
Reverse -> Reverse
IncreaseVelocity -> Increase Velocity
DecreaseVelocity -> Decrease Velocity
ResetVelocity -> Reset Velocity
IncreaseUpperLimit -> Increase Maximal distance
DecreaseUpperLimit -> Decrease Maximal distance
IncreaseLowerLimit -> Increase Minimal distance
DecreaseLowerLimit -> Decrease Minimal distance

=======================================================================================================================================

Programmable Block
----------------------

Interface name: IMyProgrammableBlock
Parent: IMyFunctionalBlock
Fields: bool IsRunning

Actions
OnOff -> Toggle block On/Off
OnOff_On -> Toggle block On
OnOff_Off -> Toggle block Off
Run -> Run

=======================================================================================================================================

Refinery
----------------------

Interface name: IMyRefinery
Parent: IMyFunctionalBlock
Parent: IMyProductionBlock
Fields: bool UseConveyorSystem

Actions
OnOff -> Toggle block On/Off
OnOff_On -> Toggle block On
OnOff_Off -> Toggle block Off
UseConveyor -> Use Conveyor System On/Off

=======================================================================================================================================

Spotlight
----------------------

Interface name: IMyReflectorLight
Parent: IMyLightingBlock
Parent: IMyFunctionalBlock
Fields:
float Radius
float Intensity
float BlinkIntervalSeconds
float BlinkLenght
float BlinkOffset

Actions
OnOff -> Toggle block On/Off
OnOff_On -> Toggle block On
OnOff_Off -> Toggle block Off
IncreaseRadius -> Increase Radius
DecreaseRadius -> Decrease Radius
IncreaseBlink Interval -> Increase Blink Interval
DecreaseBlink Interval -> Decrease Blink Interval
IncreaseBlink Lenght -> Increase Blink Length
DecreaseBlink Lenght -> Decrease Blink Length
IncreaseBlink Offset -> Increase Blink Offset
DecreaseBlink Offset -> Decrease Blink Offset

=======================================================================================================================================

Remote Control
----------------------

Interface name: IMyRemoteControl
Parent: IMyShipController
Fields:
bool ControlWheels
bool ControlThrusters
bool HandBrake 
bool DampenersOverride

Actions
ControlThrusters -> Control thrusters On/Off
ControlWheels -> Control wheels On/Off
HandBrake -> Handbrake On/Off
DampenersOverride -> Inertia dampeners On/Off
Control -> Control

=======================================================================================================================================

Rocket Launcher
----------------------

Interface name: IMySmallMissileLauncher
Parent: IMyFunctionalBlock
Fields: bool UseConveyorSystem

Actions
OnOff -> Toggle block On/Off
OnOff_On -> Toggle block On
OnOff_Off -> Toggle block Off
UseConveyor -> Use Conveyor System On/Off

=======================================================================================================================================

Reloadable Rocket Launcher
----------------------

Interface name: IMySmallMissileLauncherReload
Parent: IMyFunctionalBlock
Fields: bool UseConveyorSystem

Actions
OnOff -> Toggle block On/Off
OnOff_On -> Toggle block On
OnOff_Off -> Toggle block Off
UseConveyor -> Use Conveyor System On/Off

=======================================================================================================================================

Rotor
----------------------

Interface name: IMyMotorStator
Parent: IMyMotorBase
Parent: IMyFunctionalBlock
Fields:
bool IsAttached 
float Torque
float BrakingTorque 
float Velocity 
float LowerLimit 
float UpperLimit 
float Displacement

Actions
OnOff -> Toggle block On/Off
OnOff_On -> Toggle block On
OnOff_Off -> Toggle block Off
Reverse -> Reverse
Detach -> Detach
Attach -> Attach
IncreaseTorque -> Increase Torque
DecreaseTorque -> Decrease Torque
IncreaseBrakingTorque -> Increase Braking tor.
DecreaseBrakingTorque -> Decrease Braking tor.
IncreaseVelocity -> Increase Velocity
DecreaseVelocity -> Decrease Velocity
ResetVelocity -> Reset Velocity
IncreaseLowerLimit -> Increase Lower limit
DecreaseLowerLimit -> Decrease Lower limit
IncreaseUpperLimit -> Increase Upper limit
DecreaseUpperLimit -> Decrease Upper limit
IncreaseDisplacement -> Increase Rotor displacement
DecreaseDisplacement -> Decrease Rotor displacement

=======================================================================================================================================

Sensor
----------------------

Interface name: IMySensorBlock
Parent: IMyFunctionalBlock
Fields:
float LeftExtend 
float RightExtend 
float TopExtend 
float BottomExtend 
float FrontExtend 
float BackExtend 
bool DetectPlayers 
bool DetectFloatingObjects 
bool DetectSmallShips 
bool DetectLargeShips 
bool DetectStations 
bool DetectAsteroids

Actions
OnOff -> Toggle block On/Off
OnOff_On -> Toggle block On
OnOff_Off -> Toggle block Off
IncreaseLeft -> Increase Left extent
DecreaseLeft -> Decrease Left extent
IncreaseRight -> Increase Right extent
DecreaseRight -> Decrease Right extent
IncreaseBottom -> Increase Bottom extent
DecreaseBottom -> Decrease Bottom extent
IncreaseTop -> Increase Top extent
DecreaseTop -> Decrease Top extent
IncreaseBack -> Increase Back extent
DecreaseBack -> Decrease Back extent
IncreaseFront -> Increase Front extent
DecreaseFront -> Decrease Front extent
Detect Players -> Detect players On/Off
Detect Floating Objects -> Detect floating objects On/Off
Detect Small Ships -> Detect small ships On/Off
Detect Large Ships -> Detect large ships On/Off
Detect Stations -> Detect stations On/Off
Detect Asteroids -> Detect Asteroids On/Off

=======================================================================================================================================

Solar Panel
----------------------

Interface name: IMySolarPanel
Fields:None
Actions:None

=======================================================================================================================================

Sound Block
----------------------

Interface name: IMySoundBlock
Parent: IMyFunctionalBlock
Fields:
float Volume 
float Range 
bool IsSoundSelected
float LoopPeriod

Actions
OnOff -> Toggle block On/Off
OnOff_On -> Toggle block On
OnOff_Off -> Toggle block Off
IncreaseVolumeSlider -> Increase Volume
DecreaseVolumeSlider -> Decrease Volume
IncreaseRangeSlider -> Increase Range
DecreaseRangeSlider -> Decrease Range
PlaySound -> Play
StopSound -> Stop
IncreaseLoopableSlider -> Increase Loop time
DecreaseLoopableSlider -> Decrease Loop time

=======================================================================================================================================

Spherical Gravity Generator
----------------------

Interface name: IMyGravityGeneratorSphere
Parent: IMyGravityGeneratorBase
Parent: IMyFunctionalBlock
Fields:
float Radius 
float Gravity

Actions
OnOff -> Toggle block On/Off
OnOff_On -> Toggle block On
OnOff_Off -> Toggle block Off
IncreaseRadius -> Increase Radius
DecreaseRadius -> Decrease Radius
IncreaseGravity -> Increase Acceleration
DecreaseGravity -> Decrease Acceleration

=======================================================================================================================================

Timer Block
----------------------

Interface name: IMyTimerBlock
Parent: IMyFunctionalBlock
Fields:
bool IsCountingDown 
float TriggerDelay

Actions
----------------------

OnOff -> Toggle block On/Off
OnOff_On -> Toggle block On
OnOff_Off -> Toggle block Off
IncreaseTriggerDelay -> Increase Delay
DecreaseTriggerDelay -> Decrease Delay
TriggerNow -> Trigger now
Start -> Start
Stop -> Stop

=======================================================================================================================================

Warhead
----------------------

Interface name: IMyWarhead
Fields:
bool IsCountingDown 
float DetonationTime

Actions
IncreaseDetonationTime -> Increase Detonation time
DecreaseDetonationTime -> Decrease Detonation time
StartCountdown -> Start countdown
StopCountdown -> Stop countdown
Safety -> Safety On/Off
Detonate -> Detonate

=======================================================================================================================================

Welder
----------------------

Interface name: IMyShipWelder
Parent: IMyShipToolBase
Parent: IMyFunctionalBlock

Actions
OnOff -> Toggle block On/Off
OnOff_On -> Toggle block On
OnOff_Off -> Toggle block Off
UseConveyor -> Use Conveyor System On/Off

=======================================================================================================================================

Wheel Suspension 1x1
----------------------

Interface name: IMyMotorSuspension
Parent: IMyMotorBase
Parent: IMyFunctionalBlock
Fields:
bool Steering 
bool Propulsion 
float Damping 
float Strength 
float Friction 
float Power

Actions
OnOff -> Toggle block On/Off
OnOff_On -> Toggle block On
OnOff_Off -> Toggle block Off
Steering -> Steering On/Off
Propulsion -> Propulsion On/Off
IncreaseDamping -> Increase Damping
DecreaseDamping -> Decrease Damping
IncreaseStrength -> Increase Strength
DecreaseStrength -> Decrease Strength
IncreaseFriction -> Increase Friction
DecreaseFriction -> Decrease Friction
IncreasePower -> Increase Power
DecreasePower -> Decrease Power

=======================================================================================================================================

Wheel Suspension 3x3
----------------------

Interface name: IMyMotorSuspension
Parent: IMyMotorBase
Parent: IMyFunctionalBlock
Fields:
bool Steering 
bool Propulsion 
float Damping 
float Strength 
float Friction 
float Power

Actions
OnOff -> Toggle block On/Off
OnOff_On -> Toggle block On
OnOff_Off -> Toggle block Off
Steering -> Steering On/Off
Propulsion -> Propulsion On/Off
IncreaseDamping -> Increase Damping
DecreaseDamping -> Decrease Damping
IncreaseStrength -> Increase Strength
DecreaseStrength -> Decrease Strength
IncreaseFriction -> Increase Friction
DecreaseFriction -> Decrease Friction
IncreasePower -> Increase Power
DecreasePower -> Decrease Power

=======================================================================================================================================

Wheel Suspension 5x5
----------------------

Interface name: IMyMotorSuspension
Parent: IMyMotorBase
Parent: IMyFunctionalBlock
Fields:
bool Steering 
bool Propulsion 
float Damping 
float Strength 
float Friction 
float Power

Actions
OnOff -> Toggle block On/Off
OnOff_On -> Toggle block On
OnOff_Off -> Toggle block Off
Steering -> Steering On/Off
Propulsion -> Propulsion On/Off
IncreaseDamping -> Increase Damping
DecreaseDamping -> Decrease Damping
IncreaseStrength -> Increase Strength
DecreaseStrength -> Decrease Strength
IncreaseFriction -> Increase Friction
DecreaseFriction -> Decrease Friction
IncreasePower -> Increase Power
DecreasePower -> Decrease Power

=======================================================================================================================================
