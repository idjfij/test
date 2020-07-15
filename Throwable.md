# Throwable

> Namespace: Ximmerse.RhinoX      
> public class Throwable : MonoBehaviour

Throwable script : behaviour for throwable object.Throwable provides the following functionalities in the SDK:
- Throwable provides two methods to throw game object.

### Public Members

![Logo](https://raw.githubusercontent.com/Ximmerse/Rhino-X/gh-pages/en/images/throwable_config_1.png ':size=450X400')

#### ThrowableBehaviourType
- `public enum ThrowableBehaviourType
{
    ThrowAway = 0,
    Eject,
};// Default : ThrowAway`
Throw away: throw the object away by a common throw gesture.
Eject: press the trigger and then eject the object ahead.

#### TotalQueueTime
- `public float TotalQueueTime { get; set; }`
The total queue time to evaluate physical throw speed.

#### VelocityToForceRate
- `public float VelocityToForceRate { get; set; }`
Velocity to force rate.

#### Collider
- `public Collider Collider { get; }`
The Collider this script controls.

#### UseGravity
- `public bool UseGravity = true;`

#### EjectForce
- `public float EjectForce = 2;`

#### DisallowGrabableAfterThrown
- `public bool DisallowGrabableAfterThrow { get; set; } `
Disable grabable after it's thrown.

#### Rigidbody
- `public Rigidbody Rigidbody { get; set; }`
The rigidbody this script controls.

#### SpeedMax
- `public float SpeedMax = 2.5f;`
Speed range : max

#### Multiplier
- `public float Multiplier = 1.5f;`


### Public Methods

#### Eject
- `public async Task Eject(Vector3 Force)`
Ejects the throwable using force.
