---
title: SizedADRLIST
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SizedADRLIST
api_type:
- COM
ms.assetid: 5c64d74a-83a7-4122-b1d1-fcca0f4a6cdb
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: c35a1eb54b29c04bc8eed453272b59aae0ea737e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32282775"
---
# <a name="sizedadrlist"></a>SizedADRLIST

**Gilt für**: Outlook 2013 | Outlook 2016 
  
Definiert eine [ADRLIST](adrlist.md) -Struktur mit dem angegebenen Namen, die eine bestimmte Anzahl von [Miet](adrentry.md) Strukturen enthält. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapidefs. h  <br/> |
|Zugehörige Struktur:  <br/> |**ADRLIST** <br/> |
   
```cpp
SizedADRLIST (_centries,_name)
```

## <a name="parameters"></a>Parameter

__Zentrierungen_
  
> Die Anzahl der **Miet** Strukturen, die in die neue **ADRLIST** -Struktur eingeschlossen werden sollen. 
    
__Name_
  
> Name für die neue **ADRLIST** -Struktur. 
    
## <a name="remarks"></a>Bemerkungen

Mit dem **SizedADRLIST** -Makro können Sie eine Empfängerliste mit expliziten Grenzen definieren, wenn die Anforderungen an die Arraylänge bekannt sind. Der folgende Code zeigt, wie das Ergebnis des **SizedADRLIST** -Makros in einen **ADRLIST** -Struktur Zeiger umgewandelt wird: 
  
```cpp
lpADRList = (LPADRLIST) &SizedADRList;
```

## <a name="see-also"></a>Siehe auch

- [ADRLIST](adrlist.md)
- [ADRENTRY](adrentry.md)
- [Makros im Zusammenhang mit Strukturen](macros-related-to-structures.md)

