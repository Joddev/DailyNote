### format

- basic

  ```python
  '{0} {1}'.format('one','two') // 'one two'
  ```

- value conversion

  ```python
  '{0!r} {0!s}'.format(1, '234')
  ```

- aligning

  ```python
  '{:_<10}'.format('test') // 'test______'
  '{:^10}'.format('test') // '   test   '
  ```

- truncating

  ```python
  '{:.4}'.format('abcdefg') // 'abcd'
  ```

- naming

  ```python
  person = {'a':1, 'b':2}
  '{p[a]} {p[b]}'.format(p=person) // '1 2'
  '{a[0]} {a[3]}'.format(a=[1,2,3,4]) // '1 4'
  ```

##### References

- https://pyformat.info/

