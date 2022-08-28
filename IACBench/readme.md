- ContentProvider1_src.apk
  - write imei to ContentProvider with name "content://com.cc.frice.provider/privacy"
  - insert key: src_content
  - ExitPoint is "insert(uri, values)"
- ContentProvider_sink.apk
  - query content from ContentProvider with name "content://com.cc.frice.provider/privacy"
  - query key: src_content
  - EntryPoint is query(uri,null,null,....)



- FileShare_src.apk

  - write imei to a file with name "leakdata.txt"
  - use permission : "android.permission.WRITE_EXTERNAL_STORAGE"

- FileShare_sink.apk

  - read content from file with name "leakdata.txt"
  - the content is imei, then log it
  - use permission : "android.permission.READ_EXTERNAL_STORAGE"
