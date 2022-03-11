# Binaryiotools

> Auto-generated documentation for [binaryiotools](../../../binaryiotools/__init__.py) module.

Base binary I/O helper.

- [Binaryiotools](../README.md#binaryiotools-index) / [Modules](../MODULES.md#binaryiotools-modules) / Binaryiotools
    - [IO](#io)
        - [IO().\_\_getitem\_\_](#io__getitem__)
        - [IO().\_\_len\_\_](#io__len__)
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

[[find in source code]](../../../binaryiotools/__init__.py#L36)

```python
class IO():
    def __init__(
        data: bytearray | bytes | None = None,
        idx: int = 0,
        littleEndian: bool = False,
        boolSize: int = 8,
        stringEncoding: str = 'U',
    ):
```

Class to handle i/o to a byte buffer or file-like object.

### IO().\_\_getitem\_\_

[[find in source code]](../../../binaryiotools/__init__.py#L68)

```python
def __getitem__(idx: int):
```

Get data at a specific idx.

### IO().\_\_len\_\_

[[find in source code]](../../../binaryiotools/__init__.py#L64)

```python
def __len__() -> int:
```

Length of data.

### IO().addBytes

[[find in source code]](../../../binaryiotools/__init__.py#L658)

```python
def addBytes(ioBytes: Any):
```

Add some raw bytes and advance the index.

alias for setBytes()

#### Arguments

- `bytes` - can be a string, bytearray, or another IO object

### IO().beginContext

[[find in source code]](../../../binaryiotools/__init__.py#L94)

```python
def beginContext(newIndex: int):
```

Start a new context where the index can be changed all you want...

and when endContext() is called, it will be restored to the current position

### IO().bool16

[[find in source code]](../../../binaryiotools/__init__.py#L172)

```python
@property
def bool16() -> bool:
```

Get bool16.

### IO().bool16

[[find in source code]](../../../binaryiotools/__init__.py#L177)

```python
@bool16.setter
def bool16(ioBool: bool):
```

Set bool16.

### IO().bool32

[[find in source code]](../../../binaryiotools/__init__.py#L182)

```python
@property
def bool32() -> bool:
```

Get bool32.

### IO().bool32

[[find in source code]](../../../binaryiotools/__init__.py#L187)

```python
@bool32.setter
def bool32(ioBool: bool):
```

Set bool32.

### IO().bool64

[[find in source code]](../../../binaryiotools/__init__.py#L192)

```python
@property
def bool64() -> bool:
```

Get bool64.

### IO().bool64

[[find in source code]](../../../binaryiotools/__init__.py#L197)

```python
@bool64.setter
def bool64(ioBool: bool):
```

Set bool64.

### IO().bool8

[[find in source code]](../../../binaryiotools/__init__.py#L162)

```python
@property
def bool8() -> bool:
```

Get bool8.

### IO().bool8

[[find in source code]](../../../binaryiotools/__init__.py#L167)

```python
@bool8.setter
def bool8(ioBool: bool):
```

Set a bool8.

### IO().boolean

[[find in source code]](../../../binaryiotools/__init__.py#L135)

```python
@property
def boolean() -> bool:
```

Return bool.

### IO().boolean

[[find in source code]](../../../binaryiotools/__init__.py#L148)

```python
@boolean.setter
def boolean(ioBool: bool):
```

Set bool.

### IO().byte

[[find in source code]](../../../binaryiotools/__init__.py#L202)

```python
@property
def byte() -> Any:
```

Get byte.

### IO().byte

[[find in source code]](../../../binaryiotools/__init__.py#L207)

```python
@byte.setter
def byte(byte: Any):
```

Set byte.

### IO().cString

[[find in source code]](../../../binaryiotools/__init__.py#L845)

```python
@property
def cString() -> str:
```

Read a sequence of chars until the next null byte.

### IO().cString

[[find in source code]](../../../binaryiotools/__init__.py#L850)

```python
@cString.setter
def cString(text: str):
```

Set a sequence of chars and add a null byte.

### IO().cStringA

[[find in source code]](../../../binaryiotools/__init__.py#L856)

```python
@property
def cStringA() -> str:
```

Read a sequence of chars until the next null byte in ascii.

### IO().cStringA

[[find in source code]](../../../binaryiotools/__init__.py#L861)

```python
@cStringA.setter
def cStringA(text: str):
```

Set a sequence of chars and add a null byte in ascii.

### IO().cStringU

[[find in source code]](../../../binaryiotools/__init__.py#L878)

```python
@property
def cStringU() -> str:
```

Read a sequence of chars until the next null byte in utf-8.

### IO().cStringU

[[find in source code]](../../../binaryiotools/__init__.py#L883)

```python
@cStringU.setter
def cStringU(text: str):
```

Set a sequence of chars and add a null byte in utf-8.

### IO().cStringW

[[find in source code]](../../../binaryiotools/__init__.py#L867)

```python
@property
def cStringW() -> str:
```

Read a sequence of chars until the next null byte in ucs-2.

### IO().cStringW

[[find in source code]](../../../binaryiotools/__init__.py#L872)

```python
@cStringW.setter
def cStringW(text: str):
```

Set a sequence of chars and add a null byte in ucs-2.

### IO().data

[[find in source code]](../../../binaryiotools/__init__.py#L72)

```python
@property
def data() -> bytearray:
```

Return data.

### IO().data

[[find in source code]](../../../binaryiotools/__init__.py#L77)

```python
@data.setter
def data(data: bytearray) -> None:
```

Set data.

### IO().double

[[find in source code]](../../../binaryiotools/__init__.py#L602)

```python
@property
def double() -> float:
```

Get a double.

### IO().double

[[find in source code]](../../../binaryiotools/__init__.py#L607)

```python
@double.setter
def double(floating: float):
```

Set a double.

### IO().dword

[[find in source code]](../../../binaryiotools/__init__.py#L242)

```python
@property
def dword() -> Any:
```

Get a dword.

### IO().dword

[[find in source code]](../../../binaryiotools/__init__.py#L247)

```python
@dword.setter
def dword(dword: Any):
```

Set a dword.

### IO().endContext

[[find in source code]](../../../binaryiotools/__init__.py#L101)

```python
def endContext():
```

Restore the index to the previous location where it was when	beginContext() was called.

### IO().float32

[[find in source code]](../../../binaryiotools/__init__.py#L402)

```python
@property
def float32() -> float:
```

Get a float32.

### IO().float32

[[find in source code]](../../../binaryiotools/__init__.py#L409)

```python
@float32.setter
def float32(float32: float):
```

Set a float32.

### IO().float32be

[[find in source code]](../../../binaryiotools/__init__.py#L612)

```python
@property
def float32be() -> float:
```

Read the next 32 bit float and advance the index.

### IO().float32be

[[find in source code]](../../../binaryiotools/__init__.py#L617)

```python
@float32be.setter
def float32be(float32be: float):
```

Set a 32 bit float.

### IO().float32le

[[find in source code]](../../../binaryiotools/__init__.py#L622)

```python
@property
def float32le() -> float:
```

Read the next 32 bit float and advance the index.

### IO().float32le

[[find in source code]](../../../binaryiotools/__init__.py#L627)

```python
@float32le.setter
def float32le(float32le: float):
```

Set a 32 bit float.

### IO().float64

[[find in source code]](../../../binaryiotools/__init__.py#L417)

```python
@property
def float64() -> float:
```

Get a float64.

### IO().float64

[[find in source code]](../../../binaryiotools/__init__.py#L424)

```python
@float64.setter
def float64(float64: float):
```

Set a float64.

### IO().float64be

[[find in source code]](../../../binaryiotools/__init__.py#L632)

```python
@property
def float64be() -> float:
```

Read the next 64 bit float and advance the index.

### IO().float64be

[[find in source code]](../../../binaryiotools/__init__.py#L637)

```python
@float64be.setter
def float64be(float64be: float):
```

Set a 64 bit float.

### IO().float64le

[[find in source code]](../../../binaryiotools/__init__.py#L642)

```python
@property
def float64le() -> float:
```

Read the next 64 bit float and advance the index.

### IO().float64le

[[find in source code]](../../../binaryiotools/__init__.py#L647)

```python
@float64le.setter
def float64le(float64le: float):
```

Set a 64 bit float.

### IO().floating

[[find in source code]](../../../binaryiotools/__init__.py#L592)

```python
@property
def floating() -> float:
```

Get a float.

### IO().floating

[[find in source code]](../../../binaryiotools/__init__.py#L597)

```python
@floating.setter
def floating(floating: float):
```

Set a float.

### IO().getBytes

[[find in source code]](../../../binaryiotools/__init__.py#L652)

```python
def getBytes(nbytes: int):
```

Grab some raw bytes and advance the index.

### IO().i16

[[find in source code]](../../../binaryiotools/__init__.py#L312)

```python
@property
def i16() -> int:
```

Get an int16.

### IO().i16

[[find in source code]](../../../binaryiotools/__init__.py#L319)

```python
@i16.setter
def i16(i16: int):
```

Set an int16.

### IO().i16be

[[find in source code]](../../../binaryiotools/__init__.py#L502)

```python
@property
def i16be() -> int:
```

Read the next signed int16 and advance the index.

### IO().i16be

[[find in source code]](../../../binaryiotools/__init__.py#L507)

```python
@i16be.setter
def i16be(i16be: int):
```

Set the int16.

### IO().i16le

[[find in source code]](../../../binaryiotools/__init__.py#L492)

```python
@property
def i16le() -> int:
```

Read the next signed int16 and advance the index.

### IO().i16le

[[find in source code]](../../../binaryiotools/__init__.py#L497)

```python
@i16le.setter
def i16le(i16le: int):
```

Set the int16.

### IO().i32

[[find in source code]](../../../binaryiotools/__init__.py#L342)

```python
@property
def i32() -> int:
```

Get an int32.

### IO().i32

[[find in source code]](../../../binaryiotools/__init__.py#L349)

```python
@i32.setter
def i32(i32: int):
```

Set an int32.

### IO().i32be

[[find in source code]](../../../binaryiotools/__init__.py#L542)

```python
@property
def i32be() -> int:
```

Read the next signed int32 and advance the index.

### IO().i32be

[[find in source code]](../../../binaryiotools/__init__.py#L547)

```python
@i32be.setter
def i32be(i32be: int):
```

Set the int32.

### IO().i32le

[[find in source code]](../../../binaryiotools/__init__.py#L532)

```python
@property
def i32le() -> int:
```

Read the next signed int32 and advance the index.

### IO().i32le

[[find in source code]](../../../binaryiotools/__init__.py#L537)

```python
@i32le.setter
def i32le(i32le: int):
```

Set the int32.

### IO().i64

[[find in source code]](../../../binaryiotools/__init__.py#L372)

```python
@property
def i64() -> int:
```

Get an int64.

### IO().i64

[[find in source code]](../../../binaryiotools/__init__.py#L379)

```python
@i64.setter
def i64(i64: int):
```

Set an int64.

### IO().i64be

[[find in source code]](../../../binaryiotools/__init__.py#L582)

```python
@property
def i64be() -> int:
```

Read the next signed int64 and advance the index.

### IO().i64be

[[find in source code]](../../../binaryiotools/__init__.py#L587)

```python
@i64be.setter
def i64be(i64be: int):
```

Set the int64.

### IO().i64le

[[find in source code]](../../../binaryiotools/__init__.py#L572)

```python
@property
def i64le() -> int:
```

Read the next signed int64 and advance the index.

### IO().i64le

[[find in source code]](../../../binaryiotools/__init__.py#L577)

```python
@i64le.setter
def i64le(i64le: int):
```

Set the int64.

### IO().i8

[[find in source code]](../../../binaryiotools/__init__.py#L282)

```python
@property
def i8() -> int:
```

Get an int8.

### IO().i8

[[find in source code]](../../../binaryiotools/__init__.py#L289)

```python
@i8.setter
def i8(i8: int):
```

Set an int8.

### IO().i8be

[[find in source code]](../../../binaryiotools/__init__.py#L462)

```python
@property
def i8be() -> int:
```

Read the next signed int8 and advance the index.

### IO().i8be

[[find in source code]](../../../binaryiotools/__init__.py#L467)

```python
@i8be.setter
def i8be(i8be: int):
```

Set the int8.

### IO().i8le

[[find in source code]](../../../binaryiotools/__init__.py#L452)

```python
@property
def i8le() -> int:
```

Read the next signed int8 and advance the index.

### IO().i8le

[[find in source code]](../../../binaryiotools/__init__.py#L457)

```python
@i8le.setter
def i8le(i8le: int):
```

Set the int8.

### IO().index

[[find in source code]](../../../binaryiotools/__init__.py#L84)

```python
@property
def index() -> int:
```

Return data.

### IO().index

[[find in source code]](../../../binaryiotools/__init__.py#L89)

```python
@index.setter
def index(index: int) -> None:
```

Set index.

### IO().qword

[[find in source code]](../../../binaryiotools/__init__.py#L262)

```python
@property
def qword() -> Any:
```

Get a qword.

### IO().qword

[[find in source code]](../../../binaryiotools/__init__.py#L267)

```python
@qword.setter
def qword(qword: Any):
```

Set a qword.

### IO().setBytes

[[find in source code]](../../../binaryiotools/__init__.py#L667)

```python
def setBytes(ioBytes: Any):
```

Add some raw bytes and advance the index.

alias for addBytes()

#### Arguments

- `ioBytes` - can be a string, bytearray, or another IO object

### IO().sz754

[[find in source code]](../../../binaryiotools/__init__.py#L717)

```python
@property
def sz754() -> Any:
```

sz754.

### IO().sz754

[[find in source code]](../../../binaryiotools/__init__.py#L722)

```python
@sz754.setter
def sz754(sz754: Any):
```

Set sz754.

### IO().sz754A

[[find in source code]](../../../binaryiotools/__init__.py#L727)

```python
@property
def sz754A() -> Any:
```

sz754A.

### IO().sz754A

[[find in source code]](../../../binaryiotools/__init__.py#L732)

```python
@sz754A.setter
def sz754A(sz754: Any):
```

Set sz754A.

### IO().sz754U

[[find in source code]](../../../binaryiotools/__init__.py#L747)

```python
@property
def sz754U() -> Any:
```

sz754U.

### IO().sz754U

[[find in source code]](../../../binaryiotools/__init__.py#L752)

```python
@sz754U.setter
def sz754U(sz754: Any):
```

Set sz754U.

### IO().sz754W

[[find in source code]](../../../binaryiotools/__init__.py#L737)

```python
@property
def sz754W() -> Any:
```

sz754W.

### IO().sz754W

[[find in source code]](../../../binaryiotools/__init__.py#L742)

```python
@sz754W.setter
def sz754W(sz754: Any):
```

Set sz754W.

### IO().textLine

[[find in source code]](../../../binaryiotools/__init__.py#L785)

```python
@property
def textLine() -> str:
```

Read a sequence of chars until the next new line char.

### IO().textLine

[[find in source code]](../../../binaryiotools/__init__.py#L793)

```python
@textLine.setter
def textLine(text: str):
```

Set a sequence of chars until the next new line char.

### IO().textLineA

[[find in source code]](../../../binaryiotools/__init__.py#L800)

```python
@property
def textLineA() -> str:
```

Read a sequence of chars until the next new line char in ascii.

### IO().textLineA

[[find in source code]](../../../binaryiotools/__init__.py#L808)

```python
@textLineA.setter
def textLineA(text: str):
```

Set a sequence of chars until the next new line char in ascii.

### IO().textLineU

[[find in source code]](../../../binaryiotools/__init__.py#L830)

```python
@property
def textLineU() -> str:
```

Read a sequence of chars until the next new line char in utf-8.

### IO().textLineU

[[find in source code]](../../../binaryiotools/__init__.py#L838)

```python
@textLineU.setter
def textLineU(text: str):
```

Set a sequence of chars until the next new line char in utf-8.

### IO().textLineW

[[find in source code]](../../../binaryiotools/__init__.py#L815)

```python
@property
def textLineW() -> str:
```

Read a sequence of chars until the next new line char in ucs-2.

### IO().textLineW

[[find in source code]](../../../binaryiotools/__init__.py#L823)

```python
@textLineW.setter
def textLineW(text: str):
```

Set a sequence of chars until the next new line char in ucs-2.

### IO().u16

[[find in source code]](../../../binaryiotools/__init__.py#L327)

```python
@property
def u16() -> int:
```

Get an uint16.

### IO().u16

[[find in source code]](../../../binaryiotools/__init__.py#L334)

```python
@u16.setter
def u16(u16: int):
```

Set an unint16.

### IO().u16be

[[find in source code]](../../../binaryiotools/__init__.py#L472)

```python
@property
def u16be() -> int:
```

Read the next uint16 and advance the index.

### IO().u16be

[[find in source code]](../../../binaryiotools/__init__.py#L477)

```python
@u16be.setter
def u16be(u16be: int):
```

Set the uint16.

### IO().u16le

[[find in source code]](../../../binaryiotools/__init__.py#L482)

```python
@property
def u16le() -> int:
```

Read the next uint16 and advance the index.

### IO().u16le

[[find in source code]](../../../binaryiotools/__init__.py#L487)

```python
@u16le.setter
def u16le(u16le: int):
```

Set the uint16.

### IO().u32

[[find in source code]](../../../binaryiotools/__init__.py#L357)

```python
@property
def u32() -> int:
```

Get a uint32.

### IO().u32

[[find in source code]](../../../binaryiotools/__init__.py#L364)

```python
@u32.setter
def u32(u32: int):
```

Set a unint32.

### IO().u32be

[[find in source code]](../../../binaryiotools/__init__.py#L512)

```python
@property
def u32be() -> int:
```

Read the next uint32 and advance the index.

### IO().u32be

[[find in source code]](../../../binaryiotools/__init__.py#L517)

```python
@u32be.setter
def u32be(u32be: int):
```

Set the uint32.

### IO().u32le

[[find in source code]](../../../binaryiotools/__init__.py#L522)

```python
@property
def u32le() -> int:
```

Read the next uint32 and advance the index.

### IO().u32le

[[find in source code]](../../../binaryiotools/__init__.py#L527)

```python
@u32le.setter
def u32le(u32le: int):
```

Set the uint32.

### IO().u64

[[find in source code]](../../../binaryiotools/__init__.py#L387)

```python
@property
def u64() -> int:
```

Get a uint64.

### IO().u64

[[find in source code]](../../../binaryiotools/__init__.py#L394)

```python
@u64.setter
def u64(u64: int):
```

Set a uint64.

### IO().u64be

[[find in source code]](../../../binaryiotools/__init__.py#L552)

```python
@property
def u64be() -> int:
```

Read the next uint64 and advance the index.

### IO().u64be

[[find in source code]](../../../binaryiotools/__init__.py#L557)

```python
@u64be.setter
def u64be(u64be: int):
```

Set the uint64.

### IO().u64le

[[find in source code]](../../../binaryiotools/__init__.py#L562)

```python
@property
def u64le() -> int:
```

Read the next uint64 and advance the index.

### IO().u64le

[[find in source code]](../../../binaryiotools/__init__.py#L567)

```python
@u64le.setter
def u64le(u64le: int):
```

Set the uint64.

### IO().u8

[[find in source code]](../../../binaryiotools/__init__.py#L297)

```python
@property
def u8() -> int:
```

Get an unsigned int.

### IO().u8

[[find in source code]](../../../binaryiotools/__init__.py#L304)

```python
@u8.setter
def u8(u8: int):
```

Set an unsigned int.

### IO().u8be

[[find in source code]](../../../binaryiotools/__init__.py#L432)

```python
@property
def u8be() -> int:
```

Read the next uint8 and advance the index.

### IO().u8be

[[find in source code]](../../../binaryiotools/__init__.py#L437)

```python
@u8be.setter
def u8be(u8be: int):
```

Set the uint8.

### IO().u8le

[[find in source code]](../../../binaryiotools/__init__.py#L442)

```python
@property
def u8le() -> int:
```

Read the next uint8 and advance the index.

### IO().u8le

[[find in source code]](../../../binaryiotools/__init__.py#L447)

```python
@u8le.setter
def u8le(u8le: int):
```

Set the uint8.

### IO().unsignedByte

[[find in source code]](../../../binaryiotools/__init__.py#L212)

```python
@property
def unsignedByte() -> Any:
```

Get unsigned byte.

### IO().unsignedByte

[[find in source code]](../../../binaryiotools/__init__.py#L217)

```python
@unsignedByte.setter
def unsignedByte(byte: Any):
```

Set unsigned byte.

### IO().unsignedDword

[[find in source code]](../../../binaryiotools/__init__.py#L252)

```python
@property
def unsignedDword() -> Any:
```

Get a unsigned dword.

### IO().unsignedDword

[[find in source code]](../../../binaryiotools/__init__.py#L257)

```python
@unsignedDword.setter
def unsignedDword(unsignedDword: Any):
```

Set an unsigned dword.

### IO().unsignedQword

[[find in source code]](../../../binaryiotools/__init__.py#L272)

```python
@property
def unsignedQword() -> Any:
```

Get an unsigned qword.

### IO().unsignedQword

[[find in source code]](../../../binaryiotools/__init__.py#L277)

```python
@unsignedQword.setter
def unsignedQword(unsignedQword: Any):
```

Set an unsigned qword.

### IO().unsignedWord

[[find in source code]](../../../binaryiotools/__init__.py#L232)

```python
@property
def unsignedWord() -> Any:
```

Get an unsigned word.

### IO().unsignedWord

[[find in source code]](../../../binaryiotools/__init__.py#L237)

```python
@unsignedWord.setter
def unsignedWord(unsignedWord: Any):
```

Set an unsigned word.

### IO().word

[[find in source code]](../../../binaryiotools/__init__.py#L222)

```python
@property
def word() -> Any:
```

Get a word.

### IO().word

[[find in source code]](../../../binaryiotools/__init__.py#L227)

```python
@word.setter
def word(word: Any):
```

Set a word.
