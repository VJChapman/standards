## StandardResponse

<a id="standardresponse"></a>

```json
{
  "links": {
    "self": "http://example.com",
  },
  "meta": {
  }
}

```

### Properties

*allOf*

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|*anonymous*|[Links - Standard](#linksstandard)|false|none|none|

*and*

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|*anonymous*|object|false|none|none|
|» meta|Empty Object|true|none|none|


<a id="linksstandard"></a>
<h3 id="tocSlinks">Links - Standard</h3>


```json
{
  "self": "http://example.com",
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|self|string(uri)|true|none|Fully qualified link  to this  API  call.|



## PaginatedResponse

<a id="paginatedresponse"></a>

```json
{
  "links": {
    "self": "http://example.com",
    "first": "http://example.com",
    "prev": "http://example.com",
    "next": "http://example.com",
    "last": "http://example.com"
  },
  "meta": {
    "totalRecords": 6,
    "totalPages": 2
  }
}

```

### Properties

*allOf*

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|*anonymous*|[Links - Paginated](#linkspaginated)|false|none|none|

*and*

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|*anonymous*|object|false|none|none|
|» meta|[Meta - Paginated](#metapaginated)|true|none|none|


<a id="linkspaginated"></a>
<h3 id="tocSlinks">Links - Paginated</h3>


```json
{
  "self": "http://example.com",
  "first": "http://example.com",
  "prev": "http://example.com",
  "next": "http://example.com",
  "last": "http://example.com"
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|self|string(uri)|true|none|Fully qualified link  to this  API  call.|
|first|string(uri)|false|none|URI to  the  first  page of this set. Mandatory  if this  response is  not  the  first  page.|
|prev|string(uri)|false|none|URI to  the  previous page of this set. Mandatory if this response is not the first page.|
|next|string(uri)|false|none|URI to the next page of this set. Mandatory if this response is not the last page.|
|last|string(uri)|false|none|URI to the last page of this set.  Mandatory if this response is not the last page.|


<a id="metapaginated"></a>
<h3 id="tocSmeta">Meta - Paginated</h3>


```json
{
  "totalRecords": 6,
  "totalPages": 2
}

```

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|totalRecords|integer(int32)|true|none|The total number of records in the  full set.|
|totalPages|integer(int32)|true|none|The total number of pages in the  full set.|


<a id="error"></a>
<h2 id="tocSerror">Error</h2>


```json
{
  "code": "string",
  "title": "string",
  "detail": "string",
  "meta": {
  }
}

```

*This is the standard representaton of an error.*

### Properties

|Name|Type|Required|Restrictions|Description|
|---|---|---|---|---|
|code|string|true|none|The code of the error|
|title|string|true|none|A displayable title of the error type|
|detail|string|true|none|Detail of the error|
|meta|object|false|none|Optional additional data for specific error types|
