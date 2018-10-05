---
title: MAPI-Objektvererbungshierarchie
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 3dc0b79f-e346-416d-ac81-42eba6b6d3b2
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 4b610415089ff19165ffcabc9e13901ed63c907d
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25391787"
---
# <a name="mapi-object-inheritance-hierarchy"></a><span data-ttu-id="7ccb0-103">MAPI-Objektvererbungshierarchie</span><span class="sxs-lookup"><span data-stu-id="7ccb0-103">MAPI object inheritance hierarchy</span></span>

<span data-ttu-id="7ccb0-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7ccb0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7ccb0-105">Alle von MAPI-Objekten implementiert Schnittstellen erben letztlich von [IUnknown](https://msdn.microsoft.com/library/33f1d79a-33fc-4ce5-a372-e08bda378332%28Office.15%29.aspx), die OLE-Schnittstelle, mit dem Objekte kommunizieren kann.</span><span class="sxs-lookup"><span data-stu-id="7ccb0-105">All interfaces implemented by MAPI objects ultimately inherit from [IUnknown](https://msdn.microsoft.com/library/33f1d79a-33fc-4ce5-a372-e08bda378332%28Office.15%29.aspx), the OLE interface that enables objects to communicate.</span></span> <span data-ttu-id="7ccb0-106">Die meisten Schnittstellen erben direkt von **IUnknown**, aber einige von einer von zwei anderen Basiskalender Schnittstellen erbt: [IMAPIProp: IUnknown](imapipropiunknown.md) oder [IMAPIContainer: IMAPIProp](imapicontainerimapiprop.md).</span><span class="sxs-lookup"><span data-stu-id="7ccb0-106">Most interfaces directly inherit from **IUnknown**, but some inherit from one of two other base interfaces: [IMAPIProp : IUnknown](imapipropiunknown.md) or [IMAPIContainer : IMAPIProp](imapicontainerimapiprop.md).</span></span> <span data-ttu-id="7ccb0-107">Die folgende Abbildung zeigt die vollständige Vererbungshierarchie in MAPI.</span><span class="sxs-lookup"><span data-stu-id="7ccb0-107">The following illustration shows the complete inheritance hierarchy in MAPI.</span></span>
  
<span data-ttu-id="7ccb0-108">**MAPI-Vererbungshierarchie**</span><span class="sxs-lookup"><span data-stu-id="7ccb0-108">**MAPI inheritance hierarchy**</span></span>
  
<span data-ttu-id="7ccb0-109">![MAPI-Vererbungshierarchie] (media/amapi_06.gif "MAPI-Vererbungshierarchie")</span><span class="sxs-lookup"><span data-stu-id="7ccb0-109">![MAPI inheritance hierarchy](media/amapi_06.gif "MAPI inheritance hierarchy")</span></span>
  
## <a name="see-also"></a><span data-ttu-id="7ccb0-110">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7ccb0-110">See also</span></span>

- [<span data-ttu-id="7ccb0-111">IMAPIProp : IUnknown</span><span class="sxs-lookup"><span data-stu-id="7ccb0-111">IMAPIProp : IUnknown</span></span>](imapipropiunknown.md) 
- [<span data-ttu-id="7ccb0-112">IMAPIContainer : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="7ccb0-112">IMAPIContainer : IMAPIProp</span></span>](imapicontainerimapiprop.md)
- [<span data-ttu-id="7ccb0-113">MAPI-Objekt und Übersicht über die Benutzeroberfläche</span><span class="sxs-lookup"><span data-stu-id="7ccb0-113">MAPI Object and Interface Overview</span></span>](mapi-object-and-interface-overview.md)

