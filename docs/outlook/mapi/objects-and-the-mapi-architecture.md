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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25391040"
---
# <a name="objects-and-the-mapi-architecture"></a><span data-ttu-id="188bd-103">Objekte und die MAPI-Architektur</span><span class="sxs-lookup"><span data-stu-id="188bd-103">Objects and the MAPI architecture</span></span>

<span data-ttu-id="188bd-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="188bd-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="188bd-105">Alle Objekte, die MAPI definiert fallen in eine oder mehrere Ebenen in der MAPI-Architektur.</span><span class="sxs-lookup"><span data-stu-id="188bd-105">All of the objects that MAPI defines fall into one or more layers in the MAPI architecture.</span></span> <span data-ttu-id="188bd-106">Die Ebene der Client-Schnittstelle enthält alle Objekte, die eine Clientanwendung, Formular Viewer oder Formular Server implementieren können.</span><span class="sxs-lookup"><span data-stu-id="188bd-106">The client interface layer contains all the objects that a client application, form viewer, or form server can implement.</span></span> <span data-ttu-id="188bd-107">Die Service Provider-Schnittstellenebene enthält die Objekte, die ein Dienstanbieter eines beliebigen Typs implementieren können.</span><span class="sxs-lookup"><span data-stu-id="188bd-107">The service provider interface layer contains the objects that a service provider of any type can implement.</span></span> <span data-ttu-id="188bd-108">Diese Schicht umfasst Objekte, die von Adressbüchern, Nachrichtenspeicher, Transportanbieter und Formularbibliotheken implementiert.</span><span class="sxs-lookup"><span data-stu-id="188bd-108">This layer includes objects implemented by address books, message stores, transport providers, and form libraries.</span></span> <span data-ttu-id="188bd-109">Die Ebene, die das MAPI-Subsystem steht, wird zwischen dem Client und Dienst Anbieter Benutzeroberflächenebenen positioniert.</span><span class="sxs-lookup"><span data-stu-id="188bd-109">The layer that represents the MAPI subsystem is positioned between the client and service provider interface layers.</span></span> <span data-ttu-id="188bd-110">Die MAPI-Ebene enthält alle Objekte, die MAPI-Clients oder-Dienstanbieter verwenden implementiert wird.</span><span class="sxs-lookup"><span data-stu-id="188bd-110">The MAPI layer contains all of the objects that MAPI implements for clients or service providers to use.</span></span> 
  
<span data-ttu-id="188bd-111">Die folgende Abbildung zeigt, in dem einzelnen MAPI-Objekte in der MAPI-Architektur passt.</span><span class="sxs-lookup"><span data-stu-id="188bd-111">The following illustration shows where each of the MAPI objects fits into the MAPI architecture.</span></span> <span data-ttu-id="188bd-112">Die Objekte werden mit den Namen ihrer abgeleiteten Schnittstellen dargestellt.</span><span class="sxs-lookup"><span data-stu-id="188bd-112">The objects are represented with the names of their derived interfaces.</span></span> <span data-ttu-id="188bd-113">Beispielsweise ein Empfängerobjekt Advise wird angezeigt als [IMAPIAdviseSink: IUnknown](imapiadvisesinkiunknown.md), die Schnittstelle, die von [IUnknown](https://msdn.microsoft.com/library/33f1d79a-33fc-4ce5-a372-e08bda378332%28Office.15%29.aspx) abgeleitet wird und an, die jedes Empfängerobjekt Advise implementiert wird.</span><span class="sxs-lookup"><span data-stu-id="188bd-113">For example, an advise sink object is shown as [IMAPIAdviseSink : IUnknown](imapiadvisesinkiunknown.md), the interface that derives from [IUnknown](https://msdn.microsoft.com/library/33f1d79a-33fc-4ce5-a372-e08bda378332%28Office.15%29.aspx) and that every advise sink object implements.</span></span> <span data-ttu-id="188bd-114">Die Schnittstellen, die Ebenen Brücke sind entweder verwendet oder von mehreren Komponenten implementiert.</span><span class="sxs-lookup"><span data-stu-id="188bd-114">The interfaces that bridge layers are either used or implemented by multiple components.</span></span> <span data-ttu-id="188bd-115">Obwohl die MAPI-Ebene angezeigt wird, trennen die Client- und Anbieter Ebenen, sagen, dass die gesamte Kommunikation über MAPI, flow muss ist dies nicht der Fall.</span><span class="sxs-lookup"><span data-stu-id="188bd-115">Although the MAPI layer appears to separate the client and provider layers, implying that all communication must flow through MAPI, this is not the case.</span></span> <span data-ttu-id="188bd-116">Clients können, und führen Sie kommunizieren direkt an dienstanbieterobjekten.</span><span class="sxs-lookup"><span data-stu-id="188bd-116">Clients can and do communicate directly to service provider objects.</span></span> 
  
<span data-ttu-id="188bd-117">**Objektschichten in MAPI**</span><span class="sxs-lookup"><span data-stu-id="188bd-117">**Object layers in MAPI**</span></span>
  
<span data-ttu-id="188bd-118">![Objektebenen in MAPI] (media/amapi_38.gif "Objektebenen in MAPI")</span><span class="sxs-lookup"><span data-stu-id="188bd-118">![Object layers in MAPI](media/amapi_38.gif "Object layers in MAPI")</span></span>
  
## <a name="see-also"></a><span data-ttu-id="188bd-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="188bd-119">See also</span></span>

- [<span data-ttu-id="188bd-120">IMAPIAdviseSink : IUnknown</span><span class="sxs-lookup"><span data-stu-id="188bd-120">IMAPIAdviseSink : IUnknown</span></span>](imapiadvisesinkiunknown.md)
- [<span data-ttu-id="188bd-121">MAPI-Objekt und Übersicht über die Benutzeroberfläche</span><span class="sxs-lookup"><span data-stu-id="188bd-121">MAPI Object and Interface Overview</span></span>](mapi-object-and-interface-overview.md)

