# Installing packages from the gtp

The purpose of inflator is to let you create and install packages. The latter is easier so let's do that first.

The command for installing packages is  `inflate install`

We are going to install a package (called a gobo) from the 
[gtp](https://github.com/inflated-goboscript/gtp/ "goboscript table of packages")

Let's install [cmath](https://github.com/inflated-goboscript/cmath "Gobo for complex number calculations") and use that.

??? Warning 

    There are [a few issues with some niche functions in cmath](https://github.com/inflated-goboscript/cmath/issues/2)

## Installing cmath

Inflator has a similar syntax to pip, so you just do `inflate install cmath`

If everything goes well, you should find it say `Installed cmath v1.0.1 by FAReTek1 into <appdata directory>`.
It should also have installed `math`, which is a dependency of `cmath`.

Now that you have installed cmath, you now have to add it as a dependency in `inflator.toml`. Like so:

```toml
# inflator.toml syntax documentation: https://github.com/inflated-goboscript/inflator#inflator
name = "tutorial"
version = "v0.0.0"
username = "if this is left blank then -9999 aura 💀" # (1)

[dependencies]
cmath = "cmath"
```

1. You can change this to your username if it bothers you.

Now, run `inflate`. This will sync the packages and place them in the `inflator/` directory.

We can now `%include` cmath.

[//]: # (One day we might add a goboscript syntax highlighter, but not right now)
```gs
%include inflator/math  # (1)
%include inflator/cmath


costumes "blank.svg";

onflag {
    say "Hello, World!";
}
```

!!! Note

    If you ever want to update a package you are using, you can use `inflate install -U <pkg>` to upgrade it.

Let's use some complex math now:

```gs
%include inflator/math
%include inflator/cmath


costumes "blank.svg";

onflag {
    Complex i = Complex(0, 1);

    Complex result = c_pow(i, i);

    say c_str(result);
}
```

This program demonstrates the result of doing `i` ** `i`. You may notice that the result is actually entirely real!
