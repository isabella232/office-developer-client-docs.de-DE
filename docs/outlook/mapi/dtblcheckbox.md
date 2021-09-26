---
title: DTBLCHECKBOX
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.DTBLCHECKBOX
api_type:
- COM
ms.assetid: 0dd12990-5431-4768-9d64-27d4ef6b7b20
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 60bfb43f99ef6831ab7dda837924a00d9c3d94a6
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59630964"
---
# <a name="dtblcheckbox"></a>DTBLCHECKBOX

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält Informationen zu einem Kontrollkästchen, das in einem aus einer Anzeigetabelle erstellten Dialogfeld verwendet wird. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapidefs.h  <br/> |
|Verwandtes Makro:  <br/> |[SizedDtblCheckBox](sizeddtblcheckbox.md) <br/> |
   
```cpp
typedef struct _DTBLCHECKBOX
{
  ULONG ulbLpszLabel;
  ULONG ulFlags;
  ULONG ulPRPropertyName;
} DTBLCHECKBOX, FAR *LPDTBLCHECKBOX;

```

## <a name="members"></a>Members

 **ulbLpszLabel**
  
> Position im Speicher der Zeichenzeichenfolge, die mit dem Kontrollkästchen angezeigt wird. 
    
 **ulFlags**
  
> Bitmaske mit Kennzeichen, die zum Festlegen des Formats der Kontrollkästchenbeschriftung verwendet werden. Das folgende Kennzeichen kann festgelegt werden:
    
MAPI_UNICODE 
  
> Die Beschriftung hat das Unicode-Format. Wenn das MAPI_UNICODE-Kennzeichen nicht festgelegt ist, hat die Bezeichnung das ANSI-Format.
    
 **ulPRPropertyName**
  
> Eigenschaftstag für eine Eigenschaft vom Typ PT_BOOLEAN. Der Wert dieser Eigenschaft wird vom Status des Kontrollkästchens beeinflusst.
    
## <a name="remarks"></a>Bemerkungen

Eine **DTBLCHECKBOX-Struktur** beschreibt ein Kontrollkästchen eines Steuerelements, das einen von zwei Zuständen widerspiegelt: aktiviert (ein Kontrollkästchen) oder deaktiviert (ein leeres Kontrollkästchen). 
  
Der **ulPRPropertyName-Member** beschreibt eine boolesche Eigenschaft, deren Wert geändert wird, indem der Status des Kontrollkästchens geändert wird. Wenn das Kontrollkästchen zum ersten Mal angezeigt wird, ruft MAPI die **GetProps-Methode** der **IMAPIProp-Implementierung** auf, die der Anzeigetabelle zugeordnet ist, um einen Satz von Standardeigenschaften abzurufen. Wenn eine der Eigenschaften dem Eigenschaftentag in der **DTBLCHECKBOX-Struktur** zugeordnet ist, wird der Wert für diese Eigenschaft als Anfangswert des Kontrollkästchens angezeigt. 
  
Kontrollkästchen-Steuerelemente können modifizierbar sein. Dadurch kann ein Benutzer seine Zustände ändern. Modifiierbare Kontrollkästchen legen das DT_EDITABLE Flag im **ulCtlFlags-Element** der [DTCTL-Struktur](dtctl.md) und in der **PR_CONTROL_FLAGS** ([PidTagControlFlags](pidtagcontrolflags-canonical-property.md)) -Eigenschaft fest. Wenn ein Kontrollkästchen seinen Status ändert, ruft MAPI [IMAPIProp::SetProps](imapiprop-setprops.md) auf, um die im Eigenschaftstagelement der **DTBLCHECKBOX-Struktur** identifizierte Eigenschaft auf den neuen Status festzulegen. 
  
Beispielsweise kann ein Adressbuchanbieter ein änderbares Kontrollkästchen-Steuerelement in sein Konfigurationsdialogfeld einschließen, um die Einstellung der **Eigenschaft PR_SEND_RICH_INFO** ([PidTagSendRichInfo](pidtagsendrichinfo-canonical-property.md)) eines Empfängers anzupassen. Wenn der Benutzer das Kontrollkästchen auswählt, legt MAPI diese Eigenschaft auf TRUE fest. Wenn das Kontrollkästchen deaktiviert ist, wird die Eigenschaft auf FALSE festgelegt.
  
Eine Übersicht über Anzeigetabellen finden Sie unter ["Anzeigetabellen".](display-tables.md) Informationen zum Implementieren einer Anzeigetabelle finden Sie unter [Implementieren einer Anzeigetabelle.](display-table-implementation.md) Informationen zu Eigenschaftstypen finden Sie unter [MAPI Property Type Overview](mapi-property-type-overview.md).
  
## <a name="see-also"></a>Siehe auch



[DTCTL](dtctl.md)
  
[Kanonische PidTagControlType-Eigenschaft](pidtagcontroltype-canonical-property.md)


[MAPI-Strukturen](mapi-structures.md)

