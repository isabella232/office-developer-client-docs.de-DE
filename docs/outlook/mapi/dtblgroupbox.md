---
title: DTBLGROUPBOX
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.DTBLGROUPBOX
api_type:
- COM
ms.assetid: 5e444b62-d6b6-4cfc-8601-d34aa004c1e6
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 43aeba3be0181b4e5f5a203e7d1e4d0a64ec2bbd
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59601121"
---
# <a name="dtblgroupbox"></a>DTBLGROUPBOX

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Beschreibt ein Gruppenfeld-Steuerelement, das in einem Dialogfeld verwendet wird, das aus einer Anzeigetabelle erstellt wurde.
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapidefs.h  <br/> |
|Verwandtes Makro:  <br/> |[SizedDtblGroupBox](sizeddtblgroupbox.md) <br/> |
   
```cpp
typedef struct _DTBLGROUPBOX
{
  ULONG ulbLpszLabel;
  ULONG ulFlags;
} DTBLGROUPBOX, FAR *LPDTBLGROUPBOX;

```

## <a name="members"></a>Members

 **ulbLpszLabel**
  
> Position im Speicher der Zeichenzeichenfolge, die das Gruppenfeld begleitet. Wenn die Bezeichnung angezeigt wird, wird sie auf der linken oberen Seite des Felds angezeigt.
    
 **ulFlags**
  
> Bitmaske von Flags, die zum Festlegen des Formats der Bezeichnung verwendet werden, auf die vom **ulbLpszLabel-Element** verwiesen wird. Das folgende Kennzeichen kann festgelegt werden: 
    
MAPI_UNICODE 
  
> Die Beschriftung hat das Unicode-Format. Wenn das MAPI_UNICODE-Kennzeichen nicht festgelegt ist, hat die Bezeichnung das ANSI-Format.
    
## <a name="remarks"></a>HinwBemerkungeneise

Eine **DTBLGROUPBOX-Struktur** beschreibt ein Gruppenfeld-Steuerelement, das verwendet wird, um andere Steuerelemente im Dialogfeld visuell zuzuordnen. Die Hervorhebungstechnik umfasst die Umrandung der anderen Steuerelemente durch ein Feld. 
  
Eine Übersicht über Anzeigetabellen finden Sie unter ["Anzeigetabellen".](display-tables.md) Informationen zum Implementieren einer Anzeigetabelle finden Sie unter [Implementieren einer Anzeigetabelle.](display-table-implementation.md)
  
## <a name="see-also"></a>Siehe auch



[DTCTL](dtctl.md)


[MAPI-Strukturen](mapi-structures.md)

