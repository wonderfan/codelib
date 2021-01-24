区块链技术的可配置性，组件模块可配置性。区块链通过技术来实现不可篡改、可验证、可审计、抗攻击。不同的实现采用不同的机制来提供这些技术属性。区块链私有网络由分布式节点组成的点对点网络。联盟链网络不存在单个唯一的架构。在云计算平台中可以使用网络的隔离作用来实现联盟链网络。

基于HTTP协议的白名单列表，使用HTTP端点作为模块来形成命名空间从而达到控制访问的目的。

许可链和联盟链之间的差异，授权机制下的数据共享。
链下服务接口和生命周期。
数据资产模型和交易。
大数据支持。

权限授权、黑名单授权、节点授权、参数授权、身份授权、预言机授权。

主观标准和客观标准。联盟链是由若干组织运营的区块链网络。

联盟链权限系统设计：采用应用编程接口和后端实现代码组织形式。在应用编程接口中，对权限相关的操作进行规范定义；在后端实现中，定义权限控制器，实现具体的权限操作。应用编程接口使用结构体数据类型及其方法列表即可实现对外接口的目的。对外接口是一个统一的形式，后端实现中有不同的机制实现，在权限控制器中使用类型和版本来进行切换。
节点连接权限控制方法一：使用配置文件预先设定节点列表，检查连接节点是否在文件中，并且不是包含在黑名单中。
节点连接权限控制方法二：使用缓存机制和智能合约来管理节点列表和节点状态，对节点的可连接性进行审批，判断节点的状态是approved，allowed and disallowed。
节点连接权限控制方法三：使用权限控制服务来检测连接状态，基于节点信息生成节点编码和加密之后的身份标识符，使用编码后的身份标识符作为判断的依据，与智能合约存储的数据和状态进行对比。

使用一个源代码文件来专门儿书写和定义应用编程接口，需要关注服务接口与整个应用接口之间的关联。与网络应用相关的处理对象和数据实体。与区块链相关的依赖包括链的数据存储模型、密码相关、数据库访问相关、运行时的逻辑形式和数据表示。
根据请求的内容类型，提取请求中的内容并对内容进行正确的格式转换和数据封装。
专门书写一个状态结构体实体，用于服务应用编程接口与底层区块链和快照相关的数据操作。
在源代码中编写了服务应用编程接口、服务编译成接口相关的数据对象、服务应用编程接口构造器。建设目标实体对象，围绕目标实体对象进行全范围的外围相关方面配套建设。
在服务应用编程接口上，构造前后端交互所需要的数据，并对数据的使用范围作出公开和私有两种作用域。
使用一个结构体实体对象来刻画方法所具有的特征和属性。围绕方法描述符来进行方法调用的接口定义，为方法调用接口提供最基本的实现。不同软件程序规范的部署规范说明。接口层次化定义以及接口实现的层次化描述。中间件服务是在服务执行过程中间插入额外的组件进行处理的方式方法。

区块链框架是使用中间件方式串联起来的框架，服务是对框架功能的扩展。框架为创建区块链提供了基本构建，预留了交易处理的具体规则。服务的实现可以完成交易具体规则的处理。服务明确了交易处理的规则，交易会影响服务的状态。交易引起的状态变化会持久到键值对存储或数据库中。外部客户端可以读取服务的相关数据。服务的核心责任主要有两个方面：一是在交易处理流程中接收外部交易；二是对状态数据库进行读写操作。服务会运行在验证者节点和审计节点。服务有服务的管理者进行统一的管理，对服务进行实例化、关停服务、暂停服务、恢复服务和升级服务。与服务的生命周期操作相关有事件触发。

交易是对数据库的一系列的交易，交易的处理规则使用服务来定义和实现。这些交易规则决定了区块链应用的商业逻辑。交易封装在消息中。消息中除了交易的内容，还包括交易的创建者和发送者的签名。通过验证者的共识算法将交易包含在区块中。交易用消息来表示，消息中包含了交易的发送者的身份和验证方法。交易消息中除了交易的数据之外，交易的类型，以及方法调用信息也包括在消息内容体中。

交易消息数据结构的构造，推荐的一种形式是树状字典表。交易消息的序列化采用原型缓冲机制。交易的表示和交易处理器的接口，以及串联交易表示和交易处理器的中间件框架。交易处理器使用服务来实现，为服务提供运行时接口定义和实现。在交易消息数据实体之外，还设计执行的上下文对象来描述和囊括其他额外的数据信息。

交易的流程及交易自带属性：交易创建、交易提交、交易验证、交易广播、交易共识、交易事务处理。

服务生命周期：服务软件程序、服务实例化、服务状态转移，数据迁移。

轻量级客户端所持有的功能以及在区块链网络中作用。轻量级客户端使用适宜的高级语言来实现。原始交易数据通过业务应用提交到轻量级客户端，完成数据序列化和签名，然后再提交到全节点，业务应用受到交易处理的响应。

系统配置决定区块链网络的行为和能力，服务有自己专属的配置。从范围来看，分为全局和本地两种范围。配置具体项包括共识方面的配置、验证者密钥配置、内置服务配置、本地配置、网络配置、应用编程接口配置、内存池配置、变更配置。全节点的全局配置都是一样的，本地化配置实现不同节点相关配置的不同。全局配置只能通过监管者服务来进行变更。验证者节点有两个密钥：共识密钥和服务密钥。共识密钥用于共识过程中，服务密钥用于由服务产生的交易并对交易进行签名。

数据库提供一种持久化的能力，存储默克尔形式的数据结构。使用协议缓冲作为数据通讯序列化格式。共识算法是由一组参与者参与处理，并对处理结果达成共识。参与共识的节点需要亮明身份。网络节点之间建立通道之前先进行身份验证，在进行消息传递加密。全节点网络结构包括验证者和审计者两种节点组成的网络拓扑。整个区块链网络有全节点和轻节点共同组成。

区块链网络监管者服务，控制服务的生命周期，由节点管理者大多数授权同意才能进行监管者相关操作。