# UserBridge
A user-mode bridge based on [Npcap](https://github.com/nmap/npcap)/[WinPcap](https://www.winpcap.org)

# Build

1. Get [WinPcap 4.1.2 Developer's Pack](https://www.winpcap.org/devel.htm)
2. Build ``UserBridge.sln`` with **Visual Studio 2013**

# Usage
Launch the executable ``UserBridge.exe``, you will see a list of adapters like:
```
1. Network adapter 'Microsoft' on local host
2. Network adapter 'Intel(R) 82574L Gigabit Network Connection' on local host
3. Network adapter 'MS NDIS 6.0 LoopBack Driver' on local host

Specify filter (hit return for no filter):
```

Press ``Enter``.

```
Enter the number of the first interface to use (1-3):
```

Type in the index of the first adapter and press ``Enter``.

```
Enter the number of the second interface to use (1-3):
```

Type in the index of the second adapter and press ``Enter``.

```
Start bridging the two adapters...
```

If the bridging succeeds, you will see a lot of lines coming up in the prompt like:

```
>> Len: 142
>> Len: 94
>> Len: 142
>> Len: 142
>> Len: 94
<< Len: 142
<< Len: 142
<< Len: 142
<< Len: 94
<< Len: 142
<< Len: 142
<< Len: 142
<< Len: 142
<< Len: 142
```

All these lines show the traffic flow handled by the bridge. Line ``Len: 142`` means there's a packet with 142 bytes is handled.
