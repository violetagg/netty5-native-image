# netty5-native-image

## How to run the example
- Specify `JAVA_HOME` to `graalvm`
- Execute `mvn -Pnative package`

The following exception is observed

```
> org.graalvm.compiler.graph.GraalGraphError: com.oracle.svm.core.util.VMError$HostedError: New VarHandle found after static analysis
        at node: 3|LoadField#RECEIVED { uncheckedStamp=null, memoryOrder=PLAIN, nodeSourcePosition=at io.netty5.buffer.internal.SendFromOwned.gateReception(SendFromOwned.java:56) [bci: 0], field=AnalysisField<SendFromOwned.RECEIVED -> HotSpotResolvedJavaFieldImpl<io.netty5.buffer.internal.SendFromOwned.RECEIVED VarHandle:112>, accessed: false, read: true, written: true, folded: false>, stamp=a java.lang.invoke.VarHandle, location=SendFromOwned.RECEIVED,  }
```
