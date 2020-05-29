# Hyperledger Fabric

# SDK

使用Go语言书写单元测试时，单元测试的函数名称要符合规范，函数的输入参数要来自testing软件包。一个测试用例使用testing.T结构体来表示。按照代码里面的注释，T的主要目的是管理测试的状态和测试的输出。T类型提供了Run方法来执行子测试函数。在使用Fabric SDK之前，需要提供一个配置文件，这个配置文件描述了网络及其成员身份的信息，也就是说在访问Fabric区块链网络的时候，需要知道必要的节点信息，使用何种身份来访问，身份的密码学身份的路径位置。

# Fabric

如果某个功能可能有多种实现方式，为了保持实现的灵活性，除了使用接口和实现的多态来解决这个矛盾之外，还可以使用函数类型达到同样的目的。函数类型作为结构体的组成部分，在结构体具体实例化的过程的时候，才真正决定函数实例的实现，从结构上，只是提供了函数的原型，在使用的时候，提供具体的实现。在做实现方式的切换的时候，仅仅需要把函数原型的实现替换掉就顺利的完成了实现机制的过度。

编程中的抽象与具体思维，先书写抽象形式的部分，在写具体实现的部分。成员的身份管理中对身份的有效性验证的一个考虑因素是时间的维度，考察身份是否在有效期范围内。身份信息中涉及到公钥信息的表示、证书结构的构造。对于提供的证书，如何检测是哪种算法提供的证书？判断的依据分别是哪些？如何保证可靠性？在不同软件包中同一个对象表示之间的转换。证书的不同形式的转换，譬如说想要一种字符串的形式的话，就需要编写一个从证书转换成字符串的规则和函数。