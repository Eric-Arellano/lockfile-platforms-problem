python_requirement_library(name="ansicolors", requirements=["ansicolors"])

# This is valid because ansicolors has a bdist.
pex_binary(
    dependencies=[":ansicolors"],
    platforms=["linux-x86_64-cp-37-m", "macosx-10.14-x86_64-cp-37-m"],
)
