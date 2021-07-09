# This demonstrates Stu's proposal of doing a distinct resolve for each platform, meaning that we find all
# pex_binary's that use that platform and create a single lockfile/resolve for that platform, then each pex_binary
# subsets from that as it normally would.
#
# It's not yet clear what should happen when platforms are left off. As demonstrated in two_pex__*, we'll have issues
# if unconstrainted PEXes get mixed into platform-specific resolves. It feels like we will want to treat no platforms
# like a platform, e.g. `lock_no-platform.txt`. Or, don't use platform-specific resolves and load the lockfiles
# via constraints files and only use `resolve_all_constraints` when platforms not in use (status quo).

python_requirement_library(name="ansicolors", requirements=["ansicolors"])
python_requirement_library(name="mac-utils", requirements=["mac-utils"])
python_requirement_library(name="linux-utils", requirements=["linux-utils"])

pex_binary(
    name="macos-specific",
    dependencies=[":mac-utils"],
    platforms=["macosx-10.14-x86_64-cp-37-m"],
)

pex_binary(
    name="linux-specific",
    dependencies=[":linux-utils"],
    platforms=["linux-x86_64-cp-37-m"],
)

pex_binary(
    name="multiplatform",
    dependencies=[":ansicolors"],
    platforms=["linux-x86_64-cp-37-m", "macosx-10.14-x86_64-cp-37-m"],
)
