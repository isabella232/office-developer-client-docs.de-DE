---
title: VERerbungshierarchie für MAPI-Objekte
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 3dc0b79f-e346-416d-ac81-42eba6b6d3b2
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: af56854905b05f8b2c878f98c3e3c1c17971fc4f
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59567172"
---
# <a name="mapi-object-inheritance-hierarchy"></a>VERerbungshierarchie für MAPI-Objekte

**Gilt für**: Outlook 2013 | Outlook 2016 
  
Alle von MAPI-Objekten implementierten Schnittstellen erben letztlich von [IUnknown](https://msdn.microsoft.com/library/33f1d79a-33fc-4ce5-a372-e08bda378332%28Office.15%29.aspx), der OLE-Schnittstelle, die die Kommunikation von Objekten ermöglicht. Die meisten Schnittstellen erben direkt von **IUnknown,** einige jedoch von einer von zwei anderen [Basisschnittstellen: IMAPIProp : IUnknown](imapipropiunknown.md) oder [IMAPIContainer : IMAPIProp](imapicontainerimapiprop.md). Die folgende Abbildung zeigt die vollständige Vererbungshierarchie in MAPI.
  
**MAPI-Vererbungshierarchie**
  
![MAPI-Vererbungshierarchie](media/amapi_06.gif "MAPI-Vererbungshierarchie")
  
## <a name="see-also"></a>Siehe auch

- [IMAPIProp : IUnknown](imapipropiunknown.md) 
- [IMAPIContainer : IMAPIProp](imapicontainerimapiprop.md)
- [Übersicht über MAPI-Objekt und -Schnittstelle](mapi-object-and-interface-overview.md)

