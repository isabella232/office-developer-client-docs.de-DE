---
title: MAPI-Objektvererbungshierarchie
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 3dc0b79f-e346-416d-ac81-42eba6b6d3b2
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: a03b994a613bbb1f17db3e3220b7e053989c278a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19793021"
---
# <a name="mapi-object-inheritance-hierarchy"></a>MAPI-Objektvererbungshierarchie

**Betrifft**: Outlook 
  
Alle von MAPI-Objekten implementiert Schnittstellen erben letztlich von [IUnknown](http://msdn.microsoft.com/library/33f1d79a-33fc-4ce5-a372-e08bda378332%28Office.15%29.aspx), die OLE-Schnittstelle, mit dem Objekte kommunizieren kann. Die meisten Schnittstellen erben direkt von **IUnknown**, aber einige von einer von zwei anderen Basiskalender Schnittstellen erbt: [IMAPIProp: IUnknown](imapipropiunknown.md) oder [IMAPIContainer: IMAPIProp](imapicontainerimapiprop.md). Die folgende Abbildung zeigt die vollständige Vererbungshierarchie in MAPI.
  
**MAPI-Vererbungshierarchie**
  
![MAPI-Vererbungshierarchie] (media/amapi_06.gif "MAPI-Vererbungshierarchie")
  
## <a name="see-also"></a>Siehe auch

- [IMAPIProp: IUnknown](imapipropiunknown.md) 
- [IMAPIContainer: IMAPIProp](imapicontainerimapiprop.md)
- [MAPI-Objekt und Übersicht über die Benutzeroberfläche](mapi-object-and-interface-overview.md)

