---
title: Vererbungshierarchie des MAPI-Objekts
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 3dc0b79f-e346-416d-ac81-42eba6b6d3b2
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 4b610415089ff19165ffcabc9e13901ed63c907d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345840"
---
# <a name="mapi-object-inheritance-hierarchy"></a><span data-ttu-id="b4933-103">Vererbungshierarchie des MAPI-Objekts</span><span class="sxs-lookup"><span data-stu-id="b4933-103">MAPI object inheritance hierarchy</span></span>

<span data-ttu-id="b4933-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b4933-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b4933-105">Alle von MAPI-Objekten implementierten Schnittstellen erben letztendlich von [IUnknown](https://msdn.microsoft.com/library/33f1d79a-33fc-4ce5-a372-e08bda378332%28Office.15%29.aspx), der OLE-Schnittstelle, über die Objekte kommunizieren können.</span><span class="sxs-lookup"><span data-stu-id="b4933-105">All interfaces implemented by MAPI objects ultimately inherit from [IUnknown](https://msdn.microsoft.com/library/33f1d79a-33fc-4ce5-a372-e08bda378332%28Office.15%29.aspx), the OLE interface that enables objects to communicate.</span></span> <span data-ttu-id="b4933-106">Die meisten Schnittstellen erben direkt von **IUnknown**, aber einige erben von einer von zwei anderen Basisschnittstellen: [IMAPIProp : IUnknown](imapipropiunknown.md) oder [IMAPIContainer : IMAPIProp](imapicontainerimapiprop.md).</span><span class="sxs-lookup"><span data-stu-id="b4933-106">Most interfaces directly inherit from **IUnknown**, but some inherit from one of two other base interfaces: [IMAPIProp : IUnknown](imapipropiunknown.md) or [IMAPIContainer : IMAPIProp](imapicontainerimapiprop.md).</span></span> <span data-ttu-id="b4933-107">Die folgende Abbildung zeigt die vollständige Vererbungshierarchie in MAPI.</span><span class="sxs-lookup"><span data-stu-id="b4933-107">The following illustration shows the complete inheritance hierarchy in MAPI.</span></span>
  
<span data-ttu-id="b4933-108">**MAPI-Vererbungshierarchie**</span><span class="sxs-lookup"><span data-stu-id="b4933-108">**MAPI inheritance hierarchy**</span></span>
  
<span data-ttu-id="b4933-109">![MAPI-Vererbungshierarchie](media/amapi_06.gif "MAPI-Vererbungshierarchie")</span><span class="sxs-lookup"><span data-stu-id="b4933-109">![MAPI inheritance hierarchy](media/amapi_06.gif "MAPI inheritance hierarchy")</span></span>
  
## <a name="see-also"></a><span data-ttu-id="b4933-110">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b4933-110">See also</span></span>

- [<span data-ttu-id="b4933-111">IMAPIProp : IUnknown</span><span class="sxs-lookup"><span data-stu-id="b4933-111">IMAPIProp : IUnknown</span></span>](imapipropiunknown.md) 
- [<span data-ttu-id="b4933-112">IMAPIContainer : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="b4933-112">IMAPIContainer : IMAPIProp</span></span>](imapicontainerimapiprop.md)
- [<span data-ttu-id="b4933-113">Übersicht über das MAPI-Objekt und die Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="b4933-113">MAPI Object and Interface Overview</span></span>](mapi-object-and-interface-overview.md)

