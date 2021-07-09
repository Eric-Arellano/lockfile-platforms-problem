python_requirement_library(name="ansicolors", requirements=["ansicolors"])
python_requirement_library(name="future", requirements=["future"])

# This works iff the lockfile is used for constraints, rather than first resolving it all a la
# `[python-setup].resolve_all_constraints`.
pex_binary(
    name="multiplatform",
    dependencies=[":ansicolors"],
    platforms=["linux-x86_64-cp-37-m", "macosx-10.14-x86_64-cp-37-m"],
)

# This always works because there are no foreign platforms.
pex_binary(
    name="current_platform",
    dependencies=[":ansicolors", ":future"],
)
