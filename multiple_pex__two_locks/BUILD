python_requirement_library(name="ansicolors", requirements=["ansicolors"])
python_requirement_library(name="future", requirements=["future"])

pex_binary(
    name="multiplatform",
    dependencies=[":ansicolors"],
    platforms=["linux-x86_64-cp-37-m", "macosx-10.14-x86_64-cp-37-m"],
    lockfile="./lock_multiplatform.txt",
)

pex_binary(
    name="current_platform",
    dependencies=[":ansicolors", ":future"],
    lockfile="./lock_current_platform.txt",
)
