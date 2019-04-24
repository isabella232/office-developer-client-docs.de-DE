---
title: MAPIUID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.MAPIUID
api_type:
- COM
ms.assetid: 63eac3ee-e59b-4a06-8bb9-f72764d84bda
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: da314205f7d2dd746b72aa7e2b5ff2a13bb0c21b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32269923"
---
# <a name="mapiuid"></a>MAPIUID

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Eine unabhängige Bytereihenfolge-Version einer [GUID](guid.md) -Struktur, die zum eindeutigen Identifizieren eines Dienstanbieters verwendet wird. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapidefs. h  <br/> |
|Zugehöriges Makro:  <br/> |[IsEqualMAPIUID](isequalmapiuid.md) <br/> |
   
```cpp
typedef struct _MAPIUID
{
  BYTE ab[16];
} MAPIUID, FAR *LPMAPIUID;

```

## <a name="members"></a>Elemente

 **ab**
  
> Ein Array, das einen 16-Byte-Bezeichner enthält.
    
## <a name="remarks"></a>Bemerkungen

Eine **MAPIUID** -Struktur ist eine **GUID** -Struktur, die in die Bytereihenfolge der Intel ® processors eingefügt wird. 
  
MAPI erstellt **MAPIUID** -Strukturen so, dass es sehr selten ist, dass zwei verschiedene Elemente denselben Bezeichner aufweisen. **MAPIUID** -Strukturen können als binäre Eigenschaften oder als Dateien gespeichert werden, unabhängig von der Bytereihenfolge des Computers, auf dem Informationen gespeichert werden. 
  
 **MAPIUID** -Strukturen werden verwendet: 
  
- , Um einen Profil Abschnitt zu identifizieren.
    
- In den Eintrags Bezeichnern von Nachrichtenspeicher-und Adressbuch Objekten, um den Verantwortlichen Dienstanbieter zu identifizieren.
    
- In der **PR_SEARCH_KEY** ([pidtagsearchkey (](pidtagsearchkey-canonical-property.md))-Eigenschaft von Nachrichten.
    
Um einen **MAPIUID** -Bezeichner für einen Suchschlüssel zu generieren, rufen Dienstanbieter [IMAPISupport:: NewUID](imapisupport-newuid.md)auf.
  
Wenn ein Client eine Nachricht über ein Netzwerk übermittelt, sollte Sie ein Protokoll-oder Übertragungsformat verwenden, das die Bytereihenfolge der **MAPIUID** -Daten nicht ändert. 
  
Weitere Informationen zur Verwendung von **MAPIUID** -Strukturen finden Sie in den folgenden Themen: 
  
[Registrieren von eindeutigen Bezeichnern des Dienstanbieters](registering-service-provider-unique-identifiers.md)
  
[Festlegen des Transport Auftrags](setting-transport-order.md)
  
## <a name="see-also"></a>Siehe auch



[GUID](guid.md)
  
[IMAPISession::OpenProfileSection](imapisession-openprofilesection.md)
  
[IMAPISupport::NewUID](imapisupport-newuid.md)


[MAPI-Strukturen](mapi-structures.md)

