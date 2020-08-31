# class Camera
## Parent Class
[SingleInstance\<Camera>](./Utils/SingleInstance.md)

## 설명
게임에 사용되는 카메라에 관련된 클래스입니다. 추후 프레임워크 2.0 버전에서는 여러개의 카메라를 지원할 예정이지만, 현재는 1개의 단일 카메라만 지원하기 때문에 Singleton 패턴이 사용되었습니다.  

### ResetCamera Function
#### Usage
```c++
void ResetCamera();
```

#### Parameters
This funciton has no parameters.

#### Return value
This function has no return value.

#### Remarks
카메라의 위치 등을 전부 초기화해 처음 생성됬을때로 되돌립니다.  

### SetupMatrices Function
#### Usage
```c++
void SetupMatrices();
```

#### Parameters
This funciton has no parameters.

#### Return value
This function has no return value.

#### Remarks
렌더링에 사용 될 Matrix를 계산하는 함수입니다. Core에서 자동으로 호출되므로 게임에서 따로 호출할 필요는 없습니다.

### GetCameraPosition Function
#### Usage
```c++
D3DXVECTOR2 GetCameraPosition();
```

#### Parameters
This function has no parameters.

#### Return value
Return Currrent Camera Position (D3DXVECTOR2)

#### Remarks
MoveCamera로 인해 변경될 위치에 대한 좌표를 받아오는 것이 아닌, 해당 프레임이 시작될 때 카메라의 위치를 받아오는 함수입니다.  


### GetLastCameraPosition Function
#### Usage
```c++
D3DXVECTOR2 GetLastCameraPosition();
```

#### Parameters
This function has no parameters.

#### Return value
Return Perivous Frame's Camera Position (D3DXVECTOR2)

#### Remarks
이전 프레임에 있던 카메라의 위치를 받아오는 함수입니다.  

### GetCameraNextPosition Function
#### Usage
```c++
D3DXVECTOR2 GetCameraNextPosition();
```

#### Parameters
This function has no parameters.

#### Return value
Return Next Camera Position (D3DXVECTOR2)

#### Remarks
MoveCamera로 인해 변경될 위치의 좌표를 받아오는 함수입니다.  

### MoveCamera Function
#### Usage
```c++
void MoveCamera(D3DXVECTOR2 Position);
```

#### Parameters
```
Position
```
The Position to move the camera.

#### Return value
This function has no return value.

#### Remarks
이 함수로 인해 이동되었을 경우, GetCameraNextPosition() 과 GetCameraPosition()의 값이 현재 프레임 내에서 서로 다릅니다.

### SetVibration Function
#### Usage
```c++
void SetVibration(float Time)
```

#### Parameters
```
Time
```
카메라를 진동할 시간입니다. (단위 : 초)

#### Return value
This function has no return value.

#### Remarks
1초 이상으로 지정하고 사용할 경우 어색하게 느껴질 수 있습니다.  
