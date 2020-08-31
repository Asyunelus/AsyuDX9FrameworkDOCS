# class Time
## 설명
DeltaTime 관리와 FPS 계산을 해주는 클래스

## Parent Class
[SingleInstance\<Time>](./SingleInstance.md)

### FPS Variable
#### Var Type
int

#### Usage
```c++
int CurrentFPS = Time::GetInstance().FPS;
```

#### Remarks
현재 초당 프레임수의 값입니다.

### NowTime Variable
#### Var Type
DWORD (unsigned long)

#### Usage
```c++
DWORD CurrentSystemTime = Time::GetInstance().NowTime;
```

#### Remarks
현재 시간의 수치를 DWORD 타입으로 가져옵니다. 2^32 밀리초마다 0으로 초기화 되는 값입니다.  

### TimeScale Variable
#### Var Type
float

#### Usage
```c++
Time::GetInstance().TimeScale = 2.0f;//게임의 속도를 2배로 설정
```

#### Remarks
게임의 속도를 조절하는 용도로 사용됩니다. 이 수치에 따라 DeltaTime의 값이 자동으로 조정됩니다.  


### DeltaTime Variable
#### Usage
```c++
float DeltaTime = Time::GetInstance().DeltaTime;
```

#### Remarks
전 프레임과 현재 프레임 사이의 간격입니다. 단위는 초 입니다.  
TimeScale의 변수값에 따라 값이 변동될 수 있으므로, 실제 시간을 사용해야 되는 요소들 (게임 플레이 타임 등)에는 해당 변수를 사용하면 안됩니다.  
