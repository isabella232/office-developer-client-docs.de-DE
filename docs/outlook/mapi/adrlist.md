---
title: ADRLIST
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ADRLIST
api_type:
- COM
ms.assetid: 85f0d8a5-6dd3-4f33-b31a-246d286d6286
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: b2d3dce7835f92d9ad78f7d8837e655fdd8fd412
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791280"
---
# <a name="adrlist"></a>ADRLIST

**Betrifft**: Outlook 
  
Beschreibt NULL oder mehrere Eigenschaften, die einen oder mehrere Empfänger angehören. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapidefs.h  <br/> |
|Verwandte Makros:  <br/> |[CbADRLIST](cbadrlist.md), [CbNewADRLIST](cbnewadrlist.md), [CbNewADRLIST](cbnewadrlist.md) <br/> |
   
```cpp
typedef struct _ADRLIST
{
  ULONG cEntries;
  ADRENTRY aEntries[MAPI_DIM];
} ADRLIST, FAR *LPADRLIST;

```

## <a name="members"></a>Members

**cEntries**
  
> Anzahl der Einträge im Array vom **aEntries** Member angegeben. 
    
**aEntries**
  
> Array von [ADRENTRY](adrentry.md) Strukturen, eine Struktur für jeden Empfänger. 
    
## <a name="remarks"></a>Hinweise

Eine **ADRLIST** -Struktur enthält ein oder mehrere **ADRENTRY** Strukturen, die die Eigenschaften eines Empfängers beschreibt. Ein Empfänger kann nicht aufgelöst werden. Dies bedeutet, dass es einen Eintrag Bezeichner in dessen Array von Eigenschaftswerten fehlen. Ein aufgelöster Empfänger bedeutet, dass die **PR\_ENTRYID** -Eigenschaft ([PidTagEntryId](pidtagentryid-canonical-property.md)) enthalten ist. Außerdem müssen in der Regel aufgelösten Empfänger eine e-Mail-Adresse die **PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))-Eigenschaft. Die e-Mail-Adresse ist jedoch nicht erforderlich. **ADRLIST** -Strukturen, beispielsweise dienen zum Beschreiben der Empfängerliste für eine ausgehende Nachricht und MAPI, um die Einträge im Adressbuch anzuzeigen. 
  
**ADRLIST** -Strukturen so oder ähnlich aus [SRowSet](srowset.md) Strukturen Strukturen für das Darstellen von Zeilen in Tabellen verwendet. Diese zwei Strukturen dienen tatsächlich, damit sie austauschbar verwendet werden können. Beide enthalten ein Array von Strukturen, die eine Gruppe von Eigenschaften und die Anzahl der Werte im Array beschreibt. Während der **ADRLIST** -Struktur enthält das Array [ADRENTRY](adrentry.md) Strukturen, in der Struktur **SRowSet** das Array [SRow](srow.md) Strukturen enthält. **ADRENTRY** Strukturen und **SRow** Strukturen sind in Layout identisch. Da **ADRLIST** und **SRowSet** Strukturen dieselben Zuordnungsregeln zu befolgen, kann unverändert eine **SRowSet** -Struktur, die aus der Inhaltstabelle einer Adressbuchcontainer abgerufen wird auf eine **ADRLIST** -Struktur umgewandelt und verwendet werden. 
  
Die folgende Abbildung zeigt das Layout einer **ADRLIST** -Struktur. 
  
**ADRLIST-Komponenten**
  
![ADRLIST-Komponenten] (media/amapi_18.gif "ADRLIST-Komponenten")
  
Die Abschnitte **ADRENTRY** und [SPropValue](spropvalue.md) in einer **ADRLIST** müssen belegt und unabhängig von den anderen Teilen freigegeben werden. D. h., muss jede **SPropValue** Struktur einzeln zugeordnet werden, nachdem Speicher für die Struktur **ADRENTRY** zugewiesen wurde und freigegeben werden, bevor die Struktur **ADRENTRY** freigegeben wird. Diese Unabhängigkeit in die Behandlung von Speicher ermöglicht Empfänger und einzelne Empfängereigenschaften frei hinzugefügt oder aus der Adressliste gelöscht werden soll. 
  
Die Funktionen [MAPIAllocateBuffer](mapiallocatebuffer.md) und [MAPIFreeBuffer](mapifreebuffer.md) müssen zum Zuordnen und Freigeben der **ADRLIST** -Struktur und all seiner Teile verwendet werden. 
  
Wenn eine Empfängerliste zu groß im Arbeitsspeicher ist, können Clients die [IMessage::ModifyRecipients](imessage-modifyrecipients.md) -Methode eine Teilmenge der Liste entwickelt aufrufen. Clients sollten Address Book allgemeine Dialogfelder in dieser Situation nicht verwenden. 
  
Weitere Informationen zur Verwendung von Arbeitsspeicher für **ADRENTRY** Strukturen, finden Sie unter [Verwalten von Arbeitsspeicher für ADRLIST und SRowSet Strukturen](managing-memory-for-adrlist-and-srowset-structures.md). 
  
## <a name="see-also"></a>Siehe auch

- [ADRENTRY](adrentry.md)  
- [CbNewADRLIST](cbnewadrlist.md) 
- [IMessage::ModifyRecipients](imessage-modifyrecipients.md) 
- [' Srowset '](srowset.md)
- [MAPI-Strukturen](mapi-structures.md)

