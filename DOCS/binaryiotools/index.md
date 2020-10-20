# binaryiotools

> Auto-generated documentation for [binaryiotools](../../binaryiotools/__init__.py) module.

Base binary I/O helper.

- [Binaryiotools](../README.md#binaryiotools-index) / [Modules](../README.md#binaryiotools-modules) / binaryiotools
    - [IO](#io)
        - [IO().addBytes](#ioaddbytes)
        - [IO().beginContext](#iobegincontext)
        - [IO().bool16](#iobool16)
        - [IO().bool16](#iobool16)
        - [IO().bool32](#iobool32)
        - [IO().bool32](#iobool32)
        - [IO().bool64](#iobool64)
        - [IO().bool64](#iobool64)
        - [IO().bool8](#iobool8)
        - [IO().bool8](#iobool8)
        - [IO().boolean](#ioboolean)
        - [IO().boolean](#ioboolean)
        - [IO().byte](#iobyte)
        - [IO().byte](#iobyte)
        - [IO().cString](#iocstring)
        - [IO().cString](#iocstring)
        - [IO().cStringA](#iocstringa)
        - [IO().cStringA](#iocstringa)
        - [IO().cStringU](#iocstringu)
        - [IO().cStringU](#iocstringu)
        - [IO().cStringW](#iocstringw)
        - [IO().cStringW](#iocstringw)
        - [IO().data](#iodata)
        - [IO().data](#iodata)
        - [IO().double](#iodouble)
        - [IO().double](#iodouble)
        - [IO().dword](#iodword)
        - [IO().dword](#iodword)
        - [IO().endContext](#ioendcontext)
        - [IO().float32](#iofloat32)
        - [IO().float32](#iofloat32)
        - [IO().float32be](#iofloat32be)
        - [IO().float32be](#iofloat32be)
        - [IO().float32le](#iofloat32le)
        - [IO().float32le](#iofloat32le)
        - [IO().float64](#iofloat64)
        - [IO().float64](#iofloat64)
        - [IO().float64be](#iofloat64be)
        - [IO().float64be](#iofloat64be)
        - [IO().float64le](#iofloat64le)
        - [IO().float64le](#iofloat64le)
        - [IO().floating](#iofloating)
        - [IO().floating](#iofloating)
        - [IO().getBytes](#iogetbytes)
        - [IO().i16](#ioi16)
        - [IO().i16](#ioi16)
        - [IO().i16be](#ioi16be)
        - [IO().i16be](#ioi16be)
        - [IO().i16le](#ioi16le)
        - [IO().i16le](#ioi16le)
        - [IO().i32](#ioi32)
        - [IO().i32](#ioi32)
        - [IO().i32be](#ioi32be)
        - [IO().i32be](#ioi32be)
        - [IO().i32le](#ioi32le)
        - [IO().i32le](#ioi32le)
        - [IO().i64](#ioi64)
        - [IO().i64](#ioi64)
        - [IO().i64be](#ioi64be)
        - [IO().i64be](#ioi64be)
        - [IO().i64le](#ioi64le)
        - [IO().i64le](#ioi64le)
        - [IO().i8](#ioi8)
        - [IO().i8](#ioi8)
        - [IO().i8be](#ioi8be)
        - [IO().i8be](#ioi8be)
        - [IO().i8le](#ioi8le)
        - [IO().i8le](#ioi8le)
        - [IO().index](#ioindex)
        - [IO().index](#ioindex)
        - [IO().qword](#ioqword)
        - [IO().qword](#ioqword)
        - [IO().setBytes](#iosetbytes)
        - [IO().sz754](#iosz754)
        - [IO().sz754](#iosz754)
        - [IO().sz754A](#iosz754a)
        - [IO().sz754A](#iosz754a)
        - [IO().sz754U](#iosz754u)
        - [IO().sz754U](#iosz754u)
        - [IO().sz754W](#iosz754w)
        - [IO().sz754W](#iosz754w)
        - [IO().textLine](#iotextline)
        - [IO().textLine](#iotextline)
        - [IO().textLineA](#iotextlinea)
        - [IO().textLineA](#iotextlinea)
        - [IO().textLineU](#iotextlineu)
        - [IO().textLineU](#iotextlineu)
        - [IO().textLineW](#iotextlinew)
        - [IO().textLineW](#iotextlinew)
        - [IO().u16](#iou16)
        - [IO().u16](#iou16)
        - [IO().u16be](#iou16be)
        - [IO().u16be](#iou16be)
        - [IO().u16le](#iou16le)
        - [IO().u16le](#iou16le)
        - [IO().u32](#iou32)
        - [IO().u32](#iou32)
        - [IO().u32be](#iou32be)
        - [IO().u32be](#iou32be)
        - [IO().u32le](#iou32le)
        - [IO().u32le](#iou32le)
        - [IO().u64](#iou64)
        - [IO().u64](#iou64)
        - [IO().u64be](#iou64be)
        - [IO().u64be](#iou64be)
        - [IO().u64le](#iou64le)
        - [IO().u64le](#iou64le)
        - [IO().u8](#iou8)
        - [IO().u8](#iou8)
        - [IO().u8be](#iou8be)
        - [IO().u8be](#iou8be)
        - [IO().u8le](#iou8le)
        - [IO().u8le](#iou8le)
        - [IO().unsignedByte](#iounsignedbyte)
        - [IO().unsignedByte](#iounsignedbyte)
        - [IO().unsignedDword](#iounsigneddword)
        - [IO().unsignedDword](#iounsigneddword)
        - [IO().unsignedQword](#iounsignedqword)
        - [IO().unsignedQword](#iounsignedqword)
        - [IO().unsignedWord](#iounsignedword)
        - [IO().unsignedWord](#iounsignedword)
        - [IO().word](#ioword)
        - [IO().word](#ioword)

Does boilerplate things like reading the next uint32 from a file or binary stream

Create a new IO object and initialize/ set data

Example

```python
f = open(fileName, 'rb')
data = f.read()
f.close()
io = IO(data)
width = io.u32
height = io.u32
```

The example above reads a file in binary and sets the variables width and height
as the first two unsigned integer 32s

For a file starting with the bytes:

```none
00 00 00 C8 00 01 90
```

The values for width and height would be 200, 400

## IO

[[find in source code]](../../binaryiotools/__init__.py#L35)

```python
class IO():
    def __init__(
        data: Optional[bytearray] = None,
        idx: int = 0,
        littleEndian: bool = False,
        boolSize: int = 8,
        stringEncoding: str = 'U',
    ):
```

Class to handle i/o to a byte buffer or file-like object

### IO().addBytes

[[find in source code]](../../binaryiotools/__init__.py#L646)

```python
def addBytes(ioBytes: Union[(str, bytearray, IO, int, float)]):
```

add some raw bytes and advance the index

alias for setBytes()

#### Arguments

- `bytes` - can be a string, bytearray, or another IO object

### IO().beginContext

[[find in source code]](../../binaryiotools/__init__.py#L85)

```python
def beginContext(newIndex: int):
```

Start a new context where the index can be changed all you want,
and when endContext() is called, it will be restored to the current position

### IO().bool16

[[find in source code]](../../binaryiotools/__init__.py#L158)

```python
@property
def bool16() -> Union[(str, bytearray, IO, int, float)]:
```

get bool16

### IO().bool16

[[find in source code]](../../binaryiotools/__init__.py#L163)

```python
@bool16.setter
def bool16(ioBool: Union[(str, bytearray, IO, int, float)]):
```

set bool16

### IO().bool32

[[find in source code]](../../binaryiotools/__init__.py#L168)

```python
@property
def bool32() -> Union[(str, bytearray, IO, int, float)]:
```

get bool32

### IO().bool32

[[find in source code]](../../binaryiotools/__init__.py#L173)

```python
@bool32.setter
def bool32(ioBool: Union[(str, bytearray, IO, int, float)]):
```

set bool32

### IO().bool64

[[find in source code]](../../binaryiotools/__init__.py#L178)

```python
@property
def bool64() -> Union[(str, bytearray, IO, int, float)]:
```

get bool64

### IO().bool64

[[find in source code]](../../binaryiotools/__init__.py#L183)

```python
@bool64.setter
def bool64(ioBool: Union[(str, bytearray, IO, int, float)]):
```

set bool64

### IO().bool8

[[find in source code]](../../binaryiotools/__init__.py#L148)

```python
@property
def bool8() -> Union[(str, bytearray, IO, int, float)]:
```

get bool8

### IO().bool8

[[find in source code]](../../binaryiotools/__init__.py#L153)

```python
@bool8.setter
def bool8(ioBool: Union[(str, bytearray, IO, int, float)]):
```

set a bool8

### IO().boolean

[[find in source code]](../../binaryiotools/__init__.py#L121)

```python
@property
def boolean():
```

return bool

### IO().boolean

[[find in source code]](../../binaryiotools/__init__.py#L134)

```python
@boolean.setter
def boolean(ioBool: Union[(str, bytearray, IO, int, float)]):
```

set bool

### IO().byte

[[find in source code]](../../binaryiotools/__init__.py#L188)

```python
@property
def byte() -> Union[(str, bytearray, IO, int, float)]:
```

get byte

### IO().byte

[[find in source code]](../../binaryiotools/__init__.py#L193)

```python
@byte.setter
def byte(byte: Union[(str, bytearray, IO, int, float)]):
```

set byte

### IO().cString

[[find in source code]](../../binaryiotools/__init__.py#L837)

```python
@property
def cString() -> Union[(str, bytearray, IO, int, float)]:
```

Read a sequence of chars until the next null byte

### IO().cString

[[find in source code]](../../binaryiotools/__init__.py#L842)

```python
@cString.setter
def cString(text: Union[(str, bytearray, IO, int, float)]):
```

Set a sequence of chars and add a null byte

### IO().cStringA

[[find in source code]](../../binaryiotools/__init__.py#L848)

```python
@property
def cStringA() -> Union[(str, bytearray, IO, int, float)]:
```

Read a sequence of chars until the next null byte in ascii

### IO().cStringA

[[find in source code]](../../binaryiotools/__init__.py#L853)

```python
@cStringA.setter
def cStringA(text: Union[(str, bytearray, IO, int, float)]):
```

Set a sequence of chars and add a null byte in ascii

### IO().cStringU

[[find in source code]](../../binaryiotools/__init__.py#L870)

```python
@property
def cStringU() -> Union[(str, bytearray, IO, int, float)]:
```

Read a sequence of chars until the next null byte in utf-8

### IO().cStringU

[[find in source code]](../../binaryiotools/__init__.py#L875)

```python
@cStringU.setter
def cStringU(text: Union[(str, bytearray, IO, int, float)]):
```

Set a sequence of chars and add a null byte in utf-8

### IO().cStringW

[[find in source code]](../../binaryiotools/__init__.py#L859)

```python
@property
def cStringW() -> Union[(str, bytearray, IO, int, float)]:
```

Read a sequence of chars until the next null byte in ucs-2

### IO().cStringW

[[find in source code]](../../binaryiotools/__init__.py#L864)

```python
@cStringW.setter
def cStringW(text: Union[(str, bytearray, IO, int, float)]):
```

Set a sequence of chars and add a null byte in ucs-2

### IO().data

[[find in source code]](../../binaryiotools/__init__.py#L63)

```python
@property
def data() -> bytearray:
```

return data

### IO().data

[[find in source code]](../../binaryiotools/__init__.py#L68)

```python
@data.setter
def data(data: bytearray) -> None:
```

set data

### IO().double

[[find in source code]](../../binaryiotools/__init__.py#L588)

```python
@property
def double() -> Union[(str, bytearray, IO, int, float)]:
```

get a double

### IO().double

[[find in source code]](../../binaryiotools/__init__.py#L593)

```python
@double.setter
def double(floating: Union[(str, bytearray, IO, int, float)]):
```

set a double

### IO().dword

[[find in source code]](../../binaryiotools/__init__.py#L228)

```python
@property
def dword() -> Union[(str, bytearray, IO, int, float)]:
```

get a dword

### IO().dword

[[find in source code]](../../binaryiotools/__init__.py#L233)

```python
@dword.setter
def dword(dword: Union[(str, bytearray, IO, int, float)]):
```

set a dword

### IO().endContext

[[find in source code]](../../binaryiotools/__init__.py#L92)

```python
def endContext():
```

Restore the index to the previous location where it was when
beginContext() was called

### IO().float32

[[find in source code]](../../binaryiotools/__init__.py#L388)

```python
@property
def float32() -> Union[(str, bytearray, IO, int, float)]:
```

get a float32

### IO().float32

[[find in source code]](../../binaryiotools/__init__.py#L395)

```python
@float32.setter
def float32(float32: Union[(str, bytearray, IO, int, float)]):
```

set a float32

### IO().float32be

[[find in source code]](../../binaryiotools/__init__.py#L598)

```python
@property
def float32be() -> Union[(str, bytearray, IO, int, float)]:
```

read the next 32 bit float and advance the index

### IO().float32be

[[find in source code]](../../binaryiotools/__init__.py#L603)

```python
@float32be.setter
def float32be(float32be: Union[(str, bytearray, IO, int, float)]):
```

set a 32 bit float

### IO().float32le

[[find in source code]](../../binaryiotools/__init__.py#L608)

```python
@property
def float32le() -> Union[(str, bytearray, IO, int, float)]:
```

read the next 32 bit float and advance the index

### IO().float32le

[[find in source code]](../../binaryiotools/__init__.py#L613)

```python
@float32le.setter
def float32le(float32le: Union[(str, bytearray, IO, int, float)]):
```

set a 32 bit float

### IO().float64

[[find in source code]](../../binaryiotools/__init__.py#L403)

```python
@property
def float64() -> Union[(str, bytearray, IO, int, float)]:
```

get a float64

### IO().float64

[[find in source code]](../../binaryiotools/__init__.py#L410)

```python
@float64.setter
def float64(float64: Union[(str, bytearray, IO, int, float)]):
```

set a float64

### IO().float64be

[[find in source code]](../../binaryiotools/__init__.py#L618)

```python
@property
def float64be() -> Union[(str, bytearray, IO, int, float)]:
```

read the next 64 bit float and advance the index

### IO().float64be

[[find in source code]](../../binaryiotools/__init__.py#L623)

```python
@float64be.setter
def float64be(float64be: Union[(str, bytearray, IO, int, float)]):
```

set a 64 bit float

### IO().float64le

[[find in source code]](../../binaryiotools/__init__.py#L628)

```python
@property
def float64le() -> Union[(str, bytearray, IO, int, float)]:
```

read the next 64 bit float and advance the index

### IO().float64le

[[find in source code]](../../binaryiotools/__init__.py#L633)

```python
@float64le.setter
def float64le(float64le: Union[(str, bytearray, IO, int, float)]):
```

set a 64 bit float

### IO().floating

[[find in source code]](../../binaryiotools/__init__.py#L578)

```python
@property
def floating() -> Union[(str, bytearray, IO, int, float)]:
```

get a float

### IO().floating

[[find in source code]](../../binaryiotools/__init__.py#L583)

```python
@floating.setter
def floating(floating: Union[(str, bytearray, IO, int, float)]):
```

set a float

### IO().getBytes

[[find in source code]](../../binaryiotools/__init__.py#L638)

```python
def getBytes(nbytes: int):
```

grab some raw bytes and advance the index

### IO().i16

[[find in source code]](../../binaryiotools/__init__.py#L298)

```python
@property
def i16() -> Union[(str, bytearray, IO, int, float)]:
```

get an int16

### IO().i16

[[find in source code]](../../binaryiotools/__init__.py#L305)

```python
@i16.setter
def i16(i16: Union[(str, bytearray, IO, int, float)]):
```

set an int16

### IO().i16be

[[find in source code]](../../binaryiotools/__init__.py#L488)

```python
@property
def i16be() -> Union[(str, bytearray, IO, int, float)]:
```

read the next signed int16 and advance the index

### IO().i16be

[[find in source code]](../../binaryiotools/__init__.py#L493)

```python
@i16be.setter
def i16be(i16be: Union[(str, bytearray, IO, int, float)]):
```

set the int16

### IO().i16le

[[find in source code]](../../binaryiotools/__init__.py#L478)

```python
@property
def i16le() -> Union[(str, bytearray, IO, int, float)]:
```

read the next signed int16 and advance the index

### IO().i16le

[[find in source code]](../../binaryiotools/__init__.py#L483)

```python
@i16le.setter
def i16le(i16le: Union[(str, bytearray, IO, int, float)]):
```

set the int16

### IO().i32

[[find in source code]](../../binaryiotools/__init__.py#L328)

```python
@property
def i32() -> Union[(str, bytearray, IO, int, float)]:
```

get an int32

### IO().i32

[[find in source code]](../../binaryiotools/__init__.py#L335)

```python
@i32.setter
def i32(i32: Union[(str, bytearray, IO, int, float)]):
```

set an int32

### IO().i32be

[[find in source code]](../../binaryiotools/__init__.py#L528)

```python
@property
def i32be() -> Union[(str, bytearray, IO, int, float)]:
```

read the next signed int32 and advance the index

### IO().i32be

[[find in source code]](../../binaryiotools/__init__.py#L533)

```python
@i32be.setter
def i32be(i32be: Union[(str, bytearray, IO, int, float)]):
```

set the int32

### IO().i32le

[[find in source code]](../../binaryiotools/__init__.py#L518)

```python
@property
def i32le() -> Union[(str, bytearray, IO, int, float)]:
```

read the next signed int32 and advance the index

### IO().i32le

[[find in source code]](../../binaryiotools/__init__.py#L523)

```python
@i32le.setter
def i32le(i32le: Union[(str, bytearray, IO, int, float)]):
```

set the int32

### IO().i64

[[find in source code]](../../binaryiotools/__init__.py#L358)

```python
@property
def i64() -> Union[(str, bytearray, IO, int, float)]:
```

get an int64

### IO().i64

[[find in source code]](../../binaryiotools/__init__.py#L365)

```python
@i64.setter
def i64(i64: Union[(str, bytearray, IO, int, float)]):
```

set an int64

### IO().i64be

[[find in source code]](../../binaryiotools/__init__.py#L568)

```python
@property
def i64be() -> Union[(str, bytearray, IO, int, float)]:
```

read the next signed int64 and advance the index

### IO().i64be

[[find in source code]](../../binaryiotools/__init__.py#L573)

```python
@i64be.setter
def i64be(i64be: Union[(str, bytearray, IO, int, float)]):
```

set the int64

### IO().i64le

[[find in source code]](../../binaryiotools/__init__.py#L558)

```python
@property
def i64le() -> Union[(str, bytearray, IO, int, float)]:
```

read the next signed int64 and advance the index

### IO().i64le

[[find in source code]](../../binaryiotools/__init__.py#L563)

```python
@i64le.setter
def i64le(i64le: Union[(str, bytearray, IO, int, float)]):
```

set the int64

### IO().i8

[[find in source code]](../../binaryiotools/__init__.py#L268)

```python
@property
def i8() -> Union[(str, bytearray, IO, int, float)]:
```

get an int8

### IO().i8

[[find in source code]](../../binaryiotools/__init__.py#L275)

```python
@i8.setter
def i8(i8: Union[(str, bytearray, IO, int, float)]):
```

set an int8

### IO().i8be

[[find in source code]](../../binaryiotools/__init__.py#L448)

```python
@property
def i8be() -> Union[(str, bytearray, IO, int, float)]:
```

read the next signed int8 and advance the index

### IO().i8be

[[find in source code]](../../binaryiotools/__init__.py#L453)

```python
@i8be.setter
def i8be(i8be: Union[(str, bytearray, IO, int, float)]):
```

set the int8

### IO().i8le

[[find in source code]](../../binaryiotools/__init__.py#L438)

```python
@property
def i8le() -> Union[(str, bytearray, IO, int, float)]:
```

read the next signed int8 and advance the index

### IO().i8le

[[find in source code]](../../binaryiotools/__init__.py#L443)

```python
@i8le.setter
def i8le(i8le: Union[(str, bytearray, IO, int, float)]):
```

set the int8

### IO().index

[[find in source code]](../../binaryiotools/__init__.py#L75)

```python
@property
def index() -> int:
```

return data

### IO().index

[[find in source code]](../../binaryiotools/__init__.py#L80)

```python
@index.setter
def index(index: int) -> None:
```

set index

### IO().qword

[[find in source code]](../../binaryiotools/__init__.py#L248)

```python
@property
def qword() -> Union[(str, bytearray, IO, int, float)]:
```

get a qword

### IO().qword

[[find in source code]](../../binaryiotools/__init__.py#L253)

```python
@qword.setter
def qword(qword: Union[(str, bytearray, IO, int, float)]):
```

set a qword

### IO().setBytes

[[find in source code]](../../binaryiotools/__init__.py#L656)

```python
def setBytes(ioBytes: Union[(str, bytearray, IO, int, float)]):
```

add some raw bytes and advance the index

alias for addBytes()

#### Arguments

- `ioBytes` - can be a string, bytearray, or another IO object

### IO().sz754

[[find in source code]](../../binaryiotools/__init__.py#L708)

```python
@property
def sz754() -> Union[(str, bytearray, IO, int, float)]:
```

sz754

### IO().sz754

[[find in source code]](../../binaryiotools/__init__.py#L713)

```python
@sz754.setter
def sz754(sz754: Union[(str, bytearray, IO, int, float)]):
```

set sz754

### IO().sz754A

[[find in source code]](../../binaryiotools/__init__.py#L718)

```python
@property
def sz754A() -> Union[(str, bytearray, IO, int, float)]:
```

sz754A

### IO().sz754A

[[find in source code]](../../binaryiotools/__init__.py#L723)

```python
@sz754A.setter
def sz754A(sz754: Union[(str, bytearray, IO, int, float)]):
```

set sz754A

### IO().sz754U

[[find in source code]](../../binaryiotools/__init__.py#L738)

```python
@property
def sz754U() -> Union[(str, bytearray, IO, int, float)]:
```

sz754U

### IO().sz754U

[[find in source code]](../../binaryiotools/__init__.py#L743)

```python
@sz754U.setter
def sz754U(sz754: Union[(str, bytearray, IO, int, float)]):
```

set sz754U

### IO().sz754W

[[find in source code]](../../binaryiotools/__init__.py#L728)

```python
@property
def sz754W() -> Union[(str, bytearray, IO, int, float)]:
```

sz754W

### IO().sz754W

[[find in source code]](../../binaryiotools/__init__.py#L733)

```python
@sz754W.setter
def sz754W(sz754: Union[(str, bytearray, IO, int, float)]):
```

set sz754W

### IO().textLine

[[find in source code]](../../binaryiotools/__init__.py#L777)

```python
@property
def textLine() -> Union[(str, bytearray, IO, int, float)]:
```

Read a sequence of chars until the next new line char

### IO().textLine

[[find in source code]](../../binaryiotools/__init__.py#L785)

```python
@textLine.setter
def textLine(text: Union[(str, bytearray, IO, int, float)]):
```

Set a sequence of chars until the next new line char

### IO().textLineA

[[find in source code]](../../binaryiotools/__init__.py#L792)

```python
@property
def textLineA() -> Union[(str, bytearray, IO, int, float)]:
```

Read a sequence of chars until the next new line char in ascii

### IO().textLineA

[[find in source code]](../../binaryiotools/__init__.py#L800)

```python
@textLineA.setter
def textLineA(text: Union[(str, bytearray, IO, int, float)]):
```

Set a sequence of chars until the next new line char in ascii

### IO().textLineU

[[find in source code]](../../binaryiotools/__init__.py#L822)

```python
@property
def textLineU() -> Union[(str, bytearray, IO, int, float)]:
```

Read a sequence of chars until the next new line char in utf-8

### IO().textLineU

[[find in source code]](../../binaryiotools/__init__.py#L830)

```python
@textLineU.setter
def textLineU(text: Union[(str, bytearray, IO, int, float)]):
```

Set a sequence of chars until the next new line char in utf-8

### IO().textLineW

[[find in source code]](../../binaryiotools/__init__.py#L807)

```python
@property
def textLineW() -> Union[(str, bytearray, IO, int, float)]:
```

Read a sequence of chars until the next new line char in ucs-2

### IO().textLineW

[[find in source code]](../../binaryiotools/__init__.py#L815)

```python
@textLineW.setter
def textLineW(text: Union[(str, bytearray, IO, int, float)]):
```

Set a sequence of chars until the next new line char in ucs-2

### IO().u16

[[find in source code]](../../binaryiotools/__init__.py#L313)

```python
@property
def u16() -> Union[(str, bytearray, IO, int, float)]:
```

get an uint16

### IO().u16

[[find in source code]](../../binaryiotools/__init__.py#L320)

```python
@u16.setter
def u16(u16: Union[(str, bytearray, IO, int, float)]):
```

set an unint16

### IO().u16be

[[find in source code]](../../binaryiotools/__init__.py#L458)

```python
@property
def u16be() -> Union[(str, bytearray, IO, int, float)]:
```

read the next uint16 and advance the index

### IO().u16be

[[find in source code]](../../binaryiotools/__init__.py#L463)

```python
@u16be.setter
def u16be(u16be: Union[(str, bytearray, IO, int, float)]):
```

set the uint16

### IO().u16le

[[find in source code]](../../binaryiotools/__init__.py#L468)

```python
@property
def u16le() -> Union[(str, bytearray, IO, int, float)]:
```

read the next uint16 and advance the index

### IO().u16le

[[find in source code]](../../binaryiotools/__init__.py#L473)

```python
@u16le.setter
def u16le(u16le: Union[(str, bytearray, IO, int, float)]):
```

set the uint16

### IO().u32

[[find in source code]](../../binaryiotools/__init__.py#L343)

```python
@property
def u32() -> Union[(str, bytearray, IO, int, float)]:
```

get a uint32

### IO().u32

[[find in source code]](../../binaryiotools/__init__.py#L350)

```python
@u32.setter
def u32(u32: Union[(str, bytearray, IO, int, float)]):
```

set a unint32

### IO().u32be

[[find in source code]](../../binaryiotools/__init__.py#L498)

```python
@property
def u32be() -> Union[(str, bytearray, IO, int, float)]:
```

read the next uint32 and advance the index

### IO().u32be

[[find in source code]](../../binaryiotools/__init__.py#L503)

```python
@u32be.setter
def u32be(u32be: Union[(str, bytearray, IO, int, float)]):
```

set the uint32

### IO().u32le

[[find in source code]](../../binaryiotools/__init__.py#L508)

```python
@property
def u32le() -> Union[(str, bytearray, IO, int, float)]:
```

read the next uint32 and advance the index

### IO().u32le

[[find in source code]](../../binaryiotools/__init__.py#L513)

```python
@u32le.setter
def u32le(u32le: Union[(str, bytearray, IO, int, float)]):
```

set the uint32

### IO().u64

[[find in source code]](../../binaryiotools/__init__.py#L373)

```python
@property
def u64() -> Union[(str, bytearray, IO, int, float)]:
```

get a uint64

### IO().u64

[[find in source code]](../../binaryiotools/__init__.py#L380)

```python
@u64.setter
def u64(u64: Union[(str, bytearray, IO, int, float)]):
```

set a uint64

### IO().u64be

[[find in source code]](../../binaryiotools/__init__.py#L538)

```python
@property
def u64be() -> Union[(str, bytearray, IO, int, float)]:
```

read the next uint64 and advance the index

### IO().u64be

[[find in source code]](../../binaryiotools/__init__.py#L543)

```python
@u64be.setter
def u64be(u64be: Union[(str, bytearray, IO, int, float)]):
```

set the uint64

### IO().u64le

[[find in source code]](../../binaryiotools/__init__.py#L548)

```python
@property
def u64le() -> Union[(str, bytearray, IO, int, float)]:
```

read the next uint64 and advance the index

### IO().u64le

[[find in source code]](../../binaryiotools/__init__.py#L553)

```python
@u64le.setter
def u64le(u64le: Union[(str, bytearray, IO, int, float)]):
```

set the uint64

### IO().u8

[[find in source code]](../../binaryiotools/__init__.py#L283)

```python
@property
def u8() -> Union[(str, bytearray, IO, int, float)]:
```

get an unsigned int

### IO().u8

[[find in source code]](../../binaryiotools/__init__.py#L290)

```python
@u8.setter
def u8(u8: Union[(str, bytearray, IO, int, float)]):
```

set an unsigned int

### IO().u8be

[[find in source code]](../../binaryiotools/__init__.py#L418)

```python
@property
def u8be() -> Union[(str, bytearray, IO, int, float)]:
```

read the next uint8 and advance the index

### IO().u8be

[[find in source code]](../../binaryiotools/__init__.py#L423)

```python
@u8be.setter
def u8be(u8be: Union[(str, bytearray, IO, int, float)]):
```

set the uint8

### IO().u8le

[[find in source code]](../../binaryiotools/__init__.py#L428)

```python
@property
def u8le() -> Union[(str, bytearray, IO, int, float)]:
```

read the next uint8 and advance the index

### IO().u8le

[[find in source code]](../../binaryiotools/__init__.py#L433)

```python
@u8le.setter
def u8le(u8le: Union[(str, bytearray, IO, int, float)]):
```

set the uint8

### IO().unsignedByte

[[find in source code]](../../binaryiotools/__init__.py#L198)

```python
@property
def unsignedByte() -> Union[(str, bytearray, IO, int, float)]:
```

get unsigned byte

### IO().unsignedByte

[[find in source code]](../../binaryiotools/__init__.py#L203)

```python
@unsignedByte.setter
def unsignedByte(byte: Union[(str, bytearray, IO, int, float)]):
```

set unsigned byte

### IO().unsignedDword

[[find in source code]](../../binaryiotools/__init__.py#L238)

```python
@property
def unsignedDword() -> Union[(str, bytearray, IO, int, float)]:
```

get a unsigned dword

### IO().unsignedDword

[[find in source code]](../../binaryiotools/__init__.py#L243)

```python
@unsignedDword.setter
def unsignedDword(unsignedDword: Union[(str, bytearray, IO, int, float)]):
```

set an unsigned dword

### IO().unsignedQword

[[find in source code]](../../binaryiotools/__init__.py#L258)

```python
@property
def unsignedQword() -> Union[(str, bytearray, IO, int, float)]:
```

get an unsigned qword

### IO().unsignedQword

[[find in source code]](../../binaryiotools/__init__.py#L263)

```python
@unsignedQword.setter
def unsignedQword(unsignedQword: Union[(str, bytearray, IO, int, float)]):
```

set an unsigned qword

### IO().unsignedWord

[[find in source code]](../../binaryiotools/__init__.py#L218)

```python
@property
def unsignedWord() -> Union[(str, bytearray, IO, int, float)]:
```

get an unsigned word

### IO().unsignedWord

[[find in source code]](../../binaryiotools/__init__.py#L223)

```python
@unsignedWord.setter
def unsignedWord(unsignedWord: Union[(str, bytearray, IO, int, float)]):
```

set an unsigned word

### IO().word

[[find in source code]](../../binaryiotools/__init__.py#L208)

```python
@property
def word() -> Union[(str, bytearray, IO, int, float)]:
```

get a word

### IO().word

[[find in source code]](../../binaryiotools/__init__.py#L213)

```python
@word.setter
def word(word: Union[(str, bytearray, IO, int, float)]):
```

set a word
