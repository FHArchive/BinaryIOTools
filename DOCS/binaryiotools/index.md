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

[[find in source code]](../../binaryiotools/__init__.py#L650)

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

[[find in source code]](../../binaryiotools/__init__.py#L162)

```python
@property
def bool16() -> bool:
```

get bool16

### IO().bool16

[[find in source code]](../../binaryiotools/__init__.py#L167)

```python
@bool16.setter
def bool16(ioBool: bool):
```

set bool16

### IO().bool32

[[find in source code]](../../binaryiotools/__init__.py#L172)

```python
@property
def bool32() -> bool:
```

get bool32

### IO().bool32

[[find in source code]](../../binaryiotools/__init__.py#L177)

```python
@bool32.setter
def bool32(ioBool: bool):
```

set bool32

### IO().bool64

[[find in source code]](../../binaryiotools/__init__.py#L182)

```python
@property
def bool64() -> bool:
```

get bool64

### IO().bool64

[[find in source code]](../../binaryiotools/__init__.py#L187)

```python
@bool64.setter
def bool64(ioBool: bool):
```

set bool64

### IO().bool8

[[find in source code]](../../binaryiotools/__init__.py#L152)

```python
@property
def bool8() -> bool:
```

get bool8

### IO().bool8

[[find in source code]](../../binaryiotools/__init__.py#L157)

```python
@bool8.setter
def bool8(ioBool: bool):
```

set a bool8

### IO().boolean

[[find in source code]](../../binaryiotools/__init__.py#L121)

```python
@property
def boolean() -> bool:
```

return bool

### IO().boolean

[[find in source code]](../../binaryiotools/__init__.py#L136)

```python
@boolean.setter
def boolean(ioBool: bool):
```

set bool

### IO().byte

[[find in source code]](../../binaryiotools/__init__.py#L192)

```python
@property
def byte() -> Union[(str, bytearray, IO, int, float)]:
```

get byte

### IO().byte

[[find in source code]](../../binaryiotools/__init__.py#L197)

```python
@byte.setter
def byte(byte: Union[(str, bytearray, IO, int, float)]):
```

set byte

### IO().cString

[[find in source code]](../../binaryiotools/__init__.py#L841)

```python
@property
def cString() -> str:
```

Read a sequence of chars until the next null byte

### IO().cString

[[find in source code]](../../binaryiotools/__init__.py#L846)

```python
@cString.setter
def cString(text: str):
```

Set a sequence of chars and add a null byte

### IO().cStringA

[[find in source code]](../../binaryiotools/__init__.py#L852)

```python
@property
def cStringA() -> str:
```

Read a sequence of chars until the next null byte in ascii

### IO().cStringA

[[find in source code]](../../binaryiotools/__init__.py#L857)

```python
@cStringA.setter
def cStringA(text: str):
```

Set a sequence of chars and add a null byte in ascii

### IO().cStringU

[[find in source code]](../../binaryiotools/__init__.py#L874)

```python
@property
def cStringU() -> str:
```

Read a sequence of chars until the next null byte in utf-8

### IO().cStringU

[[find in source code]](../../binaryiotools/__init__.py#L879)

```python
@cStringU.setter
def cStringU(text: str):
```

Set a sequence of chars and add a null byte in utf-8

### IO().cStringW

[[find in source code]](../../binaryiotools/__init__.py#L863)

```python
@property
def cStringW() -> str:
```

Read a sequence of chars until the next null byte in ucs-2

### IO().cStringW

[[find in source code]](../../binaryiotools/__init__.py#L868)

```python
@cStringW.setter
def cStringW(text: str):
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

[[find in source code]](../../binaryiotools/__init__.py#L592)

```python
@property
def double() -> float:
```

get a double

### IO().double

[[find in source code]](../../binaryiotools/__init__.py#L597)

```python
@double.setter
def double(floating: float):
```

set a double

### IO().dword

[[find in source code]](../../binaryiotools/__init__.py#L232)

```python
@property
def dword() -> Union[(str, bytearray, IO, int, float)]:
```

get a dword

### IO().dword

[[find in source code]](../../binaryiotools/__init__.py#L237)

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

[[find in source code]](../../binaryiotools/__init__.py#L392)

```python
@property
def float32() -> float:
```

get a float32

### IO().float32

[[find in source code]](../../binaryiotools/__init__.py#L399)

```python
@float32.setter
def float32(float32: float):
```

set a float32

### IO().float32be

[[find in source code]](../../binaryiotools/__init__.py#L602)

```python
@property
def float32be() -> float:
```

read the next 32 bit float and advance the index

### IO().float32be

[[find in source code]](../../binaryiotools/__init__.py#L607)

```python
@float32be.setter
def float32be(float32be: float):
```

set a 32 bit float

### IO().float32le

[[find in source code]](../../binaryiotools/__init__.py#L612)

```python
@property
def float32le() -> float:
```

read the next 32 bit float and advance the index

### IO().float32le

[[find in source code]](../../binaryiotools/__init__.py#L617)

```python
@float32le.setter
def float32le(float32le: float):
```

set a 32 bit float

### IO().float64

[[find in source code]](../../binaryiotools/__init__.py#L407)

```python
@property
def float64() -> float:
```

get a float64

### IO().float64

[[find in source code]](../../binaryiotools/__init__.py#L414)

```python
@float64.setter
def float64(float64: float):
```

set a float64

### IO().float64be

[[find in source code]](../../binaryiotools/__init__.py#L622)

```python
@property
def float64be() -> float:
```

read the next 64 bit float and advance the index

### IO().float64be

[[find in source code]](../../binaryiotools/__init__.py#L627)

```python
@float64be.setter
def float64be(float64be: float):
```

set a 64 bit float

### IO().float64le

[[find in source code]](../../binaryiotools/__init__.py#L632)

```python
@property
def float64le() -> float:
```

read the next 64 bit float and advance the index

### IO().float64le

[[find in source code]](../../binaryiotools/__init__.py#L637)

```python
@float64le.setter
def float64le(float64le: float):
```

set a 64 bit float

### IO().floating

[[find in source code]](../../binaryiotools/__init__.py#L582)

```python
@property
def floating() -> float:
```

get a float

### IO().floating

[[find in source code]](../../binaryiotools/__init__.py#L587)

```python
@floating.setter
def floating(floating: float):
```

set a float

### IO().getBytes

[[find in source code]](../../binaryiotools/__init__.py#L642)

```python
def getBytes(nbytes: int):
```

grab some raw bytes and advance the index

### IO().i16

[[find in source code]](../../binaryiotools/__init__.py#L302)

```python
@property
def i16() -> int:
```

get an int16

### IO().i16

[[find in source code]](../../binaryiotools/__init__.py#L309)

```python
@i16.setter
def i16(i16: int):
```

set an int16

### IO().i16be

[[find in source code]](../../binaryiotools/__init__.py#L492)

```python
@property
def i16be() -> int:
```

read the next signed int16 and advance the index

### IO().i16be

[[find in source code]](../../binaryiotools/__init__.py#L497)

```python
@i16be.setter
def i16be(i16be: int):
```

set the int16

### IO().i16le

[[find in source code]](../../binaryiotools/__init__.py#L482)

```python
@property
def i16le() -> int:
```

read the next signed int16 and advance the index

### IO().i16le

[[find in source code]](../../binaryiotools/__init__.py#L487)

```python
@i16le.setter
def i16le(i16le: int):
```

set the int16

### IO().i32

[[find in source code]](../../binaryiotools/__init__.py#L332)

```python
@property
def i32() -> int:
```

get an int32

### IO().i32

[[find in source code]](../../binaryiotools/__init__.py#L339)

```python
@i32.setter
def i32(i32: int):
```

set an int32

### IO().i32be

[[find in source code]](../../binaryiotools/__init__.py#L532)

```python
@property
def i32be() -> int:
```

read the next signed int32 and advance the index

### IO().i32be

[[find in source code]](../../binaryiotools/__init__.py#L537)

```python
@i32be.setter
def i32be(i32be: int):
```

set the int32

### IO().i32le

[[find in source code]](../../binaryiotools/__init__.py#L522)

```python
@property
def i32le() -> int:
```

read the next signed int32 and advance the index

### IO().i32le

[[find in source code]](../../binaryiotools/__init__.py#L527)

```python
@i32le.setter
def i32le(i32le: int):
```

set the int32

### IO().i64

[[find in source code]](../../binaryiotools/__init__.py#L362)

```python
@property
def i64() -> int:
```

get an int64

### IO().i64

[[find in source code]](../../binaryiotools/__init__.py#L369)

```python
@i64.setter
def i64(i64: int):
```

set an int64

### IO().i64be

[[find in source code]](../../binaryiotools/__init__.py#L572)

```python
@property
def i64be() -> int:
```

read the next signed int64 and advance the index

### IO().i64be

[[find in source code]](../../binaryiotools/__init__.py#L577)

```python
@i64be.setter
def i64be(i64be: int):
```

set the int64

### IO().i64le

[[find in source code]](../../binaryiotools/__init__.py#L562)

```python
@property
def i64le() -> int:
```

read the next signed int64 and advance the index

### IO().i64le

[[find in source code]](../../binaryiotools/__init__.py#L567)

```python
@i64le.setter
def i64le(i64le: int):
```

set the int64

### IO().i8

[[find in source code]](../../binaryiotools/__init__.py#L272)

```python
@property
def i8() -> int:
```

get an int8

### IO().i8

[[find in source code]](../../binaryiotools/__init__.py#L279)

```python
@i8.setter
def i8(i8: int):
```

set an int8

### IO().i8be

[[find in source code]](../../binaryiotools/__init__.py#L452)

```python
@property
def i8be() -> int:
```

read the next signed int8 and advance the index

### IO().i8be

[[find in source code]](../../binaryiotools/__init__.py#L457)

```python
@i8be.setter
def i8be(i8be: int):
```

set the int8

### IO().i8le

[[find in source code]](../../binaryiotools/__init__.py#L442)

```python
@property
def i8le() -> int:
```

read the next signed int8 and advance the index

### IO().i8le

[[find in source code]](../../binaryiotools/__init__.py#L447)

```python
@i8le.setter
def i8le(i8le: int):
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

[[find in source code]](../../binaryiotools/__init__.py#L252)

```python
@property
def qword() -> Union[(str, bytearray, IO, int, float)]:
```

get a qword

### IO().qword

[[find in source code]](../../binaryiotools/__init__.py#L257)

```python
@qword.setter
def qword(qword: Union[(str, bytearray, IO, int, float)]):
```

set a qword

### IO().setBytes

[[find in source code]](../../binaryiotools/__init__.py#L660)

```python
def setBytes(ioBytes: Union[(str, bytearray, IO, int, float)]):
```

add some raw bytes and advance the index

alias for addBytes()

#### Arguments

- `ioBytes` - can be a string, bytearray, or another IO object

### IO().sz754

[[find in source code]](../../binaryiotools/__init__.py#L712)

```python
@property
def sz754() -> Union[(str, bytearray, IO, int, float)]:
```

sz754

### IO().sz754

[[find in source code]](../../binaryiotools/__init__.py#L717)

```python
@sz754.setter
def sz754(sz754: Union[(str, bytearray, IO, int, float)]):
```

set sz754

### IO().sz754A

[[find in source code]](../../binaryiotools/__init__.py#L722)

```python
@property
def sz754A() -> Union[(str, bytearray, IO, int, float)]:
```

sz754A

### IO().sz754A

[[find in source code]](../../binaryiotools/__init__.py#L727)

```python
@sz754A.setter
def sz754A(sz754: Union[(str, bytearray, IO, int, float)]):
```

set sz754A

### IO().sz754U

[[find in source code]](../../binaryiotools/__init__.py#L742)

```python
@property
def sz754U() -> Union[(str, bytearray, IO, int, float)]:
```

sz754U

### IO().sz754U

[[find in source code]](../../binaryiotools/__init__.py#L747)

```python
@sz754U.setter
def sz754U(sz754: Union[(str, bytearray, IO, int, float)]):
```

set sz754U

### IO().sz754W

[[find in source code]](../../binaryiotools/__init__.py#L732)

```python
@property
def sz754W() -> Union[(str, bytearray, IO, int, float)]:
```

sz754W

### IO().sz754W

[[find in source code]](../../binaryiotools/__init__.py#L737)

```python
@sz754W.setter
def sz754W(sz754: Union[(str, bytearray, IO, int, float)]):
```

set sz754W

### IO().textLine

[[find in source code]](../../binaryiotools/__init__.py#L781)

```python
@property
def textLine() -> str:
```

Read a sequence of chars until the next new line char

### IO().textLine

[[find in source code]](../../binaryiotools/__init__.py#L789)

```python
@textLine.setter
def textLine(text: str):
```

Set a sequence of chars until the next new line char

### IO().textLineA

[[find in source code]](../../binaryiotools/__init__.py#L796)

```python
@property
def textLineA() -> str:
```

Read a sequence of chars until the next new line char in ascii

### IO().textLineA

[[find in source code]](../../binaryiotools/__init__.py#L804)

```python
@textLineA.setter
def textLineA(text: str):
```

Set a sequence of chars until the next new line char in ascii

### IO().textLineU

[[find in source code]](../../binaryiotools/__init__.py#L826)

```python
@property
def textLineU() -> str:
```

Read a sequence of chars until the next new line char in utf-8

### IO().textLineU

[[find in source code]](../../binaryiotools/__init__.py#L834)

```python
@textLineU.setter
def textLineU(text: str):
```

Set a sequence of chars until the next new line char in utf-8

### IO().textLineW

[[find in source code]](../../binaryiotools/__init__.py#L811)

```python
@property
def textLineW() -> str:
```

Read a sequence of chars until the next new line char in ucs-2

### IO().textLineW

[[find in source code]](../../binaryiotools/__init__.py#L819)

```python
@textLineW.setter
def textLineW(text: str):
```

Set a sequence of chars until the next new line char in ucs-2

### IO().u16

[[find in source code]](../../binaryiotools/__init__.py#L317)

```python
@property
def u16() -> int:
```

get an uint16

### IO().u16

[[find in source code]](../../binaryiotools/__init__.py#L324)

```python
@u16.setter
def u16(u16: int):
```

set an unint16

### IO().u16be

[[find in source code]](../../binaryiotools/__init__.py#L462)

```python
@property
def u16be() -> int:
```

read the next uint16 and advance the index

### IO().u16be

[[find in source code]](../../binaryiotools/__init__.py#L467)

```python
@u16be.setter
def u16be(u16be: int):
```

set the uint16

### IO().u16le

[[find in source code]](../../binaryiotools/__init__.py#L472)

```python
@property
def u16le() -> int:
```

read the next uint16 and advance the index

### IO().u16le

[[find in source code]](../../binaryiotools/__init__.py#L477)

```python
@u16le.setter
def u16le(u16le: int):
```

set the uint16

### IO().u32

[[find in source code]](../../binaryiotools/__init__.py#L347)

```python
@property
def u32() -> int:
```

get a uint32

### IO().u32

[[find in source code]](../../binaryiotools/__init__.py#L354)

```python
@u32.setter
def u32(u32: int):
```

set a unint32

### IO().u32be

[[find in source code]](../../binaryiotools/__init__.py#L502)

```python
@property
def u32be() -> int:
```

read the next uint32 and advance the index

### IO().u32be

[[find in source code]](../../binaryiotools/__init__.py#L507)

```python
@u32be.setter
def u32be(u32be: int):
```

set the uint32

### IO().u32le

[[find in source code]](../../binaryiotools/__init__.py#L512)

```python
@property
def u32le() -> int:
```

read the next uint32 and advance the index

### IO().u32le

[[find in source code]](../../binaryiotools/__init__.py#L517)

```python
@u32le.setter
def u32le(u32le: int):
```

set the uint32

### IO().u64

[[find in source code]](../../binaryiotools/__init__.py#L377)

```python
@property
def u64() -> int:
```

get a uint64

### IO().u64

[[find in source code]](../../binaryiotools/__init__.py#L384)

```python
@u64.setter
def u64(u64: int):
```

set a uint64

### IO().u64be

[[find in source code]](../../binaryiotools/__init__.py#L542)

```python
@property
def u64be() -> int:
```

read the next uint64 and advance the index

### IO().u64be

[[find in source code]](../../binaryiotools/__init__.py#L547)

```python
@u64be.setter
def u64be(u64be: int):
```

set the uint64

### IO().u64le

[[find in source code]](../../binaryiotools/__init__.py#L552)

```python
@property
def u64le() -> int:
```

read the next uint64 and advance the index

### IO().u64le

[[find in source code]](../../binaryiotools/__init__.py#L557)

```python
@u64le.setter
def u64le(u64le: int):
```

set the uint64

### IO().u8

[[find in source code]](../../binaryiotools/__init__.py#L287)

```python
@property
def u8() -> int:
```

get an unsigned int

### IO().u8

[[find in source code]](../../binaryiotools/__init__.py#L294)

```python
@u8.setter
def u8(u8: int):
```

set an unsigned int

### IO().u8be

[[find in source code]](../../binaryiotools/__init__.py#L422)

```python
@property
def u8be() -> int:
```

read the next uint8 and advance the index

### IO().u8be

[[find in source code]](../../binaryiotools/__init__.py#L427)

```python
@u8be.setter
def u8be(u8be: int):
```

set the uint8

### IO().u8le

[[find in source code]](../../binaryiotools/__init__.py#L432)

```python
@property
def u8le() -> int:
```

read the next uint8 and advance the index

### IO().u8le

[[find in source code]](../../binaryiotools/__init__.py#L437)

```python
@u8le.setter
def u8le(u8le: int):
```

set the uint8

### IO().unsignedByte

[[find in source code]](../../binaryiotools/__init__.py#L202)

```python
@property
def unsignedByte() -> Union[(str, bytearray, IO, int, float)]:
```

get unsigned byte

### IO().unsignedByte

[[find in source code]](../../binaryiotools/__init__.py#L207)

```python
@unsignedByte.setter
def unsignedByte(byte: Union[(str, bytearray, IO, int, float)]):
```

set unsigned byte

### IO().unsignedDword

[[find in source code]](../../binaryiotools/__init__.py#L242)

```python
@property
def unsignedDword() -> Union[(str, bytearray, IO, int, float)]:
```

get a unsigned dword

### IO().unsignedDword

[[find in source code]](../../binaryiotools/__init__.py#L247)

```python
@unsignedDword.setter
def unsignedDword(unsignedDword: Union[(str, bytearray, IO, int, float)]):
```

set an unsigned dword

### IO().unsignedQword

[[find in source code]](../../binaryiotools/__init__.py#L262)

```python
@property
def unsignedQword() -> Union[(str, bytearray, IO, int, float)]:
```

get an unsigned qword

### IO().unsignedQword

[[find in source code]](../../binaryiotools/__init__.py#L267)

```python
@unsignedQword.setter
def unsignedQword(unsignedQword: Union[(str, bytearray, IO, int, float)]):
```

set an unsigned qword

### IO().unsignedWord

[[find in source code]](../../binaryiotools/__init__.py#L222)

```python
@property
def unsignedWord() -> Union[(str, bytearray, IO, int, float)]:
```

get an unsigned word

### IO().unsignedWord

[[find in source code]](../../binaryiotools/__init__.py#L227)

```python
@unsignedWord.setter
def unsignedWord(unsignedWord: Union[(str, bytearray, IO, int, float)]):
```

set an unsigned word

### IO().word

[[find in source code]](../../binaryiotools/__init__.py#L212)

```python
@property
def word() -> Union[(str, bytearray, IO, int, float)]:
```

get a word

### IO().word

[[find in source code]](../../binaryiotools/__init__.py#L217)

```python
@word.setter
def word(word: Union[(str, bytearray, IO, int, float)]):
```

set a word
