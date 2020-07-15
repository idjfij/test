#RxInteractionSystem

> Namespace: Ximmerse.RhinoX     
> public sealed class ARCamera : MonoBehaviour   
      
![Logo](https://raw.githubusercontent.com/Ximmerse/Rhino-X/gh-pages/en/images/RXInteractionSystem_config_1.png)

>组件简介：RxEventSystem和RxInputModule属于底层范畴，用于响应机器抛出的事件。与之对应的是RxInteractionSystem组件，用于响应控制器手柄与物体间发生的交互事件（如：触碰、抓取、抛出）。   
>使用方式：将RxInteractionSystem组件添加到RxEventSystem对象上。     
>实现效果：可以处理控制器手柄与物体间发生的交互事件。

!> 场景必须有此组件， Grabable等HighLevel 组件才可以与用户产生交互。请开发者确保场景中有且只有一个此组件。

##公共方法

#### CurrentTouchingObjects()
- `public static IReadOnlyList<I_Touchable> CurrentTouchingObjects{get;}`     
获取当前触碰的物体

#### TouchingObjectCount()
- `public static int TouchingObjectCount{get;}`     
获取被触碰物体的数量

#### CurrentTouchingObjects()
- `public static IReadOnlyList<I_Grabable> CurrentGrabingObjects{get;}`     
获取当前抓取的物体

#### GrabingObjectCount()
- `public static int GrabingObjectCount{get;}`     
获取被抓取物体的数量

#### RegisterTouchable()
- `public static void RegisterTouchable (I_Touchable touchable);`     
注册可触摸的物体


#### UnregisterTouchable()
- `public static void UnregisterTouchable(I_Touchable touchable)`     
注销可触摸的物体

#### RegisterGrabable()
- `public static void RegisterGrabable(I_Grabable grabable)`     
注册可抓取的物体

#### UnregisterGrabable()
- `public static void UnregisterGrabable(I_Grabable grabable)`     
注销可抓取的物体

#### RegisterThrowable()
- `public static void RegisterThrowable(I_ThrowableObject throwable)`     
注册可投掷的物体

#### UnregisterThrowable()
- `public static void UnregisterThrowable(I_ThrowableObject throwable)`     
注销可投掷的物体

##静态成员

#### Instance
- `public static RXInteractionSystem Instance { get; }`     
RXInteractionSystem 的静态单例引用。

####OnTouchBeginEvent, OnTouchStayEvent, OnTouchEndEvent
- `public static event System.Action<PlayerHand, I_Touchable> OnTouchBeginEvent, OnTouchStayEvent, OnTouchEndEvent;`     
用于开始触碰、一直触碰、结束触碰的事件触发器

####OnGrabBeginEvent, OnGrabUpdateEvent, OnGranEndEvent
- `public static event System.Action<PlayerHand, I_Touchable> OnGrabBeginEvent, OnGrabUpdateEvent, OnGranEndEvent;`     
用于开始抓取、一直抓取、放开物体的事件触发器
####OnTouchBeginEvent, OnTouchStayEvent, OnTouchEndEvent
- `public static event System.Action<PlayerHand, I_Touchable>OnThrowEvent;`     
用于抛出物体的事件触发器
