python_requirement_library(name="future", requirements=["future"])

# This is invalid because future only has an sdist.
pex_binary(
    dependencies=[":future"],
    platforms=["linux-x86_64-cp-37-m", "macosx-10.14-x86_64-cp-37-m"],
)
