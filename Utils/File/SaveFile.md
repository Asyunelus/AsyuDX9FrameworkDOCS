# class SaveFile
> 파일을 저장하기 위한 유틸입니다. 간단하게 사용할 수 있습니다.
## 설명
[bifstream](./bifstream.md) 과 [bofstream](./bofstream.md)을 활용해 제작된 유틸입니다.  
다양한 자료형을 이름과 같이 저장할 수 있습니다.  

## 함수 목록
### Constructor
#### Usage
```c++
SaveFile(std::wstring path)
```

#### Parameters
```
path
```
The path of the file to be saved.

#### Return value
This function has no return value.

#### Remarks
이 함수는 생성자입니다.  
경로를 지정하지 않은 생성자는 없습니다.  


### Load Function
#### Usage
```c++
void Load();
```

#### Parameters
This function has no parameters.

#### Return value
This function has no return value.

#### Remarks
이 함수는 동기적인 데이터 로딩을 진행합니다.  
파일크기가 커 로딩이 오래걸릴 경우 프로그램이 멈출 수 있습니다.  

### AsyncLoad Function
#### Usage
```c++
void AsyncLoad();
```

#### Parameters
This function has no parameters.

#### Return value
This function has no return value.

#### Remarks
이 함수는 비동기적인 데이터 로딩을 진행합니다.  
파일 로딩이 끝나기 전에 GetInt32 등의 함수를 사용한다면 제대로된 값이 나오지 않을 수 있습니다.  

### Save Function
#### Usage
```c++
void Save();
```

#### Parameters
This function has no parameters.

#### Return value
This function has no return value.

#### Remarks
이 함수는 동기적인 데이터 저장을 진행합니다.  
저장할 데이터가 많아 저장이 오래걸릴 경우 프로그램이 멈출 수 있습니다.


### AsyncSave Function
#### Usage
```c++
void AsyncSave();
```

#### Parameters
This function has no parameters.

#### Return value
This function has no return value.

#### Remarks
이 함수는 비동기적인 데이터 저장을 진행합니다.  
파일 저장이 끝나기 전에 프로그램이 종료될 경우 예기치 못한 상황이 발생할 수 있습니다.  

### Get Function
#### Usage
```c++
void Get(std::string name, short value);
void Get(std::string name, int value);
void Get(std::string name, long long value);
void Get(std::string name, float value);
void Get(std::string name, double value);
void Get(std::string name, std::string value);
void Get(std::string name, std::wstring value);

void GetInt16(std::string name, short value);
void GetInt32(std::string name, int value);
void GetInt64(std::string name, long long value);
void GetSingle(std::string name, float value);
void GetDouble(std::string name, double value);
void GetString(std::string name, std::string value);
void GetWideString(std::string name, std::wstring value);
```

#### Parameters
```
name
```
The name of the value to be loaded.

```
value
```
This is the default value to get when loading fails.

#### Return value
This function has no return value.

#### Remarks
이 함수는 7가지 자료형의 로딩을 지원합니다.  
Get(std::string, short)는 GetInt16(std::string, short)으로 리다이렉트 되므로, 컴파일러의 최적화로 최적화가 진행되지 않으면, GetInt16이 성능이 더 좋습니다.  

### Set Function
#### Usage
```c++
void Set(std::string name, short value);
void Set(std::string name, int value);
void Set(std::string name, long long value);
void Set(std::string name, float value);
void Set(std::string name, double value);
void Set(std::string name, std::string value);
void Set(std::string name, std::wstring value);

void SetInt16(std::string name, short value);
void SetInt32(std::string name, int value);
void SetInt64(std::string name, long long value);
void SetSingle(std::string name, float value);
void SetDouble(std::string name, double value);
void SetString(std::string name, std::string value);
void SetWideString(std::string name, std::wstring value);
```

#### Parameters
```
name
```
The name of the value to be saved.

```
value
```
The value to be saved.

#### Return value
This function has no return value.

#### Remarks
이 함수는 7가지 자료형의 저장을 지원합니다.  
Set(std::string, short)는 SetInt16(std::string, short)으로 리다이렉트 되므로, 컴파일러의 최적화로 최적화가 진행되지 않으면, SetInt16이 성능이 더 좋습니다.  
