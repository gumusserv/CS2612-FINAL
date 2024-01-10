```
DECLARATION
  Object:
    ARRAY(a[CONST(3)])
  Init List:
    None

ASGN
  Left:
    ARRAY
      Object:
        VAR(a)
      Index:
        CONST(2)
    
  Right:
    PLUS
      Left:
        ARRAY
          Object:
            VAR(a)
          Index:
            CONST(0)
        
      Right:
        ARRAY
          Object:
            VAR(a)
          Index:
            CONST(3)



DECLARATION
  Object:
    PTR(a, level: 1)
  Init Expr:
    None

ASGN
  Left:
    DEREF
      VAR(a)

  Right:
    PLUS
      Left:
        DEREF
          PLUS
            Left:
              VAR(a)
            Right:
              CONST(4)


      Right:
        DEREF
          PLUS
            Left:
              VAR(a)
            Right:
              CONST(8)




DECLARATION
  Object:
    ARRAY(a[CONST(1)][CONST(2)])
  Init List:
    None

DECLARATION
  Object:
    ARRAY(a[CONST(3)][CONST(2)][CONST(2)])
  Init List:
    None

ASGN
  Left:
    ARRAY
      Object:
        ARRAY
          Object:
            VAR(a)
          Index:
            CONST(2)

      Index:
        CONST(3)

  Right:
    CONST(1)

ASGN
  Left:
    ARRAY
      Object:
        ARRAY
          Object:
            VAR(a)
          Index:
            CONST(0)

      Index:
        CONST(1)

  Right:
    MUL
      Left:
        ARRAY
          Object:
            ARRAY
              Object:
                VAR(a)
              Index:
                CONST(0)

          Index:
            CONST(2)

      Right:
        ARRAY
          Object:
            ARRAY
              Object:
                VAR(a)
              Index:
                CONST(3)

          Index:
            CONST(0)



DECLARATION
  Object:
    PTR(abc, level: 3)
  Init Expr:
    None

ASGN
  Left:
    DEREF
      VAR(a)

  Right:
    MUL
      Left:
        DEREF
          PLUS
            Left:
              VAR(a)
            Right:
              CONST(4)


      Right:
        DEREF
          DEREF
            DEREF
              DEREF
                DEREF
                  DEREF
                    DEREF
                      PLUS
                        Left:
                          VAR(a)
                        Right:
                          CONST(8)
```

```
DECLARATION
  Object:
    VAR(a)
  Init Expr:
    CONST(3)

DECLARATION
  Object:
    VAR(b)
  Init Expr:
    VAR(a)

DECLARATION
  Object:
    VAR(c)
  Init Expr:
    PLUS
      Left:
        CONST(3)
      Right:
        CONST(4)


DECLARATION
  Object:
    VAR(d)
  Init Expr:
    MUL
      Left:
        VAR(b)
      Right:
        VAR(c)


DECLARATION
  Object:
    VAR(e)
  Init Expr:
    ARRAY
      Object:
        VAR(a)
      Index:
        CONST(2)


DECLARATION
  Object:
    VAR(hello)
  Init Expr:
    ARRAY
      Object:
        ARRAY
          Object:
            VAR(world)
          Index:
            CONST(2)

      Index:
        CONST(3)


DECLARATION
  Object:
    VAR(f)
  Init Expr:
    DEREF
      PLUS
        Left:
          VAR(a)
        Right:
          CONST(4)



DECLARATION
  Object:
    ARRAY(a[CONST(3)])
  Init List:
    CONST(2)
    CONST(3)
    CONST(4)


DECLARATION
  Object:
    ARRAY(mul[CONST(2)][CONST(2)])
  Init List:
    INIT_LIST
      CONST(1)
      CONST(2)

    INIT_LIST
      CONST(3)
      CONST(4)



PTR_DECL(a, level: 1)
  Size Expr:
    MALLOC
      VAR(n)
```

```
CHAR_DECL(a)
CHAR_DECL(a)
  Init Char:
    CHAR('s')
STRING_DECL(a)
ASGN
  Left:
    ARRAY
      Object:
        VAR(a)
      Index:
        CONST(1)

  Right:
    CHAR('s')

STRING_DECL(a)
  Init String:
    CHAR_LIST
      CHAR('a')
      CHAR('b')
      CHAR('c')

STRING_DECL(a)
  Init String:
    STRING("hello")
STRING_DECL(a)
  Init String:
    STRING("world")
DECLARATION
  Object:
    VAR(a)
  Init Expr:
    None
  Object:
    VAR(b)
  Init Expr:
    None
  Object:
    VAR(c)
  Init Expr:
    None

DECLARATION
  Object:
    VAR(a)
  Init Expr:
    None
  Object:
    ARRAY(b[CONST(2)])
  Init List:
    None
  Object:
    PTR(c, level: 1)
  Init Expr:
    None

DECLARATION
  Object:
    PTR(a, level: 1)
  Init Expr:
    None
  Object:
    PTR(b, level: 2)
  Init Expr:
    None
  Object:
    PTR(c, level: 3)
  Init Expr:
    None

DECLARATION
  Object:
    VAR(a)
  Init Expr:
    CONST(1)
  Object:
    ARRAY(b[CONST(3)])
  Init List:
    CONST(2)
    CONST(3)

  Object:
    ARRAY(c[CONST(2)][CONST(3)])
  Init List:
    INIT_LIST
      CONST(1)
      CONST(2)
      CONST(3)

    INIT_LIST
      CONST(4)
      CONST(5)
      CONST(6)
```


