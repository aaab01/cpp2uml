# cpp2uml
a utility to show UML from c++ source file

## usage
- python cpp2uml.py any_source_dir/*.hpp > uml.txt
- java -jar plantuml.jar uml.txt
- generated demo.png at current directory, the example show as below.

## Requirements
- java
- plantUML http://plantuml.com/
- clang http://clang.llvm.org/get_started.html
- dot & graphviz

## Issue
- Only .hpp & .cpp file name accepted.
- It doesn't work when Class definition like below format(definition and its parent has been splited mult-line).
```
class Camera :
    public CameraBase<Camera>,
    public BnCameraClient
{
public:
```
- enum is discarded

- struct definition in Class would be discarded.
```
class example {
    struct Header {
        uint32_t type;
    } header;
};

```


- 
![image](https://github.com/aaab01/cpp2uml/blob/master/demo.png)
