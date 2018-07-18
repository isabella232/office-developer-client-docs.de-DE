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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: c6726b852176fa31bf879b5a32b63c35ce2be514
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791587"
---
# <a name="dtblcheckbox"></a>DTBLCHECKBOX

  
  
**Betrifft**: Outlook 
  
Enthält Informationen über ein Kontrollkästchen, die in einem Dialogfeld erstellt aus einer Tabelle anzeigen verwendet werden. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapidefs.h  <br/> |
|Verwandte Makro:  <br/> |[SizedDtblCheckBox](sizeddtblcheckbox.md) <br/> |
   
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
  
> Die Position im Speicher der Zeichenfolge, die das Kontrollkästchen angezeigt wird. 
    
 **ulFlags**
  
> Bitmaske aus Flags verwendet, um das Format der Beschriftung des Kontrollkästchens festzulegen. Das folgende Flag kann festgelegt werden:
    
PARAMETER MAPI_UNICODE 
  
> Die Beschriftung wird im Unicode-Format. Wenn die Option MAPI_UNICODE nicht festgelegt ist, ist die Bezeichnung im ANSI-Format.
    
 **ulPRPropertyName**
  
> Eigenschaftentag für eine Eigenschaft vom Typ PT_BOOLEAN. Der Wert dieser Eigenschaft wird von den Status des Kontrollkästchens beeinflusst.
    
## <a name="remarks"></a>Bemerkungen

Eine Struktur **DTBLCHECKBOX** beschreibt ein Kontrollkästchen ein Steuerelement, das einen von zwei Status widerspiegelt: (aktivierte Kontrollkästchen) aktiviert oder deaktiviert (ein leeres Feld). 
  
Der **UlPRPropertyName** -Member beschreibt eine boolesche Eigenschaft, deren Wert bearbeitet wird, indem Sie den Status des Kontrollkästchens ändern. Wenn das Kontrollkästchen zuerst angezeigt wird, ruft MAPI die **GetProps** -Methode der **IMAPIProp** -Implementierung, die die Tabelle anzeigen zum Abrufen von Standardeigenschaften zugeordnet ist. Wenn eine der Eigenschaften in der Struktur **DTBLCHECKBOX** das Eigenschafts-Tag zugeordnet ist, wird der Wert für diese Eigenschaft als Anfangswert das Kontrollkästchen angezeigt. 
  
Kontrollkästchen-Steuerelementen können geändert werden. Dies ermöglicht einem Benutzer, ändert sich ihr Status. Änderbare Kontrollkästchen legen Sie das DT_EDITABLE-Flag im **UlCtlFlags** Mitglied ihrer [DTCTL](dtctl.md) Struktur und in ihre **PR_CONTROL_FLAGS** ([PidTagControlFlags](pidtagcontrolflags-canonical-property.md))-Eigenschaft. Wenn Sie den Zustand ein Kontrollkästchens geändert wird, ruft MAPI [IMAPIProp::SetProps](imapiprop-setprops.md) zum Festlegen der Eigenschaft in der Eigenschaft Tag Member der Struktur in den neuen Zustand **DTBLCHECKBOX** identifiziert. 
  
Adressbuch-Dienstanbieter kann beispielsweise eine änderbare Kontrollkästchen-Steuerelement im Dialogfeld Konfiguration die Einstellung der Eigenschaft für einen Empfänger **PR_SEND_RICH_INFO** ([PidTagSendRichInfo](pidtagsendrichinfo-canonical-property.md)) anpassen enthalten. Wenn der Benutzer das Kontrollkästchen auswählt, wird diese Eigenschaft von MAPI auf TRUE festgelegt. Wenn das Kontrollkästchen deaktiviert ist, wird die Eigenschaft auf FALSE festgelegt.
  
Eine Übersicht über die Anzeige Tabellen finden Sie unter [Tabellen angezeigt](display-tables.md). Informationen zum Implementieren einer Tabelle anzeigen finden Sie unter [Implementieren einer Tabelle anzuzeigen](display-table-implementation.md). Informationen zu Eigenschaftstypen finden Sie unter [MAPI-Eigenschaft Type Overview](mapi-property-type-overview.md).
  
## <a name="see-also"></a>Siehe auch



[DTCTL](dtctl.md)
  
[PidTagControlType (kanonische Eigenschaft)](pidtagcontroltype-canonical-property.md)


[MAPI-Strukturen](mapi-structures.md)

