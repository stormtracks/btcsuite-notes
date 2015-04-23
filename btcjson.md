
## Public methods broken down by file

#### cmdinfo.go

[func CmdMethod(cmd interface{}) (string, error)]
(http://godoc.org/github.com/btcsuite/btcd/btcjson/v2/btcjson#CmdMethod)

[func MethodUsageFlags(method string) (UsageFlag, error)]
(http://godoc.org/github.com/btcsuite/btcd/btcjson/v2/btcjson#MethodUsageFlags)

[func MethodUsageText(method string) (string, error)]
(http://godoc.org/github.com/btcsuite/btcd/btcjson/v2/btcjson#MethodUsageText)

#### cmdparse.go

[func MarshalCmd(id interface{}, cmd interface{}) ([]byte, error)]
(http://godoc.org/github.com/btcsuite/btcd/btcjson/v2/btcjson#MarshalCmd)

[func UnmarshalCmd(r *Request) (interface{}, error)]
(http://godoc.org/github.com/btcsuite/btcd/btcjson/v2/btcjson#UnmarshalCmd)

[func NewCmd(method string, args ...interface{}) (interface{}, error)]
(http://godoc.org/github.com/btcsuite/btcd/btcjson/v2/btcjson#NewCmd)

#### help.go

[func GenerateHelp(method string, descs map[string]string, resultTypes ...interface{}) (string, error)]
(http://godoc.org/github.com/btcsuite/btcd/btcjson/v2/btcjson#GenerateHelp)
