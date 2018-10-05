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
# <a name="mapi-object-inheritance-hierarchy"></a>MAPI-Objektvererbungshierarchie

**Gilt für**: Outlook 2013 | Outlook 2016 
  
Alle von MAPI-Objekten implementiert Schnittstellen erben letztlich von [IUnknown](https://msdn.microsoft.com/library/33f1d79a-33fc-4ce5-a372-e08bda378332%28Office.15%29.aspx), die OLE-Schnittstelle, mit dem Objekte kommunizieren kann. Die meisten Schnittstellen erben direkt von **IUnknown**, aber einige von einer von zwei anderen Basiskalender Schnittstellen erbt: [IMAPIProp: IUnknown](imapipropiunknown.md) oder [IMAPIContainer: IMAPIProp](imapicontainerimapiprop.md). Die folgende Abbildung zeigt die vollständige Vererbungshierarchie in MAPI.
  
**MAPI-Vererbungshierarchie**
  
![MAPI-Vererbungshierarchie] (media/amapi_06.gif "MAPI-Vererbungshierarchie")
  
## <a name="see-also"></a>Siehe auch

- [IMAPIProp : IUnknown](imapipropiunknown.md) 
- [IMAPIContainer : IMAPIProp](imapicontainerimapiprop.md)
- [MAPI-Objekt und Übersicht über die Benutzeroberfläche](mapi-object-and-interface-overview.md)

