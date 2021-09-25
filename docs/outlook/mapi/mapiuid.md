---
title: MAPIUID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.MAPIUID
api_type:
- COM
ms.assetid: 63eac3ee-e59b-4a06-8bb9-f72764d84bda
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 807d517c2856c52ca47838f0927db44b0b7dda68
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59579466"
---
# <a name="mapiuid"></a>MAPIUID

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Eine bytereihenfolgeunabhängige Version einer [GUID-Struktur,](guid.md) die verwendet wird, um einen Dienstanbieter eindeutig zu identifizieren. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapidefs.h  <br/> |
|Verwandtes Makro:  <br/> |[IsEqualMAPIUID](isequalmapiuid.md) <br/> |
   
```cpp
typedef struct _MAPIUID
{
  BYTE ab[16];
} MAPIUID, FAR *LPMAPIUID;

```

## <a name="members"></a>Members

 **ab**
  
> Ein Array, das einen 16-Byte-Bezeichner enthält.
    
## <a name="remarks"></a>HinwBemerkungeneise

Eine **MAPIUID-Struktur** ist eine **GUID-Struktur,** die in Intel® Prozessorbytereihenfolge eingefügt wird. 
  
MAPI erstellt **MAPIUID-Strukturen** so, dass es sehr selten ist, dass zwei verschiedene Elemente denselben Bezeichner haben. **MAPIUID-Strukturen** können als binäre Eigenschaften oder als Dateien gespeichert werden, ohne Berücksichtigung der Bytereihenfolge des Computers, der die Informationen speichert oder darauf zugreift. 
  
 **MAPIUID-Strukturen** werden verwendet: 
  
- So identifizieren Sie einen Profilabschnitt.
    
- In den Eintragsbezeichnern von Nachrichtenspeicher- und Adressbuchobjekten, um den verantwortlichen Dienstanbieter zu identifizieren.
    
- In der **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)) -Eigenschaft von Nachrichten.
    
Um einen **MAPIUID-Bezeichner** für einen Suchschlüssel zu generieren, rufen Dienstanbieter [IMAPISupport::NewUID](imapisupport-newuid.md)auf.
  
Wenn ein Client eine Nachricht über ein Netzwerk überträgt, sollte er ein Protokoll- oder Übertragungsformat verwenden, das die Bytereihenfolge von **MAPIUID-Daten** nicht ändert. 
  
Weitere Informationen zur Verwendung von **MAPIUID-Strukturen** finden Sie in den folgenden Themen: 
  
[Registrieren eindeutiger Bezeichner des Dienstanbieters](registering-service-provider-unique-identifiers.md)
  
[Festlegen der Transportreihenfolge](setting-transport-order.md)
  
## <a name="see-also"></a>Siehe auch



[GUID](guid.md)
  
[IMAPISession::OpenProfileSection](imapisession-openprofilesection.md)
  
[IMAPISupport::NewUID](imapisupport-newuid.md)


[MAPI-Strukturen](mapi-structures.md)

