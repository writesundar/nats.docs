# subscribe

/ [config](/ref/config/index.md) / [leafnodes](/ref/config/config/leafnodes/index.md) / [authorization](/ref/config/config/leafnodes/authorization/index.md) / [default_permissions](/ref/config/config/leafnodes/authorization/default_permissions/index.md)

A single subject, list of subjects, or a allow-deny map of
subjects for subscribing. Note, that the subject permission can
have an optional second value declaring a queue name.

_Aliases_

- `sub`

## Examples

Allow subscribe on `foo`

```
foo
```

Allow subscribe on `foo` in group matching `*.dev`

```
foo *.dev
```

Allow subscribe on `foo.>` and `bar` in group `v1`

```
[foo.>, "bar v1"]
```

Allow subscribe to `foo.*` except `foo.bar`

```
{
  allow: "foo.*"
  deny: "foo.bar"
}
```