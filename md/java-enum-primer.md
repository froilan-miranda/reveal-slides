### Enumeration Classes

```
public enum Size { SMALL, MEDIUM, LARGE, EXTRA_LARGE };
```

The type defined by this declaration is actually a class

You never need to use equals for values of enumerated types. Simply use == to compare them.
-

You can add constructors, methods, and fields to an enumerated type.

```
public enum Size 
{
	
	private String abbreviation;
}
```

-

All enumerated types are subclasses of the class Enum. They inherit a number of methods from that class.

``Size.SMALL.toString()``

conversly

``Size s = Enum.valueOf(Size.class, "SMALL");``

``Size.MEDIUM.ordinal()``
