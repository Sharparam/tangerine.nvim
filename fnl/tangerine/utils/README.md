# diff.fnl
> Contains diffing algorithm used by compiler.

Works by creating marker that looks like `-- :fennel:<UTC>`,
compares UTC in marker to ftime(source).

**EXPORTS**
```fennel
:diff {
	:create-marker (function 1)
	:read-marker   (function 2)
	:stale?        (function 3)
}
```

# env.fnl
> Stores environment used by rest of tangerine

Provides getter and setter so that multiple modules can have shared configurations.

**EXPORTS**
```fennel
:env {
	:conf (function 1)
	:get  (function 2)
	:set  (function 3)
}
```

# fs.fnl
> Basic utils around file system handlers.

**EXPORTS**
```fennel
:fs {
	:read      (function 1)
	:readable? (function 2)
	:remove    (function 3)
	:write     (function 4)
}
```

# path.fnl
> Provides path manipulation and indexing functions

**DEPENDS:**
```
utils[env]
```

**EXPORTS**
```fennel
:path {
	:goto-output    (function 1)
	:gsub           (function 2)
	:match          (function 3)
	:resolve        (function 4)
	:shortname      (function 5)
	:source         (function 6)
	:target         (function 7)
	:transform-path (function 8)
	:wildcard       (function 9)
}
```

# srlize.fnl
> Serializes lua data structures into fennel syntax.

**EXPORTS**
```fennel
:srlize (function 1)
```

# window.fnl
> Contains functions to create and control floating windows.

**DEPENDS:**
```
utils[env]
```

**EXPORTS**
```fennel
:window {
	:close        (function 1)
	:create-float (function 2)
	:killall      (function 3)
	:next         (function 4)
	:prev         (function 5)
	:resize       (function 6)
	:set-float    (function 7)
	:__stack {
		:total 0
	}
}
```

