# Resty Struct
[中文说明](./README-zh.md)

convert between binary and lua, based on luajit.

just use like [struct][1] class of Python.

this module is still on developing and do not use it now.

example:

```lua
local struct = require 'resty.struct'

local binary, err = struct.pack('HHL', 1, 2, 3)

if not binary then print(err) end

local table, count = struct.unpack('HHL', binary)

if table then
    for i = 1, count do
        print(table[i])
    end
else
    print(count) -- error message instead
end

```

  [1]: https://docs.python.org/2/library/struct.html