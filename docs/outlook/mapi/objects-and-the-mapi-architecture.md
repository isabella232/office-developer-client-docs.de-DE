---
title: Objekte und die MAPI-Architektur
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: c3bcbda5-820d-4ef5-bffd-c254eea9dff6
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 0e89c2ad37b700a977962e5e0ff0ca30b9d910e2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19793311"
---
# <a name="objects-and-the-mapi-architecture"></a><span data-ttu-id="542ee-103">Objekte und die MAPI-Architektur</span><span class="sxs-lookup"><span data-stu-id="542ee-103">Objects and the MAPI architecture</span></span>

<span data-ttu-id="542ee-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="542ee-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="542ee-105">Alle Objekte, die MAPI definiert fallen in eine oder mehrere Ebenen in der MAPI-Architektur.</span><span class="sxs-lookup"><span data-stu-id="542ee-105">All of the objects that MAPI defines fall into one or more layers in the MAPI architecture.</span></span> <span data-ttu-id="542ee-106">Die Ebene der Client-Schnittstelle enthält alle Objekte, die eine Clientanwendung, Formular Viewer oder Formular Server implementieren können.</span><span class="sxs-lookup"><span data-stu-id="542ee-106">The client interface layer contains all the objects that a client application, form viewer, or form server can implement.</span></span> <span data-ttu-id="542ee-107">Die Service Provider-Schnittstellenebene enthält die Objekte, die ein Dienstanbieter eines beliebigen Typs implementieren können.</span><span class="sxs-lookup"><span data-stu-id="542ee-107">The service provider interface layer contains the objects that a service provider of any type can implement.</span></span> <span data-ttu-id="542ee-108">Diese Schicht umfasst Objekte, die von Adressbüchern, Nachrichtenspeicher, Transportanbieter und Formularbibliotheken implementiert.</span><span class="sxs-lookup"><span data-stu-id="542ee-108">This layer includes objects implemented by address books, message stores, transport providers, and form libraries.</span></span> <span data-ttu-id="542ee-109">Die Ebene, die das MAPI-Subsystem steht, wird zwischen dem Client und Dienst Anbieter Benutzeroberflächenebenen positioniert.</span><span class="sxs-lookup"><span data-stu-id="542ee-109">The layer that represents the MAPI subsystem is positioned between the client and service provider interface layers.</span></span> <span data-ttu-id="542ee-110">Die MAPI-Ebene enthält alle Objekte, die MAPI-Clients oder-Dienstanbieter verwenden implementiert wird.</span><span class="sxs-lookup"><span data-stu-id="542ee-110">The MAPI layer contains all of the objects that MAPI implements for clients or service providers to use.</span></span> 
  
<span data-ttu-id="542ee-111">Die folgende Abbildung zeigt, in dem einzelnen MAPI-Objekte in der MAPI-Architektur passt.</span><span class="sxs-lookup"><span data-stu-id="542ee-111">The following illustration shows where each of the MAPI objects fits into the MAPI architecture.</span></span> <span data-ttu-id="542ee-112">Die Objekte werden mit den Namen ihrer abgeleiteten Schnittstellen dargestellt.</span><span class="sxs-lookup"><span data-stu-id="542ee-112">The objects are represented with the names of their derived interfaces.</span></span> <span data-ttu-id="542ee-113">Beispielsweise ein Empfängerobjekt Advise wird angezeigt als [IMAPIAdviseSink: IUnknown](imapiadvisesinkiunknown.md), die Schnittstelle, die von [IUnknown](http://msdn.microsoft.com/library/33f1d79a-33fc-4ce5-a372-e08bda378332%28Office.15%29.aspx) abgeleitet wird und an, die jedes Empfängerobjekt Advise implementiert wird.</span><span class="sxs-lookup"><span data-stu-id="542ee-113">For example, an advise sink object is shown as [IMAPIAdviseSink : IUnknown](imapiadvisesinkiunknown.md), the interface that derives from [IUnknown](http://msdn.microsoft.com/library/33f1d79a-33fc-4ce5-a372-e08bda378332%28Office.15%29.aspx) and that every advise sink object implements.</span></span> <span data-ttu-id="542ee-114">Die Schnittstellen, die Ebenen Brücke sind entweder verwendet oder von mehreren Komponenten implementiert.</span><span class="sxs-lookup"><span data-stu-id="542ee-114">The interfaces that bridge layers are either used or implemented by multiple components.</span></span> <span data-ttu-id="542ee-115">Obwohl die MAPI-Ebene angezeigt wird, trennen die Client- und Anbieter Ebenen, sagen, dass die gesamte Kommunikation über MAPI, flow muss ist dies nicht der Fall.</span><span class="sxs-lookup"><span data-stu-id="542ee-115">Although the MAPI layer appears to separate the client and provider layers, implying that all communication must flow through MAPI, this is not the case.</span></span> <span data-ttu-id="542ee-116">Clients können, und führen Sie kommunizieren direkt an dienstanbieterobjekten.</span><span class="sxs-lookup"><span data-stu-id="542ee-116">Clients can and do communicate directly to service provider objects.</span></span> 
  
<span data-ttu-id="542ee-117">**Objektebenen in MAPI**</span><span class="sxs-lookup"><span data-stu-id="542ee-117">**Object layers in MAPI**</span></span>
  
<span data-ttu-id="542ee-118">![Objektebenen in MAPI] (media/amapi_38.gif "Objektebenen in MAPI")</span><span class="sxs-lookup"><span data-stu-id="542ee-118">![Object layers in MAPI](media/amapi_38.gif "Object layers in MAPI")</span></span>
  
## <a name="see-also"></a><span data-ttu-id="542ee-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="542ee-119">See also</span></span>

- [<span data-ttu-id="542ee-120">IMAPIAdviseSink: IUnknown</span><span class="sxs-lookup"><span data-stu-id="542ee-120">IMAPIAdviseSink : IUnknown</span></span>](imapiadvisesinkiunknown.md)
- [<span data-ttu-id="542ee-121">MAPI-Objekt und Übersicht über die Benutzeroberfläche</span><span class="sxs-lookup"><span data-stu-id="542ee-121">MAPI Object and Interface Overview</span></span>](mapi-object-and-interface-overview.md)

