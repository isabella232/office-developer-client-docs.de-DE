---
title: SizedENTRYID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.SizedENTRYID
api_type:
- COM
ms.assetid: 491170af-db35-4d7e-a912-44ffe8c7506b
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 551c230ebf203bab702b8d7ba9dbc57aeb97d130
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59566605"
---
# <a name="sizedentryid"></a>SizedENTRYID

**Gilt für**: Outlook 2013 | Outlook 2016 
  
Erstellt eine benannte [ENTRYID-Struktur,](entryid.md) die ein **Ab-Element** einer angegebenen Größe enthält. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapidefs.h  <br/> |
|Verwandte Struktur:  <br/> |**ENTRYID** <br/> |
   
```cpp
SizedENTRYID (_cb, _name)
```

## <a name="parameters"></a>Parameter

_ _cb_
  
> Anzahl der Bytes im **Ab-Element** der neuen Struktur. 
    
_ _Name_
  
> Name für die neue Struktur.
    
## <a name="remarks"></a>HinwBemerkungeneise

Mit dem Makro **SizeENTRYID** können Sie einen Eintragsbezeichner definieren, nachdem Anforderungen für die Arraylänge bekannt sind. Verwenden Sie dieses Makro, um einen Eintragsbezeichner mit expliziten Grenzen zu erstellen. 
  
Führen Sie die folgende Umwandlung aus, um die neue Struktur zu verwenden, die aus dem Makro **SizeENTRYID** als Zeiger auf eine **ENTRYID-Struktur** resultiert: 
  
```cpp
lpENTRYID = (LPENTRYID) &SizedENTRYID;

```

## <a name="see-also"></a>Siehe auch

- [ENTRYID](entryid.md)
- [Makros im Zusammenhang mit Strukturen](macros-related-to-structures.md)

