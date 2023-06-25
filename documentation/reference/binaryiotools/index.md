# Binaryiotools

[Binaryiotools Index](../README.md#binaryiotools-index) /
Binaryiotools

> Auto-generated documentation for [binaryiotools](../../../binaryiotools/__init__.py) module.

- [Binaryiotools](#binaryiotools)
  - [IO](#io)
    - [IO().__getitem__](#io()__getitem__)
    - [IO().__len__](#io()__len__)
    - [IO().addBytes](#io()addbytes)
    - [IO().beginContext](#io()begincontext)
    - [IO().bool16](#io()bool16)
    - [IO().bool16](#io()bool16-1)
    - [IO().bool32](#io()bool32)
    - [IO().bool32](#io()bool32-1)
    - [IO().bool64](#io()bool64)
    - [IO().bool64](#io()bool64-1)
    - [IO().bool8](#io()bool8)
    - [IO().bool8](#io()bool8-1)
    - [IO().boolean](#io()boolean)
    - [IO().boolean](#io()boolean-1)
    - [IO().byte](#io()byte)
    - [IO().byte](#io()byte-1)
    - [IO().cString](#io()cstring)
    - [IO().cString](#io()cstring-1)
    - [IO().cStringA](#io()cstringa)
    - [IO().cStringA](#io()cstringa-1)
    - [IO().cStringU](#io()cstringu)
    - [IO().cStringU](#io()cstringu-1)
    - [IO().cStringW](#io()cstringw)
    - [IO().cStringW](#io()cstringw-1)
    - [IO().data](#io()data)
    - [IO().data](#io()data-1)
    - [IO().double](#io()double)
    - [IO().double](#io()double-1)
    - [IO().dword](#io()dword)
    - [IO().dword](#io()dword-1)
    - [IO().endContext](#io()endcontext)
    - [IO().float32](#io()float32)
    - [IO().float32](#io()float32-1)
    - [IO().float32be](#io()float32be)
    - [IO().float32be](#io()float32be-1)
    - [IO().float32le](#io()float32le)
    - [IO().float32le](#io()float32le-1)
    - [IO().float64](#io()float64)
    - [IO().float64](#io()float64-1)
    - [IO().float64be](#io()float64be)
    - [IO().float64be](#io()float64be-1)
    - [IO().float64le](#io()float64le)
    - [IO().float64le](#io()float64le-1)
    - [IO().floating](#io()floating)
    - [IO().floating](#io()floating-1)
    - [IO().getBytes](#io()getbytes)
    - [IO().i16](#io()i16)
    - [IO().i16](#io()i16-1)
    - [IO().i16be](#io()i16be)
    - [IO().i16be](#io()i16be-1)
    - [IO().i16le](#io()i16le)
    - [IO().i16le](#io()i16le-1)
    - [IO().i32](#io()i32)
    - [IO().i32](#io()i32-1)
    - [IO().i32be](#io()i32be)
    - [IO().i32be](#io()i32be-1)
    - [IO().i32le](#io()i32le)
    - [IO().i32le](#io()i32le-1)
    - [IO().i64](#io()i64)
    - [IO().i64](#io()i64-1)
    - [IO().i64be](#io()i64be)
    - [IO().i64be](#io()i64be-1)
    - [IO().i64le](#io()i64le)
    - [IO().i64le](#io()i64le-1)
    - [IO().i8](#io()i8)
    - [IO().i8](#io()i8-1)
    - [IO().i8be](#io()i8be)
    - [IO().i8be](#io()i8be-1)
    - [IO().i8le](#io()i8le)
    - [IO().i8le](#io()i8le-1)
    - [IO().index](#io()index)
    - [IO().index](#io()index-1)
    - [IO().qword](#io()qword)
    - [IO().qword](#io()qword-1)
    - [IO().setBytes](#io()setbytes)
    - [IO().sz754](#io()sz754)
    - [IO().sz754](#io()sz754-1)
    - [IO().sz754A](#io()sz754a)
    - [IO().sz754A](#io()sz754a-1)
    - [IO().sz754U](#io()sz754u)
    - [IO().sz754U](#io()sz754u-1)
    - [IO().sz754W](#io()sz754w)
    - [IO().sz754W](#io()sz754w-1)
    - [IO().textLine](#io()textline)
    - [IO().textLine](#io()textline-1)
    - [IO().textLineA](#io()textlinea)
    - [IO().textLineA](#io()textlinea-1)
    - [IO().textLineU](#io()textlineu)
    - [IO().textLineU](#io()textlineu-1)
    - [IO().textLineW](#io()textlinew)
    - [IO().textLineW](#io()textlinew-1)
    - [IO().u16](#io()u16)
    - [IO().u16](#io()u16-1)
    - [IO().u16be](#io()u16be)
    - [IO().u16be](#io()u16be-1)
    - [IO().u16le](#io()u16le)
    - [IO().u16le](#io()u16le-1)
    - [IO().u32](#io()u32)
    - [IO().u32](#io()u32-1)
    - [IO().u32be](#io()u32be)
    - [IO().u32be](#io()u32be-1)
    - [IO().u32le](#io()u32le)
    - [IO().u32le](#io()u32le-1)
    - [IO().u64](#io()u64)
    - [IO().u64](#io()u64-1)
    - [IO().u64be](#io()u64be)
    - [IO().u64be](#io()u64be-1)
    - [IO().u64le](#io()u64le)
    - [IO().u64le](#io()u64le-1)
    - [IO().u8](#io()u8)
    - [IO().u8](#io()u8-1)
    - [IO().u8be](#io()u8be)
    - [IO().u8be](#io()u8be-1)
    - [IO().u8le](#io()u8le)
    - [IO().u8le](#io()u8le-1)
    - [IO().unsignedByte](#io()unsignedbyte)
    - [IO().unsignedByte](#io()unsignedbyte-1)
    - [IO().unsignedDword](#io()unsigneddword)
    - [IO().unsignedDword](#io()unsigneddword-1)
    - [IO().unsignedQword](#io()unsignedqword)
    - [IO().unsignedQword](#io()unsignedqword-1)
    - [IO().unsignedWord](#io()unsignedword)
    - [IO().unsignedWord](#io()unsignedword-1)
    - [IO().word](#io()word)
    - [IO().word](#io()word-1)

## IO

[Show source in __init__.py:36](../../../binaryiotools/__init__.py#L36)

Class to handle i/o to a byte buffer or file-like object.

#### Signature

```python
class IO:
    def __init__(
        self,
        data: bytearray | bytes | None = None,
        idx: int = 0,
        littleEndian: bool = False,
        boolSize: int = 8,
        stringEncoding: str = "U",
    ):
        ...
```

### IO().__getitem__

[Show source in __init__.py:68](../../../binaryiotools/__init__.py#L68)

Get data at a specific idx.

#### Signature

```python
def __getitem__(self, idx: int):
    ...
```

### IO().__len__

[Show source in __init__.py:64](../../../binaryiotools/__init__.py#L64)

Length of data.

#### Signature

```python
def __len__(self) -> int:
    ...
```

### IO().addBytes

[Show source in __init__.py:658](../../../binaryiotools/__init__.py#L658)

Add some raw bytes and advance the index.

alias for setBytes()

#### Arguments

- `bytes` - can be a string, bytearray, or another IO object

#### Signature

```python
def addBytes(self, ioBytes: Any):
    ...
```

### IO().beginContext

[Show source in __init__.py:94](../../../binaryiotools/__init__.py#L94)

Start a new context where the index can be changed all you want...

and when endContext() is called, it will be restored to the current position

#### Signature

```python
def beginContext(self, newIndex: int):
    ...
```

### IO().bool16

[Show source in __init__.py:172](../../../binaryiotools/__init__.py#L172)

Get bool16.

#### Signature

```python
@property
def bool16(self) -> bool:
    ...
```

### IO().bool16

[Show source in __init__.py:177](../../../binaryiotools/__init__.py#L177)

Set bool16.

#### Signature

```python
@bool16.setter
def bool16(self, ioBool: bool):
    ...
```

### IO().bool32

[Show source in __init__.py:182](../../../binaryiotools/__init__.py#L182)

Get bool32.

#### Signature

```python
@property
def bool32(self) -> bool:
    ...
```

### IO().bool32

[Show source in __init__.py:187](../../../binaryiotools/__init__.py#L187)

Set bool32.

#### Signature

```python
@bool32.setter
def bool32(self, ioBool: bool):
    ...
```

### IO().bool64

[Show source in __init__.py:192](../../../binaryiotools/__init__.py#L192)

Get bool64.

#### Signature

```python
@property
def bool64(self) -> bool:
    ...
```

### IO().bool64

[Show source in __init__.py:197](../../../binaryiotools/__init__.py#L197)

Set bool64.

#### Signature

```python
@bool64.setter
def bool64(self, ioBool: bool):
    ...
```

### IO().bool8

[Show source in __init__.py:162](../../../binaryiotools/__init__.py#L162)

Get bool8.

#### Signature

```python
@property
def bool8(self) -> bool:
    ...
```

### IO().bool8

[Show source in __init__.py:167](../../../binaryiotools/__init__.py#L167)

Set a bool8.

#### Signature

```python
@bool8.setter
def bool8(self, ioBool: bool):
    ...
```

### IO().boolean

[Show source in __init__.py:135](../../../binaryiotools/__init__.py#L135)

Return bool.

#### Signature

```python
@property
def boolean(self) -> bool:
    ...
```

### IO().boolean

[Show source in __init__.py:148](../../../binaryiotools/__init__.py#L148)

Set bool.

#### Signature

```python
@boolean.setter
def boolean(self, ioBool: bool):
    ...
```

### IO().byte

[Show source in __init__.py:202](../../../binaryiotools/__init__.py#L202)

Get byte.

#### Signature

```python
@property
def byte(self) -> Any:
    ...
```

### IO().byte

[Show source in __init__.py:207](../../../binaryiotools/__init__.py#L207)

Set byte.

#### Signature

```python
@byte.setter
def byte(self, byte: Any):
    ...
```

### IO().cString

[Show source in __init__.py:845](../../../binaryiotools/__init__.py#L845)

Read a sequence of chars until the next null byte.

#### Signature

```python
@property
def cString(self) -> str:
    ...
```

### IO().cString

[Show source in __init__.py:850](../../../binaryiotools/__init__.py#L850)

Set a sequence of chars and add a null byte.

#### Signature

```python
@cString.setter
def cString(self, text: str):
    ...
```

### IO().cStringA

[Show source in __init__.py:856](../../../binaryiotools/__init__.py#L856)

Read a sequence of chars until the next null byte in ascii.

#### Signature

```python
@property
def cStringA(self) -> str:
    ...
```

### IO().cStringA

[Show source in __init__.py:861](../../../binaryiotools/__init__.py#L861)

Set a sequence of chars and add a null byte in ascii.

#### Signature

```python
@cStringA.setter
def cStringA(self, text: str):
    ...
```

### IO().cStringU

[Show source in __init__.py:878](../../../binaryiotools/__init__.py#L878)

Read a sequence of chars until the next null byte in utf-8.

#### Signature

```python
@property
def cStringU(self) -> str:
    ...
```

### IO().cStringU

[Show source in __init__.py:883](../../../binaryiotools/__init__.py#L883)

Set a sequence of chars and add a null byte in utf-8.

#### Signature

```python
@cStringU.setter
def cStringU(self, text: str):
    ...
```

### IO().cStringW

[Show source in __init__.py:867](../../../binaryiotools/__init__.py#L867)

Read a sequence of chars until the next null byte in ucs-2.

#### Signature

```python
@property
def cStringW(self) -> str:
    ...
```

### IO().cStringW

[Show source in __init__.py:872](../../../binaryiotools/__init__.py#L872)

Set a sequence of chars and add a null byte in ucs-2.

#### Signature

```python
@cStringW.setter
def cStringW(self, text: str):
    ...
```

### IO().data

[Show source in __init__.py:72](../../../binaryiotools/__init__.py#L72)

Return data.

#### Signature

```python
@property
def data(self) -> bytearray:
    ...
```

### IO().data

[Show source in __init__.py:77](../../../binaryiotools/__init__.py#L77)

Set data.

#### Signature

```python
@data.setter
def data(self, data: bytearray) -> None:
    ...
```

### IO().double

[Show source in __init__.py:602](../../../binaryiotools/__init__.py#L602)

Get a double.

#### Signature

```python
@property
def double(self) -> float:
    ...
```

### IO().double

[Show source in __init__.py:607](../../../binaryiotools/__init__.py#L607)

Set a double.

#### Signature

```python
@double.setter
def double(self, floating: float):
    ...
```

### IO().dword

[Show source in __init__.py:242](../../../binaryiotools/__init__.py#L242)

Get a dword.

#### Signature

```python
@property
def dword(self) -> Any:
    ...
```

### IO().dword

[Show source in __init__.py:247](../../../binaryiotools/__init__.py#L247)

Set a dword.

#### Signature

```python
@dword.setter
def dword(self, dword: Any):
    ...
```

### IO().endContext

[Show source in __init__.py:101](../../../binaryiotools/__init__.py#L101)

Restore the index to the previous location where it was when	beginContext() was called.

#### Signature

```python
def endContext(self):
    ...
```

### IO().float32

[Show source in __init__.py:402](../../../binaryiotools/__init__.py#L402)

Get a float32.

#### Signature

```python
@property
def float32(self) -> float:
    ...
```

### IO().float32

[Show source in __init__.py:409](../../../binaryiotools/__init__.py#L409)

Set a float32.

#### Signature

```python
@float32.setter
def float32(self, float32: float):
    ...
```

### IO().float32be

[Show source in __init__.py:612](../../../binaryiotools/__init__.py#L612)

Read the next 32 bit float and advance the index.

#### Signature

```python
@property
def float32be(self) -> float:
    ...
```

### IO().float32be

[Show source in __init__.py:617](../../../binaryiotools/__init__.py#L617)

Set a 32 bit float.

#### Signature

```python
@float32be.setter
def float32be(self, float32be: float):
    ...
```

### IO().float32le

[Show source in __init__.py:622](../../../binaryiotools/__init__.py#L622)

Read the next 32 bit float and advance the index.

#### Signature

```python
@property
def float32le(self) -> float:
    ...
```

### IO().float32le

[Show source in __init__.py:627](../../../binaryiotools/__init__.py#L627)

Set a 32 bit float.

#### Signature

```python
@float32le.setter
def float32le(self, float32le: float):
    ...
```

### IO().float64

[Show source in __init__.py:417](../../../binaryiotools/__init__.py#L417)

Get a float64.

#### Signature

```python
@property
def float64(self) -> float:
    ...
```

### IO().float64

[Show source in __init__.py:424](../../../binaryiotools/__init__.py#L424)

Set a float64.

#### Signature

```python
@float64.setter
def float64(self, float64: float):
    ...
```

### IO().float64be

[Show source in __init__.py:632](../../../binaryiotools/__init__.py#L632)

Read the next 64 bit float and advance the index.

#### Signature

```python
@property
def float64be(self) -> float:
    ...
```

### IO().float64be

[Show source in __init__.py:637](../../../binaryiotools/__init__.py#L637)

Set a 64 bit float.

#### Signature

```python
@float64be.setter
def float64be(self, float64be: float):
    ...
```

### IO().float64le

[Show source in __init__.py:642](../../../binaryiotools/__init__.py#L642)

Read the next 64 bit float and advance the index.

#### Signature

```python
@property
def float64le(self) -> float:
    ...
```

### IO().float64le

[Show source in __init__.py:647](../../../binaryiotools/__init__.py#L647)

Set a 64 bit float.

#### Signature

```python
@float64le.setter
def float64le(self, float64le: float):
    ...
```

### IO().floating

[Show source in __init__.py:592](../../../binaryiotools/__init__.py#L592)

Get a float.

#### Signature

```python
@property
def floating(self) -> float:
    ...
```

### IO().floating

[Show source in __init__.py:597](../../../binaryiotools/__init__.py#L597)

Set a float.

#### Signature

```python
@floating.setter
def floating(self, floating: float):
    ...
```

### IO().getBytes

[Show source in __init__.py:652](../../../binaryiotools/__init__.py#L652)

Grab some raw bytes and advance the index.

#### Signature

```python
def getBytes(self, nbytes: int):
    ...
```

### IO().i16

[Show source in __init__.py:312](../../../binaryiotools/__init__.py#L312)

Get an int16.

#### Signature

```python
@property
def i16(self) -> int:
    ...
```

### IO().i16

[Show source in __init__.py:319](../../../binaryiotools/__init__.py#L319)

Set an int16.

#### Signature

```python
@i16.setter
def i16(self, i16: int):
    ...
```

### IO().i16be

[Show source in __init__.py:502](../../../binaryiotools/__init__.py#L502)

Read the next signed int16 and advance the index.

#### Signature

```python
@property
def i16be(self) -> int:
    ...
```

### IO().i16be

[Show source in __init__.py:507](../../../binaryiotools/__init__.py#L507)

Set the int16.

#### Signature

```python
@i16be.setter
def i16be(self, i16be: int):
    ...
```

### IO().i16le

[Show source in __init__.py:492](../../../binaryiotools/__init__.py#L492)

Read the next signed int16 and advance the index.

#### Signature

```python
@property
def i16le(self) -> int:
    ...
```

### IO().i16le

[Show source in __init__.py:497](../../../binaryiotools/__init__.py#L497)

Set the int16.

#### Signature

```python
@i16le.setter
def i16le(self, i16le: int):
    ...
```

### IO().i32

[Show source in __init__.py:342](../../../binaryiotools/__init__.py#L342)

Get an int32.

#### Signature

```python
@property
def i32(self) -> int:
    ...
```

### IO().i32

[Show source in __init__.py:349](../../../binaryiotools/__init__.py#L349)

Set an int32.

#### Signature

```python
@i32.setter
def i32(self, i32: int):
    ...
```

### IO().i32be

[Show source in __init__.py:542](../../../binaryiotools/__init__.py#L542)

Read the next signed int32 and advance the index.

#### Signature

```python
@property
def i32be(self) -> int:
    ...
```

### IO().i32be

[Show source in __init__.py:547](../../../binaryiotools/__init__.py#L547)

Set the int32.

#### Signature

```python
@i32be.setter
def i32be(self, i32be: int):
    ...
```

### IO().i32le

[Show source in __init__.py:532](../../../binaryiotools/__init__.py#L532)

Read the next signed int32 and advance the index.

#### Signature

```python
@property
def i32le(self) -> int:
    ...
```

### IO().i32le

[Show source in __init__.py:537](../../../binaryiotools/__init__.py#L537)

Set the int32.

#### Signature

```python
@i32le.setter
def i32le(self, i32le: int):
    ...
```

### IO().i64

[Show source in __init__.py:372](../../../binaryiotools/__init__.py#L372)

Get an int64.

#### Signature

```python
@property
def i64(self) -> int:
    ...
```

### IO().i64

[Show source in __init__.py:379](../../../binaryiotools/__init__.py#L379)

Set an int64.

#### Signature

```python
@i64.setter
def i64(self, i64: int):
    ...
```

### IO().i64be

[Show source in __init__.py:582](../../../binaryiotools/__init__.py#L582)

Read the next signed int64 and advance the index.

#### Signature

```python
@property
def i64be(self) -> int:
    ...
```

### IO().i64be

[Show source in __init__.py:587](../../../binaryiotools/__init__.py#L587)

Set the int64.

#### Signature

```python
@i64be.setter
def i64be(self, i64be: int):
    ...
```

### IO().i64le

[Show source in __init__.py:572](../../../binaryiotools/__init__.py#L572)

Read the next signed int64 and advance the index.

#### Signature

```python
@property
def i64le(self) -> int:
    ...
```

### IO().i64le

[Show source in __init__.py:577](../../../binaryiotools/__init__.py#L577)

Set the int64.

#### Signature

```python
@i64le.setter
def i64le(self, i64le: int):
    ...
```

### IO().i8

[Show source in __init__.py:282](../../../binaryiotools/__init__.py#L282)

Get an int8.

#### Signature

```python
@property
def i8(self) -> int:
    ...
```

### IO().i8

[Show source in __init__.py:289](../../../binaryiotools/__init__.py#L289)

Set an int8.

#### Signature

```python
@i8.setter
def i8(self, i8: int):
    ...
```

### IO().i8be

[Show source in __init__.py:462](../../../binaryiotools/__init__.py#L462)

Read the next signed int8 and advance the index.

#### Signature

```python
@property
def i8be(self) -> int:
    ...
```

### IO().i8be

[Show source in __init__.py:467](../../../binaryiotools/__init__.py#L467)

Set the int8.

#### Signature

```python
@i8be.setter
def i8be(self, i8be: int):
    ...
```

### IO().i8le

[Show source in __init__.py:452](../../../binaryiotools/__init__.py#L452)

Read the next signed int8 and advance the index.

#### Signature

```python
@property
def i8le(self) -> int:
    ...
```

### IO().i8le

[Show source in __init__.py:457](../../../binaryiotools/__init__.py#L457)

Set the int8.

#### Signature

```python
@i8le.setter
def i8le(self, i8le: int):
    ...
```

### IO().index

[Show source in __init__.py:84](../../../binaryiotools/__init__.py#L84)

Return data.

#### Signature

```python
@property
def index(self) -> int:
    ...
```

### IO().index

[Show source in __init__.py:89](../../../binaryiotools/__init__.py#L89)

Set index.

#### Signature

```python
@index.setter
def index(self, index: int) -> None:
    ...
```

### IO().qword

[Show source in __init__.py:262](../../../binaryiotools/__init__.py#L262)

Get a qword.

#### Signature

```python
@property
def qword(self) -> Any:
    ...
```

### IO().qword

[Show source in __init__.py:267](../../../binaryiotools/__init__.py#L267)

Set a qword.

#### Signature

```python
@qword.setter
def qword(self, qword: Any):
    ...
```

### IO().setBytes

[Show source in __init__.py:667](../../../binaryiotools/__init__.py#L667)

Add some raw bytes and advance the index.

alias for addBytes()

#### Arguments

- `ioBytes` - can be a string, bytearray, or another IO object

#### Signature

```python
def setBytes(self, ioBytes: Any):
    ...
```

### IO().sz754

[Show source in __init__.py:717](../../../binaryiotools/__init__.py#L717)

sz754.

#### Signature

```python
@property
def sz754(self) -> Any:
    ...
```

### IO().sz754

[Show source in __init__.py:722](../../../binaryiotools/__init__.py#L722)

Set sz754.

#### Signature

```python
@sz754.setter
def sz754(self, sz754: Any):
    ...
```

### IO().sz754A

[Show source in __init__.py:727](../../../binaryiotools/__init__.py#L727)

sz754A.

#### Signature

```python
@property
def sz754A(self) -> Any:
    ...
```

### IO().sz754A

[Show source in __init__.py:732](../../../binaryiotools/__init__.py#L732)

Set sz754A.

#### Signature

```python
@sz754A.setter
def sz754A(self, sz754: Any):
    ...
```

### IO().sz754U

[Show source in __init__.py:747](../../../binaryiotools/__init__.py#L747)

sz754U.

#### Signature

```python
@property
def sz754U(self) -> Any:
    ...
```

### IO().sz754U

[Show source in __init__.py:752](../../../binaryiotools/__init__.py#L752)

Set sz754U.

#### Signature

```python
@sz754U.setter
def sz754U(self, sz754: Any):
    ...
```

### IO().sz754W

[Show source in __init__.py:737](../../../binaryiotools/__init__.py#L737)

sz754W.

#### Signature

```python
@property
def sz754W(self) -> Any:
    ...
```

### IO().sz754W

[Show source in __init__.py:742](../../../binaryiotools/__init__.py#L742)

Set sz754W.

#### Signature

```python
@sz754W.setter
def sz754W(self, sz754: Any):
    ...
```

### IO().textLine

[Show source in __init__.py:785](../../../binaryiotools/__init__.py#L785)

Read a sequence of chars until the next new line char.

#### Signature

```python
@property
def textLine(self) -> str:
    ...
```

### IO().textLine

[Show source in __init__.py:793](../../../binaryiotools/__init__.py#L793)

Set a sequence of chars until the next new line char.

#### Signature

```python
@textLine.setter
def textLine(self, text: str):
    ...
```

### IO().textLineA

[Show source in __init__.py:800](../../../binaryiotools/__init__.py#L800)

Read a sequence of chars until the next new line char in ascii.

#### Signature

```python
@property
def textLineA(self) -> str:
    ...
```

### IO().textLineA

[Show source in __init__.py:808](../../../binaryiotools/__init__.py#L808)

Set a sequence of chars until the next new line char in ascii.

#### Signature

```python
@textLineA.setter
def textLineA(self, text: str):
    ...
```

### IO().textLineU

[Show source in __init__.py:830](../../../binaryiotools/__init__.py#L830)

Read a sequence of chars until the next new line char in utf-8.

#### Signature

```python
@property
def textLineU(self) -> str:
    ...
```

### IO().textLineU

[Show source in __init__.py:838](../../../binaryiotools/__init__.py#L838)

Set a sequence of chars until the next new line char in utf-8.

#### Signature

```python
@textLineU.setter
def textLineU(self, text: str):
    ...
```

### IO().textLineW

[Show source in __init__.py:815](../../../binaryiotools/__init__.py#L815)

Read a sequence of chars until the next new line char in ucs-2.

#### Signature

```python
@property
def textLineW(self) -> str:
    ...
```

### IO().textLineW

[Show source in __init__.py:823](../../../binaryiotools/__init__.py#L823)

Set a sequence of chars until the next new line char in ucs-2.

#### Signature

```python
@textLineW.setter
def textLineW(self, text: str):
    ...
```

### IO().u16

[Show source in __init__.py:327](../../../binaryiotools/__init__.py#L327)

Get an uint16.

#### Signature

```python
@property
def u16(self) -> int:
    ...
```

### IO().u16

[Show source in __init__.py:334](../../../binaryiotools/__init__.py#L334)

Set an unint16.

#### Signature

```python
@u16.setter
def u16(self, u16: int):
    ...
```

### IO().u16be

[Show source in __init__.py:472](../../../binaryiotools/__init__.py#L472)

Read the next uint16 and advance the index.

#### Signature

```python
@property
def u16be(self) -> int:
    ...
```

### IO().u16be

[Show source in __init__.py:477](../../../binaryiotools/__init__.py#L477)

Set the uint16.

#### Signature

```python
@u16be.setter
def u16be(self, u16be: int):
    ...
```

### IO().u16le

[Show source in __init__.py:482](../../../binaryiotools/__init__.py#L482)

Read the next uint16 and advance the index.

#### Signature

```python
@property
def u16le(self) -> int:
    ...
```

### IO().u16le

[Show source in __init__.py:487](../../../binaryiotools/__init__.py#L487)

Set the uint16.

#### Signature

```python
@u16le.setter
def u16le(self, u16le: int):
    ...
```

### IO().u32

[Show source in __init__.py:357](../../../binaryiotools/__init__.py#L357)

Get a uint32.

#### Signature

```python
@property
def u32(self) -> int:
    ...
```

### IO().u32

[Show source in __init__.py:364](../../../binaryiotools/__init__.py#L364)

Set a unint32.

#### Signature

```python
@u32.setter
def u32(self, u32: int):
    ...
```

### IO().u32be

[Show source in __init__.py:512](../../../binaryiotools/__init__.py#L512)

Read the next uint32 and advance the index.

#### Signature

```python
@property
def u32be(self) -> int:
    ...
```

### IO().u32be

[Show source in __init__.py:517](../../../binaryiotools/__init__.py#L517)

Set the uint32.

#### Signature

```python
@u32be.setter
def u32be(self, u32be: int):
    ...
```

### IO().u32le

[Show source in __init__.py:522](../../../binaryiotools/__init__.py#L522)

Read the next uint32 and advance the index.

#### Signature

```python
@property
def u32le(self) -> int:
    ...
```

### IO().u32le

[Show source in __init__.py:527](../../../binaryiotools/__init__.py#L527)

Set the uint32.

#### Signature

```python
@u32le.setter
def u32le(self, u32le: int):
    ...
```

### IO().u64

[Show source in __init__.py:387](../../../binaryiotools/__init__.py#L387)

Get a uint64.

#### Signature

```python
@property
def u64(self) -> int:
    ...
```

### IO().u64

[Show source in __init__.py:394](../../../binaryiotools/__init__.py#L394)

Set a uint64.

#### Signature

```python
@u64.setter
def u64(self, u64: int):
    ...
```

### IO().u64be

[Show source in __init__.py:552](../../../binaryiotools/__init__.py#L552)

Read the next uint64 and advance the index.

#### Signature

```python
@property
def u64be(self) -> int:
    ...
```

### IO().u64be

[Show source in __init__.py:557](../../../binaryiotools/__init__.py#L557)

Set the uint64.

#### Signature

```python
@u64be.setter
def u64be(self, u64be: int):
    ...
```

### IO().u64le

[Show source in __init__.py:562](../../../binaryiotools/__init__.py#L562)

Read the next uint64 and advance the index.

#### Signature

```python
@property
def u64le(self) -> int:
    ...
```

### IO().u64le

[Show source in __init__.py:567](../../../binaryiotools/__init__.py#L567)

Set the uint64.

#### Signature

```python
@u64le.setter
def u64le(self, u64le: int):
    ...
```

### IO().u8

[Show source in __init__.py:297](../../../binaryiotools/__init__.py#L297)

Get an unsigned int.

#### Signature

```python
@property
def u8(self) -> int:
    ...
```

### IO().u8

[Show source in __init__.py:304](../../../binaryiotools/__init__.py#L304)

Set an unsigned int.

#### Signature

```python
@u8.setter
def u8(self, u8: int):
    ...
```

### IO().u8be

[Show source in __init__.py:432](../../../binaryiotools/__init__.py#L432)

Read the next uint8 and advance the index.

#### Signature

```python
@property
def u8be(self) -> int:
    ...
```

### IO().u8be

[Show source in __init__.py:437](../../../binaryiotools/__init__.py#L437)

Set the uint8.

#### Signature

```python
@u8be.setter
def u8be(self, u8be: int):
    ...
```

### IO().u8le

[Show source in __init__.py:442](../../../binaryiotools/__init__.py#L442)

Read the next uint8 and advance the index.

#### Signature

```python
@property
def u8le(self) -> int:
    ...
```

### IO().u8le

[Show source in __init__.py:447](../../../binaryiotools/__init__.py#L447)

Set the uint8.

#### Signature

```python
@u8le.setter
def u8le(self, u8le: int):
    ...
```

### IO().unsignedByte

[Show source in __init__.py:212](../../../binaryiotools/__init__.py#L212)

Get unsigned byte.

#### Signature

```python
@property
def unsignedByte(self) -> Any:
    ...
```

### IO().unsignedByte

[Show source in __init__.py:217](../../../binaryiotools/__init__.py#L217)

Set unsigned byte.

#### Signature

```python
@unsignedByte.setter
def unsignedByte(self, byte: Any):
    ...
```

### IO().unsignedDword

[Show source in __init__.py:252](../../../binaryiotools/__init__.py#L252)

Get a unsigned dword.

#### Signature

```python
@property
def unsignedDword(self) -> Any:
    ...
```

### IO().unsignedDword

[Show source in __init__.py:257](../../../binaryiotools/__init__.py#L257)

Set an unsigned dword.

#### Signature

```python
@unsignedDword.setter
def unsignedDword(self, unsignedDword: Any):
    ...
```

### IO().unsignedQword

[Show source in __init__.py:272](../../../binaryiotools/__init__.py#L272)

Get an unsigned qword.

#### Signature

```python
@property
def unsignedQword(self) -> Any:
    ...
```

### IO().unsignedQword

[Show source in __init__.py:277](../../../binaryiotools/__init__.py#L277)

Set an unsigned qword.

#### Signature

```python
@unsignedQword.setter
def unsignedQword(self, unsignedQword: Any):
    ...
```

### IO().unsignedWord

[Show source in __init__.py:232](../../../binaryiotools/__init__.py#L232)

Get an unsigned word.

#### Signature

```python
@property
def unsignedWord(self) -> Any:
    ...
```

### IO().unsignedWord

[Show source in __init__.py:237](../../../binaryiotools/__init__.py#L237)

Set an unsigned word.

#### Signature

```python
@unsignedWord.setter
def unsignedWord(self, unsignedWord: Any):
    ...
```

### IO().word

[Show source in __init__.py:222](../../../binaryiotools/__init__.py#L222)

Get a word.

#### Signature

```python
@property
def word(self) -> Any:
    ...
```

### IO().word

[Show source in __init__.py:227](../../../binaryiotools/__init__.py#L227)

Set a word.

#### Signature

```python
@word.setter
def word(self, word: Any):
    ...
```


