# class SingleInstance<T>
## 설명
template을 사용한 클래스이므로, 상속할 때 SingleInstance<클래스명> 처럼 타입을 명시해 주어야 합니다.    
Singleton 패턴을 사용하는 모든 클래스의 부모 클래스입니다. 기본 생성자를 제외한 다른 생성자의 선언이 금지되어 있습니다.

### GetInstance Function
#### Usage
```c++
static Input& Input::GetInstance()
```

#### Parameters
This function has no parameters.

#### Return value
return Input&

#### Remarks
Thread-safe한 Singleton 패턴이 사용되었습니다.
