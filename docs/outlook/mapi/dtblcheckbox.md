---
title: DTBLCHECKBOX
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.DTBLCHECKBOX
api_type:
- COM
ms.assetid: 0dd12990-5431-4768-9d64-27d4ef6b7b20
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: ed0bbe986f374648e2ee85f3a0d2dfe7bc392e0f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436832"
---
# <a name="dtblcheckbox"></a>DTBLCHECKBOX

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält Informationen zu einem Kontrollkästchen, das in einem Dialogfeld verwendet wird, das aus einer Anzeigetabelle erstellt wird. 
  
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

## <a name="members"></a>Elemente

 **ulbLpszLabel**
  
> Position im Arbeitsspeicher der Zeichenzeichenfolge, die mit dem Kontrollkästchen angezeigt wird. 
    
 **ulFlags**
  
> Bitmaske von Flags, die zum Festlegen des Formats der Kontrollkästchenbeschriftung verwendet werden. Das folgende Flag kann festgelegt werden:
    
MAPI_UNICODE 
  
> Die Bezeichnung ist im Unicode-Format. Wenn das MAPI_UNICODE nicht festgelegt ist, befindet sich die Bezeichnung im ANSI-Format.
    
 **ulPRPropertyName**
  
> Eigenschaftstag für eine Eigenschaft vom Typ PT_BOOLEAN. Der Wert dieser Eigenschaft wird vom Status des Kontrollkästchens beeinflusst.
    
## <a name="remarks"></a>Hinweise

Eine **DTBLCHECKBOX-Struktur** beschreibt ein Kontrollkästchen eines Steuerelements, das einen der beiden Zustände widerspiegelt: aktiviert (ein aktiviertes Kontrollkästchen) oder deaktiviert (ein leeres Feld). 
  
Das **UlPRPropertyName-Element** beschreibt eine boolesche Eigenschaft, deren Wert durch Ändern des Status des Kontrollkästchens geändert wird. Wenn das Kontrollkästchen zum ersten Mal angezeigt wird, ruft MAPI die **GetProps-Methode** der **IMAPIProp-Implementierung** auf, die der Anzeigetabelle zugeordnet ist, um eine Reihe von Standardeigenschaften abzurufen. Wenn eine der Eigenschaften dem Eigenschaftstag in der **DTBLCHECKBOX-Struktur** zu ordnet, wird der Wert für diese Eigenschaft als Anfangswert des Kontrollkästchens angezeigt. 
  
Kontrollkästchensteuerelemente können geändert werden. Dadurch kann ein Benutzer seine Zustände ändern. Modifizierbare Kontrollkästchen legen das DT_EDITABLE-Flag im **ulCtlFlags-Element** der [DTCTL-Struktur](dtctl.md) und in der **PR_CONTROL_FLAGS** ([PidTagControlFlags](pidtagcontrolflags-canonical-property.md)) -Eigenschaft. Wenn ein Kontrollkästchen seinen Status ändert, ruft MAPI [IMAPIProp::SetProps](imapiprop-setprops.md) auf, um die im Eigenschaftstagm member der **DTBLCHECKBOX-Struktur** identifizierte Eigenschaft auf den neuen Zustand zu setzen. 
  
Ein **Adressbuchanbieter** kann z. B. ein modifizierbares Kontrollkästchensteuerelement in sein Konfigurationsdialogfeld hinzufügen, um die Einstellung der PR_SEND_RICH_INFO ([PidTagSendRichInfo](pidtagsendrichinfo-canonical-property.md))-Eigenschaft eines Empfängers anzupassen. Wenn der Benutzer das Kontrollkästchen auswählt, legt MAPI diese Eigenschaft auf TRUE fest. Wenn das Kontrollkästchen deaktiviert ist, wird die Eigenschaft auf FALSE festgelegt.
  
Eine Übersicht über Anzeigetabellen finden Sie unter [Display Tables](display-tables.md). Informationen zum Implementieren einer Anzeigetabelle finden Sie unter [Implementieren einer Anzeigetabelle](display-table-implementation.md). Informationen zu Eigenschaftstypen finden Sie unter [MAPI Property Type Overview](mapi-property-type-overview.md).
  
## <a name="see-also"></a>Siehe auch



[DTCTL](dtctl.md)
  
[PidTagControlType (kanonische Eigenschaft)](pidtagcontroltype-canonical-property.md)


[MAPI-Strukturen](mapi-structures.md)

