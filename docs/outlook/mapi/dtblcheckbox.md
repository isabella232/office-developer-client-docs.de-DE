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
ms.openlocfilehash: ed0bbe986f374648e2ee85f3a0d2dfe7bc392e0f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32287269"
---
# <a name="dtblcheckbox"></a>DTBLCHECKBOX

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält Informationen zu einem Kontrollkästchen, das in einem von einer Anzeigetabelle erstellten Dialogfeldverwendet wird. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapidefs. h  <br/> |
|Zugehöriges Makro:  <br/> |[SizedDtblCheckBox](sizeddtblcheckbox.md) <br/> |
   
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
  
> Position im Arbeitsspeicher der Zeichenfolge, die mit dem Kontrollkästchen angezeigt wird. 
    
 **ulFlags**
  
> Bitmaske von Flags, die zum Festlegen des Formats der Kontrollkästchenbeschriftung verwendet werden. Das folgende Flag kann festgelegt werden:
    
MAPI_UNICODE 
  
> Die Bezeichnung ist im Unicode-Format. Wenn das MAPI_UNICODE-Flag nicht festgelegt ist, ist die Bezeichnung im ANSI-Format.
    
 **ulPRPropertyName**
  
> Property-Tag für eine Eigenschaft vom Typ PT_BOOLEAN. Der Wert dieser Eigenschaft hängt vom Status des Kontrollkästchens ab.
    
## <a name="remarks"></a>Bemerkungen

Eine **DTBLCHECKBOX** -Struktur beschreibt ein Kontrollkästchen ein Steuerelement, das einen der beiden Zustände widerspiegelt: Enabled (ein aktiviertes Kontrollkästchen) oder deaktiviert (ein leeres Feld). 
  
Das **ulPRPropertyName** -Element beschreibt eine boolesche Eigenschaft, deren Wert durch Ändern des Status des Kontrollkästchens geändert wird. Wenn das Kontrollkästchen zuerst angezeigt wird, ruft MAPI die **** GetProps-Methode der **IMAPIProp** -Implementierung auf, die der Anzeigetabelle zugeordnet ist, um einen Satz von Standardeigenschaften abzurufen. Wenn eine der Eigenschaften dem Property-Tag in der **DTBLCHECKBOX** -Struktur zugeordnet ist, wird der Wert für diese Eigenschaft als Anfangswert des Kontrollkästchens angezeigt. 
  
Kontrollkästchen-Steuerelemente können geändert werden. Dadurch kann ein Benutzer seine Status ändern. Veränderbare Kontrollkästchen legen Sie das DT_EDITABLE-Flag im **ulCtlFlags** -Element ihrer [DTCTL](dtctl.md) -Struktur und in Ihrer **PR_CONTROL_FLAGS** ([pidtagcontrolflags (](pidtagcontrolflags-canonical-property.md))-Eigenschaft fest. Wenn ein Kontrollkästchen seinen Status ändert, ruft MAPI [IMAPIProp::](imapiprop-setprops.md) SetProps auf, um die im Property-Tag-Element der **DTBLCHECKBOX** -Struktur angegebene Eigenschaft auf den neuen Status festzulegen. 
  
Ein Adressbuchanbieter kann beispielsweise ein änderbares Kontrollkästchen-Steuerelement in sein Konfigurationsdialogfeld aufnehmen, um die Einstellung der **PR_SEND_RICH_INFO** ([pidtagsendrichinfo (](pidtagsendrichinfo-canonical-property.md))-Eigenschaft eines Empfängers anzupassen. Wenn der Benutzer das Kontrollkästchen aktiviert, wird diese Eigenschaft von MAPI auf TRUE festgelegt. Wenn das Kontrollkästchen deaktiviert ist, wird die Eigenschaft auf FALSE festgelegt.
  
Eine Übersicht über Anzeige Tabellen finden Sie unter [Display Tables](display-tables.md). Weitere Informationen zum Implementieren einer Anzeigetabelle finden Sie unter [Implementieren einer Anzeigetabelle](display-table-implementation.md). Weitere Informationen zu Eigenschaftstypen finden Sie unter [MAPI property Type Overview](mapi-property-type-overview.md).
  
## <a name="see-also"></a>Siehe auch



[DTCTL](dtctl.md)
  
[Kanonische Pidtagcontroltype (-Eigenschaft](pidtagcontroltype-canonical-property.md)


[MAPI-Strukturen](mapi-structures.md)

