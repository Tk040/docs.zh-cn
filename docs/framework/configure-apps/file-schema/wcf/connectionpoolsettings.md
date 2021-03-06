---
description: 了解详细信息： <connectionPoolSettings>
title: <connectionPoolSettings>
ms.date: 03/30/2017
ms.assetid: 6fa7fa65-2c6e-4eab-b8cf-7690112c0be5
ms.openlocfilehash: 5acf2d800f1a18f45750d0fabd23516f987b2c5e
ms.sourcegitcommit: ddf7edb67715a5b9a45e3dd44536dabc153c1de0
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/06/2021
ms.locfileid: "99782164"
---
# \<connectionPoolSettings>

指定命名管道绑定的其他连接池设置。  
  
[**\<configuration>**](../configuration-element.md)\
&nbsp;&nbsp;[**\<system.serviceModel>**](system-servicemodel.md)\
&nbsp;&nbsp;&nbsp;&nbsp;[**\<bindings>**](bindings.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<customBinding>**](custombinding.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<binding>**\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[**\<namedPipeTransport>**](namedpipetransport.md)\
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<connectionPoolSettings>**  
  
## <a name="syntax"></a>语法  
  
```xml  
<connectionPoolSettings groupName="String"
                        idleTimeout="TimeSpan"
                        maxOutboundConnectionsPerEndpoint="Integer" />
```  
  
## <a name="attributes-and-elements"></a>特性和元素  

 下列各节描述了特性、子元素和父元素。  
  
### <a name="attributes"></a>特性  
  
|属性|说明|  
|---------------|-----------------|  
|`groupName`|一个字符串，定义用于传出通道的连接池的名称。 在流处理模式中，不共享连接，这意味着禁用连接池。 默认值为字符串 "default"。 可以修改此值，以便将特定客户端的连接隔离到不同的组中。|  
|`idleTimeout`|一个值为正的 <xref:System.TimeSpan>，指定连接在断开前可以空闲的最长时间。 默认值为 00:02:00。|  
|`maxOutboundConnectionsPerEndpoint`|一个正整数，指定由服务启动的与远程终结点的最大连接数。 超出此限制的连接需要排队，直到连接数低于限制值。 `idleTimeout` 限制连接在引发异常前保持排队状态的持续时间。 默认值为 10。<br /><br /> 此属性限制从客户端到特定服务终结点的同时活动的连接数。 如果由于具有更多的活动客户端连接而超出此值，则服务可能表现为对客户端无响应。 在此情况下，应调整此值使之超过与特定终结点的同时活动的最大预期客户端连接数。|  
  
### <a name="child-elements"></a>子元素  

 无。  
  
### <a name="parent-elements"></a>父元素  
  
|元素|说明|  
|-------------|-----------------|  
|[\<namedPipeTransport>](namedpipetransport.md)|定义传输，该传输使通道使用命名管道传输消息。|  
  
## <a name="see-also"></a>请参阅

- <xref:System.ServiceModel.Configuration.NamedPipeConnectionPoolSettingsElement>
- <xref:System.ServiceModel.Channels.NamedPipeTransportBindingElement.ConnectionPoolSettings%2A>
- <xref:System.ServiceModel.Channels.NamedPipeConnectionPoolSettings>
- <xref:System.ServiceModel.Channels.TransportBindingElement>
- <xref:System.ServiceModel.Channels.CustomBinding>
- [传输](../../../wcf/feature-details/transports.md)
- [选择传输方式](../../../wcf/feature-details/choosing-a-transport.md)
- [绑定](../../../wcf/bindings.md)
- [扩展绑定](../../../wcf/extending/extending-bindings.md)
- [自定义绑定](../../../wcf/extending/custom-bindings.md)
- [\<customBinding>](custombinding.md)
