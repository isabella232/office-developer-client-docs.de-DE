---
title: Objekte und die MAPI-Architektur
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: c3bcbda5-820d-4ef5-bffd-c254eea9dff6
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 4f8bc2a5268d220c17a59148f8b8ba1d320d225b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32279788"
---
# <a name="objects-and-the-mapi-architecture"></a><span data-ttu-id="aba8b-103">Objekte und die MAPI-Architektur</span><span class="sxs-lookup"><span data-stu-id="aba8b-103">Objects and the MAPI architecture</span></span>

<span data-ttu-id="aba8b-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="aba8b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="aba8b-105">Alle objekte, die MAPI definiert, fallen in eine oder mehrere Ebenen der MAPI-Architektur.</span><span class="sxs-lookup"><span data-stu-id="aba8b-105">All of the objects that MAPI defines fall into one or more layers in the MAPI architecture.</span></span> <span data-ttu-id="aba8b-106">Die Clientschnittstellenebene enthält alle Objekte, die eine Clientanwendung, eine Formularanzeige oder ein Formularserver implementieren kann.</span><span class="sxs-lookup"><span data-stu-id="aba8b-106">The client interface layer contains all the objects that a client application, form viewer, or form server can implement.</span></span> <span data-ttu-id="aba8b-107">Die Schnittstellesebene des Dienstanbieters enthält die Objekte, die ein Dienstanbieter eines beliebigen Typs implementieren kann.</span><span class="sxs-lookup"><span data-stu-id="aba8b-107">The service provider interface layer contains the objects that a service provider of any type can implement.</span></span> <span data-ttu-id="aba8b-108">Diese Ebene umfasst Objekte, die von Adressbüchern, Nachrichtenspeichern, Transportanbietern und Formularbibliotheken implementiert werden.</span><span class="sxs-lookup"><span data-stu-id="aba8b-108">This layer includes objects implemented by address books, message stores, transport providers, and form libraries.</span></span> <span data-ttu-id="aba8b-109">Die Ebene, die das MAPI-Subsystem darstellt, wird zwischen den Client- und Dienstanbieterschnittstellenebenen positioniert.</span><span class="sxs-lookup"><span data-stu-id="aba8b-109">The layer that represents the MAPI subsystem is positioned between the client and service provider interface layers.</span></span> <span data-ttu-id="aba8b-110">Die MAPI-Ebene enthält alle Objekte, die MAPI für Clients oder Dienstanbieter implementiert.</span><span class="sxs-lookup"><span data-stu-id="aba8b-110">The MAPI layer contains all of the objects that MAPI implements for clients or service providers to use.</span></span> 
  
<span data-ttu-id="aba8b-111">Die folgende Abbildung zeigt, wo die einzelnen MAPI-Objekte in die MAPI-Architektur passen.</span><span class="sxs-lookup"><span data-stu-id="aba8b-111">The following illustration shows where each of the MAPI objects fits into the MAPI architecture.</span></span> <span data-ttu-id="aba8b-112">Die Objekte werden mit den Namen ihrer abgeleiteten Schnittstellen dargestellt.</span><span class="sxs-lookup"><span data-stu-id="aba8b-112">The objects are represented with the names of their derived interfaces.</span></span> <span data-ttu-id="aba8b-113">Beispielsweise wird ein Advise Sink -Objekt als [IMAPIAdviseSink angezeigt: IUnknown](imapiadvisesinkiunknown.md), die Schnittstelle, die von [IUnknown](https://msdn.microsoft.com/library/33f1d79a-33fc-4ce5-a372-e08bda378332%28Office.15%29.aspx) ab leitet und die jedes advise sink -Objekt implementiert.</span><span class="sxs-lookup"><span data-stu-id="aba8b-113">For example, an advise sink object is shown as [IMAPIAdviseSink : IUnknown](imapiadvisesinkiunknown.md), the interface that derives from [IUnknown](https://msdn.microsoft.com/library/33f1d79a-33fc-4ce5-a372-e08bda378332%28Office.15%29.aspx) and that every advise sink object implements.</span></span> <span data-ttu-id="aba8b-114">Die Schnittstellen, die Layer überbrücken, werden von mehreren Komponenten verwendet oder implementiert.</span><span class="sxs-lookup"><span data-stu-id="aba8b-114">The interfaces that bridge layers are either used or implemented by multiple components.</span></span> <span data-ttu-id="aba8b-115">Obwohl die MAPI-Ebene die Client- und Anbieterebenen zu trennen scheint, bedeutet dies, dass die kommunikation über MAPI fließen muss, dies ist jedoch nicht der Fall.</span><span class="sxs-lookup"><span data-stu-id="aba8b-115">Although the MAPI layer appears to separate the client and provider layers, implying that all communication must flow through MAPI, this is not the case.</span></span> <span data-ttu-id="aba8b-116">Clients können und können direkt mit Dienstanbieterobjekten kommunizieren.</span><span class="sxs-lookup"><span data-stu-id="aba8b-116">Clients can and do communicate directly to service provider objects.</span></span> 
  
<span data-ttu-id="aba8b-117">**Objektschichten in MAPI**</span><span class="sxs-lookup"><span data-stu-id="aba8b-117">**Object layers in MAPI**</span></span>
  
<span data-ttu-id="aba8b-118">![Objektebenen in MAPI-Objektebenen](media/amapi_38.gif "in MAPI")</span><span class="sxs-lookup"><span data-stu-id="aba8b-118">![Object layers in MAPI](media/amapi_38.gif "Object layers in MAPI")</span></span>
  
## <a name="see-also"></a><span data-ttu-id="aba8b-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="aba8b-119">See also</span></span>

- [<span data-ttu-id="aba8b-120">IMAPIAdviseSink : IUnknown</span><span class="sxs-lookup"><span data-stu-id="aba8b-120">IMAPIAdviseSink : IUnknown</span></span>](imapiadvisesinkiunknown.md)
- [<span data-ttu-id="aba8b-121">Übersicht über das MAPI-Objekt und die Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="aba8b-121">MAPI Object and Interface Overview</span></span>](mapi-object-and-interface-overview.md)

