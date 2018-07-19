---
title: TNEF-Korrelation in SMTP-Gateways und Transport
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 593f57d7-2891-40d1-a661-478a62d490ff
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: ec1d826ee2b3b46685a2c03dfaf45d2843869cc5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795736"
---
# <a name="tnef-correlation-in-smtp-gateways-and-transports"></a><span data-ttu-id="fa75a-103">TNEF-Korrelation in SMTP-Gateways und Transport</span><span class="sxs-lookup"><span data-stu-id="fa75a-103">TNEF Correlation in SMTP Gateways and Transports</span></span>

  
  
<span data-ttu-id="fa75a-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="fa75a-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="fa75a-105">Gateways und Transport, die mit dem Internet verbunden-basierte Systeme, mit denen SMTP verwenden, verwenden Sie den Wert von MessageID SMTP-Kopfzeile und die **PR_TNEF_CORRELATION_KEY** -Eigenschaft zur Implementierung einer TNEF Korrelation.</span><span class="sxs-lookup"><span data-stu-id="fa75a-105">Gateways and transports that connect to internet based systems, those that use SMTP, use the value of the MessageID SMTP header and the **PR_TNEF_CORRELATION_KEY** property to implement TNEF correlation.</span></span> 
  
<span data-ttu-id="fa75a-106">Der Wert der MessageID-Header der ausgehende Nachricht sollte der **PR_TNEF_CORRELATION_KEY** ([PidTagTnefCorrelationKey](pidtagtnefcorrelationkey-canonical-property.md))-Eigenschaft kopiert und in das [AttMAPIProps](attmapiprops.md) -Attribut des Datenstroms TNEF codiert werden.</span><span class="sxs-lookup"><span data-stu-id="fa75a-106">The value of the MessageID header of the outbound message should be copied to the **PR_TNEF_CORRELATION_KEY** ([PidTagTnefCorrelationKey](pidtagtnefcorrelationkey-canonical-property.md)) property and encoded in the [attMAPIProps](attmapiprops.md) attribute of the TNEF stream.</span></span> <span data-ttu-id="fa75a-107">Beachten Sie, dass **PR_TNEF_CORRELATION_KEY** eine binäre Eigenschaft, die MessageID eine Zeichenfolge ist. die null-Terminator sollte in der Kopie und im Vergleich eingefügt werden.</span><span class="sxs-lookup"><span data-stu-id="fa75a-107">Note that **PR_TNEF_CORRELATION_KEY** is a binary property, while the MessageID is a string; the null terminator should be included in the copy and in the comparison.</span></span> 
  
<span data-ttu-id="fa75a-108">Dieses Verfahren wird von allen Microsoft-Software verwendet, die mit dem Internet, wie beispielsweise Microsoft Exchange Server MAPI-basierten Messagingsystemen verbindet.</span><span class="sxs-lookup"><span data-stu-id="fa75a-108">This technique is used by all Microsoft software that connects MAPI-based messaging systems to the Internet, such as Microsoft Exchange Server.</span></span> <span data-ttu-id="fa75a-109">Dieses Verfahren sollte verwendet werden, durch eine beliebige SMTP-Gateways und Transport, die mit Systemen, die MAPI-Clients unterstützen verbunden, um die Interoperabilität zu maximieren.</span><span class="sxs-lookup"><span data-stu-id="fa75a-109">This technique should be used by any SMTP gateways and transports that connect to systems that support MAPI clients in order to maximize interoperability.</span></span>
  

