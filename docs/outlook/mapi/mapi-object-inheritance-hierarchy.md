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
# <a name="mapi-object-inheritance-hierarchy"></a>Vererbungshierarchie des MAPI-Objekts

**Gilt für**: Outlook 2013 | Outlook 2016 
  
Alle von MAPI-Objekten implementierten Schnittstellen erben letztendlich von [IUnknown](https://msdn.microsoft.com/library/33f1d79a-33fc-4ce5-a372-e08bda378332%28Office.15%29.aspx), der OLE-Schnittstelle, über die Objekte kommunizieren können. Die meisten Schnittstellen erben direkt von **IUnknown**, aber einige erben von einer von zwei anderen Basisschnittstellen: [IMAPIProp : IUnknown](imapipropiunknown.md) oder [IMAPIContainer : IMAPIProp](imapicontainerimapiprop.md). Die folgende Abbildung zeigt die vollständige Vererbungshierarchie in MAPI.
  
**MAPI-Vererbungshierarchie**
  
![MAPI-Vererbungshierarchie](media/amapi_06.gif "MAPI-Vererbungshierarchie")
  
## <a name="see-also"></a>Siehe auch

- [IMAPIProp : IUnknown](imapipropiunknown.md) 
- [IMAPIContainer : IMAPIProp](imapicontainerimapiprop.md)
- [Übersicht über das MAPI-Objekt und die Schnittstelle](mapi-object-and-interface-overview.md)

