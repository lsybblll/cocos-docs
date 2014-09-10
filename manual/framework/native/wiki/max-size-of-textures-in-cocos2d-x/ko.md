

#Cocos2d-x에서 플랫폼별 최대 텍스쳐 크기


이론적으로 Cocos2d-x는 어떤 크기의 텍스쳐도 표현할수 있지만, 텍스쳐의 최대크기는 하드웨어에 의해 제한됩니다.
플랫폼의 에뮬레이터에서 텍스쳐 크기 제한을 아래에 제공하고 있습니다.

|플랫폼|최대크기(pixel)|
|------------|------------|
|win32	|2048 * 2048|
|android	|4096 * 4096|
|iPhone3	|1024 * 1024|
|iPhone3GS	|2048 * 2048|
|iPhone4	|2048 * 2048|


실기기에서는 또다른 제한이 있을 수 있습니다. 예를 들어 : G3(Hero) 1024*1024, iPhone4 2048*2048

그러므로 다중 플랫폼 게임을 원할히 개발하기 위해서는 텍스쳐 크기를  최저사양인 1024 * 1024로 유지하기 바랍니다.

기기에서 지원하는 텍스쳐 최대크기를 얻는 코드:(시뮬레이터에서는 지원하지 않을 수 있습니다.)

```
GLint m_maxTextureSize = 0;
glGetIntegerv(GL_MAX_TEXTURE_SIZE, &m_maxTextureSize);
```
