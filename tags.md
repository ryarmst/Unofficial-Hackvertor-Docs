# Tags Reference

Hackvertor includes ~200 built-in tags organized by category.

## Encode

| Tag | Description | Example |
|-----|-------------|---------|
| `base64` | Base64 encode | `<@base64>text</@base64>` |
| `base64url` | URL-safe Base64 | `<@base64url>text</@base64url>` |
| `base32` | Base32 encode | |
| `base58` | Base58 encode | |
| `urlencode` | URL encode | `<@urlencode>a=b&c=d</@urlencode>` |
| `urlencode_all` | URL encode all characters | |
| `burp_urlencode` | Burp-style URL encode | |
| `html_entities` | HTML entity encode | `<@html_entities><script></@html_entities>` |
| `html5_entities` | HTML5 named entities | |
| `hex` | Hex encode with separator | `<@hex(" ")>ABC</@hex>` → `41 42 43` |
| `hex_entities` | `&#xNN;` format | |
| `hex_escapes` | `\xNN` format | |
| `unicode_escapes` | `\uNNNN` format | |
| `css_escapes` | CSS escape format | |
| `octal_escapes` | `\NNN` format | |
| `dec_entities` | `&#NN;` decimal entities | |
| `jwt` | Create JWT token | `<@jwt("HS256","secret")>{"sub":"1234"}</@jwt>` |
| `quoted_printable` | Quoted-printable encode | |
| `saml` | SAML encode (deflate+base64) | |
| `powershell` | PowerShell encoded command | |
| `php_chr` | PHP chr() format | |
| `sql_hex` | SQL hex string `0x...` | |
| `utf7` | UTF-7 encode | |

## Decode

| Tag | Description |
|-----|-------------|
| `d_base64` | Decode Base64 |
| `d_base64url` | Decode URL-safe Base64 |
| `d_base32` | Decode Base32 |
| `d_base58` | Decode Base58 |
| `d_url` | URL decode |
| `d_burp_url` | Burp-style URL decode |
| `d_html_entities` | Decode HTML entities |
| `d_html5_entities` | Decode HTML5 entities |
| `d_js_string` | Decode JS escape sequences |
| `d_css_escapes` | Decode CSS escapes |
| `d_octal_escapes` | Decode octal escapes |
| `d_unicode_escapes` | Decode unicode escapes |
| `d_jwt_get_payload` | Extract JWT payload |
| `d_jwt_get_header` | Extract JWT header |
| `d_jwt_verify` | Verify JWT signature |
| `d_quoted_printable` | Decode quoted-printable |
| `d_saml` | Decode SAML |
| `d_utf7` | Decode UTF-7 |
| `auto_decode` | Auto-detect and decode |
| `auto_decode_no_decrypt` | Auto-decode without decryption |
| `json_parse` | Parse JSON and extract values |
## Hash

| Tag | Description |
|-----|-------------|
| `md5` | MD5 hash |
| `sha1` | SHA-1 hash |
| `sha256` | SHA-256 hash |
| `sha384` | SHA-384 hash |
| `sha512` | SHA-512 hash |
| `sha3`, `sha3_256`, etc. | SHA-3 variants |
| `md2`, `md4` | MD2/MD4 hashes |
| `ripemd128/160/256/320` | RIPEMD variants |
| `whirlpool` | Whirlpool hash |
| `tiger` | Tiger hash |
| `sm3` | SM3 hash |
| `gost3411` | GOST hash |
| `skein_*` | Skein hash variants |

## HMAC

| Tag | Example |
|-----|---------|
| `hmac_md5` | `<@hmac_md5("SECRET")>message</@hmac_md5>` |
| `hmac_sha1` | |
| `hmac_sha256` | |
| `hmac_sha384` | |
| `hmac_sha512` | |

## String

| Tag | Description | Example |
|-----|-------------|---------|
| `uppercase` | Convert to uppercase | |
| `lowercase` | Convert to lowercase | |
| `capitalise` | Capitalize first letter | |
| `reverse` | Reverse string | |
| `length` | Get string length | |
| `unique` | Remove duplicate chars | |
| `find` | Regex find | `<@find("\\d+")>abc123</@find>` → `123` |
| `replace` | String replace | `<@replace("old","new")>text</@replace>` |
| `regex_replace` | Regex replace | Supports capture groups `$1`, `$2` |
| `repeat` | Repeat string | `<@repeat(3)>ab</@repeat>` → `ababab` |
| `substring` | Extract substring | `<@substring(0,5)>hello world</@substring>` |
| `split_join` | Split and rejoin | |
| `from_charcode` | Char codes to string | |
| `to_charcode` | String to char codes | |
| `space` | Insert space (no input) | |
| `newline` | Insert newline (no input) | |
| `remove_output` | Suppress output | |

## Convert

| Tag | Description |
|-----|-------------|
| `dec2hex` | Decimal to hex |
| `hex2dec` | Hex to decimal |
| `dec2oct` | Decimal to octal |
| `oct2dec` | Octal to decimal |
| `dec2bin` | Decimal to binary |
| `bin2dec` | Binary to decimal |
| `ascii2hex` | ASCII to hex |
| `hex2ascii` | Hex to ASCII |
| `ascii2bin` | ASCII to binary |
| `bin2ascii` | Binary to ASCII |
| `chunked_dec2hex` | Chunked transfer encoding |
## Math

| Tag | Description | Example |
|-----|-------------|---------|
| `random` | Random from charset | `<@random(10)>abc123</@random>` |
| `random_alpha_lower` | Random lowercase letters | `<@random_alpha_lower(8)></@random_alpha_lower>` |
| `random_alphanum_mixed` | Random alphanumeric | |
| `random_num` | Random numbers | |
| `random_hex` | Random hex | |
| `random_unicode` | Random unicode chars | |
| `uuid` | Generate UUID | `<@uuid></@uuid>` |
| `range` | Generate number range | `<@range(1,10,1)></@range>` |
| `arithmetic` | Math operations | |
| `zeropad` | Zero-pad numbers | |
| `total` | Sum numbers | |

## Encrypt

| Tag | Description |
|-----|-------------|
| `aes_encrypt` | AES encryption |
| `xor` | XOR with key |
| `rotN` | ROT-N cipher (e.g., ROT13) |
| `affine_encrypt` | Affine cipher |
| `atbash_encrypt` | Atbash cipher |
| `rail_fence_encrypt` | Rail fence cipher |
| `substitution_encrypt` | Substitution cipher |
| `rotN_bruteforce` | Try all ROT values |
## Decrypt

| Tag | Description |
|-----|-------------|
| `aes_decrypt` | AES decryption |
| `xor_decrypt` | XOR decrypt (guess key) |
| `affine_decrypt` | Affine decrypt |
| `atbash_decrypt` | Atbash decrypt |
| `rail_fence_decrypt` | Rail fence decrypt |
| `substitution_decrypt` | Substitution decrypt |
## Compression

| Tag | Description |
|-----|-------------|
| `gzip` | Gzip compress |
| `d_gzip` | Gzip decompress |
| `bzip2` | Bzip2 compress |
| `d_bzip2` | Bzip2 decompress |
| `deflate` | Deflate compress |
| `d_deflate` | Deflate decompress |
| `d_brotli` | Brotli decompress |
## Variables

| Tag | Description |
|-----|-------------|
| `set` / `set_variable` | Store a value |
| `get` / `get_variable` | Retrieve a value |
| `increment_var` | Auto-increment variable |
| `decrement_var` | Auto-decrement variable |

See [Global Variables](global-variables.md) for details.

## Context Tags

Context tags access request data during conversion. They require the tag execution key.

| Tag | Description |
|-----|-------------|
| `context_request` | Full request text |
| `context_url` | Request URL or component |
| `context_header` | Get header value |
| `context_body` | Request body |
| `context_param` | Get parameter value |
| `context_cookie` | Get cookie value |
| `context_method` | HTTP method |
| `context_path` | Request path |
## Charsets

Tags for charset conversion (e.g., `UTF-8`, `ISO-8859-1`, `UTF-16`). The charset name is used as the tag name.

## Date

| Tag | Description |
|-----|-------------|
| `timestamp` | Current Unix timestamp |
| `timestamp_millis` | Timestamp in milliseconds |
| `date` | Formatted date string |

## Fake (Data Generation)

Generates fake data using JavaFaker:

`name`, `email`, `phone`, `address`, `company`, `creditcard`, `uuid`, and many more.

Example: `<@name></@name>` → `John Smith`

## XSS

XSS payload generators for testing:

`behavior`, `css_expression`, `datasrc`, `eval_fromcharcode`, `iframe_data_url`, `script_data`, `template_eval`, `throw_eval`, etc.

## Languages (Custom Code)

| Tag | Description |
|-----|-------------|
| `javascript` | Execute JavaScript |
| `python` | Execute Python (Jython) |
| `groovy` | Execute Groovy |
| `java` | Execute Java (BeanShell) |

See [Custom Tags](custom-tags.md) for creating code-based tags.

## System

| Tag | Description |
|-----|-------------|
| `system` | Execute system command |
| `read_file` | Read file contents |
| `read_url_burp` | Fetch URL through Burp |

**Note**: System tags require "Allow code execution tags" in settings.

