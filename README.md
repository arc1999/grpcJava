DESCRIPTION: <br />
This project implements the Client Side of a GRPC.The server side of the code is written in GO.The code can be fetched from https://github.com/arc1999/grpc
<br />
<br />
COMPILING RESOURCES <br />
We need to generate servicegrpc.java file from the proto file and also the class files from .proto file.
<br />
<br />
<br />
->for genrating ServiceGrpc <br />
------> we need to have protoc. <br />
-------->and then run the below command with proper path. <br />
$ protoc --plugin=protoc-gen-grpc-java=/home/ayush/protoc-gen-grpc-java-1.21.0-linux-x86_64.exe --grpc-java_out=/home/ayush/go -I/home/ayush/ /home/ayush/table.proto
<br />
<br />
<br />
-->for genrating the class files.<br />
-----> run the below command with proper paths.<br />
------> specifying the source directory (where your application's source code lives – the current directory is used if you don't provide a value), the destination directory (where you want the generated code to go; often the same as $SRC_DIR), and the path to your .proto. In this case, you...: <br />
$ protoc -I=$SRC_DIR --java_out=$DST_DIR $SRC_DIR/addressbook.proto  <br />
My command with correct path <br />
$ protoc -I=/home/ayush/grpcJava/ --java_out=/home/ayush/grpcJava/generated/main/java/com/proto/calculator/ /home/ayush/grpcJava/build/extracted-include-protos/test/table.proto
<br />
<br />
<br />
We can also use IDE for compiling of proto file.<br />
Follow the following Steps<br />
Delegate IDE Action<br />

This is necessary in order to allow IntelliJ to execute all build and test action via Gradle.<br />

    Navigate to Settings > Build, Exection, Deployment > Build Tools > Gradle > Runner
    Check the box Delegate IDE build/run actions to gradle

<br />
<br />
<br />
<br />
    
HOW TO RUN:<br />
-> Start the Server from the main.go file.(present in https://github.com/arc1999/grpc) You need to run the Server routine only(comment the client function).
<br />
-> Run the client.java file present in 'grpcJava/src/main/java/' directory.
<br />
-> Make Sure the Client and Server have the same Port no.
<br />
<br />

OUTPUT:
<br />
<br />
![task2](https://user-images.githubusercontent.com/36637661/59031684-fe4b0980-8881-11e9-8697-e65f1beb3018.png)
