## 앱이 foreground에 있을 때와 background에 있을 때 어떤 제약사이 있고, 상태 변화에 따라 다른 동작을 처리하기 위한 델리게이트 메서드들을 설명하시오.

#### foreground(앱이 실행상태)와 background(앱이 내려가있는 상태)에 있을때 제약사항

foreground에 있을때 작업중이던게  background으로 이동시에 이어서 할 경우 background fetch로 개발을 해줘야 합니다. 작업은 연산이나  그리고 최소한에 대한 작업만 가능 합니다. iOS는 background에 대한 제약이 심해서 메모리가 일정부분 넘어가면 작업에 대한 쓰레드를 종료 시킵니다. 

백그라운드 모드를 사용하기 위해서는 Capabilities에서 백그라운드 모드를 활성화 할 목록을 선택해 주면 된다.

<img src="/images/backgroundmodes.png" width="150"/>



[자료](https://medium.com/cashwalk/ios-background-mode-9bf921f1c55b)

[자료](https://kka7.tistory.com/133)

#### 상태 변화에 따른 델리게이트 메서드

시작 프로세스가 시작되었지만 상태 복원이 아직 발생하지 않았 음을 대리인에게 알립니다.

```swift
func application(_ application: UIApplication, willFinishLaunchingWithOptions launchOptions: [UIApplication.LaunchOptionsKey : Any]? = nil) -> Bool {
  return true
}
```

대리인에게 시작 프로세스가 거의 완료되었으며 앱을 거의 실행할 준비가되었음을 알립니다.

```swift
func applicationDidFinishLaunching(_ application: UIApplication) {
}	
```

앱의 상태가 활성화로 되었을때 호출 됩니다.

```swift
func applicationDidBecomeActive(_ application: UIApplication) {
}
```

대리인에게 앱이 비활성화 될 예정임을 알려줍니다.

```swift
func applicationWillResignActive(_ application: UIApplication) {
}
```

앱이 현재 백그라운드에 있음을 대리인에게 알려줍니다.

```swift
func applicationDidEnterBackground(_ application: UIApplication) {
}
```

앱이 포 그라운드로 진입하려고한다고 델리게이트에게 알려줍니다.

```swift
func applicationWillEnterForeground(_ application: UIApplication) {
}
```

앱이 종료 되려고 할 때 대리인에게 알립니다

```swift
func applicationWillTerminate(_ application: UIApplication) {
}
```

[자료](https://blog.yagom.net/480)

