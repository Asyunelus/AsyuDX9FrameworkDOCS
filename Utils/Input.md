# class Input
## Parent Class
[SingleInstance\<Input>](./SingleInstance.md)

## 설명
키 입력과 관련된 클래스입니다.  

### GetInstance Function
#### Usage
```c++
static Input& GetInstance()
```

#### Parameters
This function has no parameters.

#### Return value
return Input&

#### Remarks
Thread-safe한 Singleton 패턴이 사용되었습니다.

### IsEnglish Function
#### Usage
```c++
bool IsEnglish();
```

#### Parameters
This function has no parameters.

#### Return value
만약 키보드가 영어 입력 상태일 경우 True, 아닐 경우 False를 리턴합니다.

#### Remarks
[EditText](../UI/Widget/EditText.md)등에서 사용하는 함수입니다.  

### GetMousePosition function
#### Usage
```c++
D3DXVECTOR2 GetMousePosition();
```

#### Parameters
This function has no parameters.

#### Return value
마우스의 게임 내 위치를 가져옵니다. 게임의 [Camera](../Camera.md) 위치에 따라 값이 바뀔 수 있습니다.  

### GetMouseSystemPosition function
#### Usage
```c++
D3DXVECTOR2 GetMouseSystemPosition();
```

#### Parameters
This function has no parameters.

#### Return value
마우스의 실제 위치를 가져옵니다. 게임의 창 기준으로, 좌측 상단을 (0, 0)으로 기준을 잡으며, [Camera](../Camera.md) 위치에 따라 값이 바뀌지 않습니다.  
