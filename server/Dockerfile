FROM itzg/minecraft-server:java17

# https://itzg.github.io/docker-minecraft-docs/java/versions/minecraft/
ENV VERSION=1.18.2

# https://itzg.github.io/docker-minecraft-docs/java/server-types/forge/
ENV TYPE="FORGE"
ENV EULA="true"

# https://itzg.github.io/docker-minecraft-docs/java/server-types/packwiz/
ENV PACKWIZ_URL="https://github.com/klaribot/CivFun-packwiz/blob/master/packwiz/pack.toml?raw=true"

# https://itzg.github.io/docker-minecraft-docs/java/configuration/icon/
ENV ICON="https://github.com/klaribot/CivFun-packwiz/blob/master/client/pack.png?raw=true"
ENV OVERRIDE_ICON="true"

# https://itzg.github.io/docker-minecraft-docs/java/configuration/forcegamemode/
ENV FORCE_GAMEMODE="true"

# https://itzg.github.io/docker-minecraft-docs/java/configuration/snooper/
ENV SNOOPER_ENABLED="false"

# https://github.com/etil2jz/etil-minecraft-flags
ENV JVM_OPTS="-Xms14G -Xmx14G -XX:+UseG1GC -XX:+ParallelRefProcEnabled -XX:MaxGCPauseMillis=200 -XX:+UnlockExperimentalVMOptions -XX:+UnlockDiagnosticVMOptions -XX:+DisableExplicitGC -XX:+AlwaysPreTouch -XX:G1NewSizePercent=40 -XX:G1MaxNewSizePercent=50 -XX:G1HeapRegionSize=16M -XX:G1ReservePercent=15 -XX:G1HeapWastePercent=5 -XX:G1MixedGCCountTarget=4 -XX:InitiatingHeapOccupancyPercent=20 -XX:G1MixedGCLiveThresholdPercent=90 -XX:G1RSetUpdatingPauseTimePercent=5 -XX:SurvivorRatio=32 -XX:+PerfDisableSharedMem -XX:MaxTenuringThreshold=1 -XX:-UseBiasedLocking -XX:UseAVX=3 -XX:+UseStringDeduplication -XX:+UseFastUnorderedTimeStamps -XX:+UseAES -XX:+UseAESIntrinsics -XX:UseSSE=4 -XX:+UseFMA -XX:AllocatePrefetchStyle=1 -XX:+UseLoopPredicate -XX:+RangeCheckElimination -XX:+EliminateLocks -XX:+DoEscapeAnalysis -XX:+UseCodeCacheFlushing -XX:+SegmentedCodeCache -XX:+UseFastJNIAccessors -XX:+OptimizeStringConcat -XX:+UseCompressedOops -XX:+UseThreadPriorities -XX:+OmitStackTraceInFastThrow -XX:+TrustFinalNonStaticFields -XX:ThreadPriorityPolicy=1 -XX:+UseInlineCaches -XX:+RewriteBytecodes -XX:+RewriteFrequentPairs -XX:+UseNUMA -XX:-DontCompileHugeMethods -XX:+UseFPUForSpilling -XX:+UseFastStosb -XX:+UseNewLongLShift -XX:+UseVectorCmov -XX:+UseXMMForArrayCopy -XX:+UseXmmI2D -XX:+UseXmmI2F -XX:+UseXmmLoadAndClearUpper -XX:+UseXmmRegToRegMoveAll -Dfile.encoding=UTF-8 -Xlog:async -Djava.security.egd=file:/dev/urandom --add-modules jdk.incubator.vector"

# https://itzg.github.io/docker-minecraft-docs/java/configuration/misc-options/
ENV EXTRA_ARGS="--universe ./worlds/"
ENV GUI="false"
ENV USE_SIMD_FLAGS="true"

# create a new system user and system group to restrict our container's runtime
RUN useradd --system --no-create-home --user-group minecraft
