# PlayerHand

> Namespace: Ximmerse.RhinoX      
> public class PlayerHand : MonoBehaviour

PlayerHand script is the infrasture of the user interaction system, it delegates to user's hand in AR environment. PlayerHand provides the following functionalities in the SDK:
- Grab support.
- Throw support.

### Public Members

![Logo](https://raw.githubusercontent.com/Ximmerse/Rhino-X/gh-pages/en/images/playerHand_config_1.png ':size=450X400')

#### side
- `public Side side { get; set; }`

Left / right hand side,system doesn't distinguish hands for now.

#### EnableGrasp
- `public bool EnableGrasp { get; set; }`

If the hand object is able to perform grab action.

#### GrabableLayerMask
- `public LayerMask GrabableLayerMask { get; set; }`

The grabable collider target's layer mask.

#### handAnimator
- `public PlayerHandAnimator handAnimator { get; }`

Hand animation.


### Public Methods


#### InstantiateGrabable()
- `public void InstantiateGrabable(Grabable Prefab)`

Instantiate grabable prefab.

#### EnableHands()
- `public static void EnableHands(bool enabled)`

Enable or disable all hands. When hand disabled, the views , animation, and interaction will be disabled all together.

#### SetGrabbedObjectsActive()
- `public static void SetGrabbedObjectsActive(bool active)`

Set all hands current grabbed object active or disactive.
