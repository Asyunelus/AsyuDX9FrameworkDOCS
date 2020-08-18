# struct FRECT
> float형 사각형을 나타내기 위한 RECT 입니다.
## 설명
D3DXVECTOR2, D3DXVECTOR3, FRECT와의 사칙연산 operator를 지원합니다.  

## 함수 목록
### Constructor
#### Usage
```c++
FRECT();
FRECT(float left, float top, float right, float bottom);
```

#### Parameters
```
left
```
Specifies the x-coordinate of the upper-left corner of the rectangle.

```
top
```
Specifies the y-coordinate of the upper-left corner of the rectangle.

```
right
```
Specifies the x-coordinate of the lower-right corner of the rectangle.

```
bottom
```
Specifies the y-coordinate of the lower-right corner of the rectangle.

#### Return value
This function has no return value.

#### Remarks
The FRECT structure is identical to the FRECT structure.

### IsInteract Function
#### Usage
```c++
bool IsInteract(const _FRECT& other);
bool IsInteract(const D3DXVECTOR2& other);
bool IsInteract(const D3DXVECTOR3& other);
```

#### Parameters
```
other
```
Variable to perform collision check for FRECT or Position

#### Return value
Returns True if there was a collision, False otherwise.

### GetOverlapRect Function
#### Usage
```c++
FRECT GetOverlapRect(const _FRECT& other);
```

#### Parameters
```
other
```
겹친 부분을 계산하기 위한 다른 FRECT입니다.  

#### Return value
두 FRECT의 겹친 부분을 반환합니다.  
만약, 두 FRECT가 겹치지 않을 경우, 크기가 0인 FRECT를 리턴합니다.
