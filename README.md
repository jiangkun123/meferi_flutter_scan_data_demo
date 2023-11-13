#mefei_scan_data
- - -
This plug-in is used to receive decoding results from Meferi's handheld terminal devices.

##example
```
MeferiScanData.startListening();
    MeferiScanData.onEventReceived.listen((Map<String, String> data) {
      setState(() {
        _barcode = data['data']!;
      });
    });
```

```
  @override
  void dispose() {
    MeferiScanData.stopListening();
    super.dispose();
  }
```