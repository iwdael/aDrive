/file/list
请求体 FileListRequest
```Java
data class FileListRequest(
    var drive_id: String? = null,
    var marker: String? = null,
    var parent_file_id: String? = null
)
```
响应体 FileListResponse
```Java
data class FileListResponse(
    var items: List<FileItem> = emptyList(),
    var next_marker: String? = null
)
```
```Java
data class FileItem(
    var drive_id: String,
    var file_id: String,
    var name: String,
    var updated_at: String,
    var parent_file_id: String,
    var content_hash: String?,
    var type: String?,
    var url: String?,
    var size: Long?
)
```

/file/getDownloadUrl
请求体DownloadUrlRequest
```Java
data class DownloadUrlRequest(
    var drive_id: String? = null,
    var file_id: String? = null
)
```
响应体DownloadUrlResponse
```Java
data class DownloadUrlResponse(
    val url: String? = null,
    val size: Long? = null
)
```

/file/download?url=xxx&size=xxx