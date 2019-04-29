---
title: TNEF-Korrelation in SMTP-Gateways und-Übertragungen
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 593f57d7-2891-40d1-a661-478a62d490ff
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 0a685e081d319c43daa583d95d163677e81f2480
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413668"
---
# <a name="tnef-correlation-in-smtp-gateways-and-transports"></a><span data-ttu-id="a9525-103">TNEF-Korrelation in SMTP-Gateways und-Übertragungen</span><span class="sxs-lookup"><span data-stu-id="a9525-103">TNEF Correlation in SMTP Gateways and Transports</span></span>

  
  
<span data-ttu-id="a9525-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a9525-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a9525-105">Gateways und Übertragungen, die eine Verbindung mit internetbasierten Systemen herstellen, die SMTP verwenden, verwenden Sie den Wert des SMTP-Headers MessageID und die **PR_TNEF_CORRELATION_KEY** -Eigenschaft, um die TNEF-Korrelation zu implementieren.</span><span class="sxs-lookup"><span data-stu-id="a9525-105">Gateways and transports that connect to internet based systems, those that use SMTP, use the value of the MessageID SMTP header and the **PR_TNEF_CORRELATION_KEY** property to implement TNEF correlation.</span></span> 
  
<span data-ttu-id="a9525-106">Der Wert der MessageID-Kopfzeile der ausgehenden Nachricht sollte in die **PR_TNEF_CORRELATION_KEY** ([pidtagtnefcorrelationkey (](pidtagtnefcorrelationkey-canonical-property.md))-Eigenschaft kopiert und im [attMAPIProps](attmapiprops.md) -Attribut des TNEF-Streams codiert werden.</span><span class="sxs-lookup"><span data-stu-id="a9525-106">The value of the MessageID header of the outbound message should be copied to the **PR_TNEF_CORRELATION_KEY** ([PidTagTnefCorrelationKey](pidtagtnefcorrelationkey-canonical-property.md)) property and encoded in the [attMAPIProps](attmapiprops.md) attribute of the TNEF stream.</span></span> <span data-ttu-id="a9525-107">Beachten Sie, dass **PR_TNEF_CORRELATION_KEY** eine binäre Eigenschaft ist, während die MessageId eine Zeichenfolge ist; das NULL-Terminator sollte in der Kopie und im Vergleich enthalten sein.</span><span class="sxs-lookup"><span data-stu-id="a9525-107">Note that **PR_TNEF_CORRELATION_KEY** is a binary property, while the MessageID is a string; the null terminator should be included in the copy and in the comparison.</span></span> 
  
<span data-ttu-id="a9525-108">Diese Technik wird von allen Microsoft-Software verwendet, die MAPI-basierte Messagingsysteme mit dem Internet verbindet, wie beispielsweise Microsoft Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="a9525-108">This technique is used by all Microsoft software that connects MAPI-based messaging systems to the Internet, such as Microsoft Exchange Server.</span></span> <span data-ttu-id="a9525-109">Diese Technik sollte von allen SMTP-Gateways und-Übertragungen verwendet werden, die eine Verbindung zu Systemen herstellen, die MAPI-Clients unterstützen, um die Interoperabilität zu maximieren.</span><span class="sxs-lookup"><span data-stu-id="a9525-109">This technique should be used by any SMTP gateways and transports that connect to systems that support MAPI clients in order to maximize interoperability.</span></span>
  

