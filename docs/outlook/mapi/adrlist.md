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
ms.openlocfilehash: 319c932862615e063a02ffac07e5541b1b20ac7e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32330244"
---
# <a name="adrlist"></a>ADRLIST

**Gilt für**: Outlook 2013 | Outlook 2016 
  
Beschreibt NULL oder mehr Eigenschaften, die zu einem oder mehreren Empfängern gehören. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapidefs. h  <br/> |
|Verwandte Makros:  <br/> |[CbADRLIST](cbadrlist.md), [CbNewADRLIST](cbnewadrlist.md), [CbNewADRLIST](cbnewadrlist.md) <br/> |
   
```cpp
typedef struct _ADRLIST
{
  ULONG cEntries;
  ADRENTRY aEntries[MAPI_DIM];
} ADRLIST, FAR *LPADRLIST;

```

## <a name="members"></a>Elemente

**Zentriert**
  
> Die Anzahl der Einträge im vom **aEntries** -Element angegebenen Array. 
    
**aEntries**
  
> Array von [Miet](adrentry.md) Strukturen, eine Struktur für jeden Empfänger. 
    
## <a name="remarks"></a>Bemerkungen

Eine **ADRLIST** -Struktur enthält eine oder mehrere **Miet** Strukturen, die jeweils die Eigenschaften eines Empfängers beschreiben. Ein Empfänger kann nicht aufgelöst werden. Dies bedeutet, dass es in seinem Array von Eigenschaftswerten keine Eintrags-ID gibt. Ein aufgelöster Empfänger bedeutet, dass die **\_PR** -Eintrags-Eigenschaft ([PidTagEntryId](pidtagentryid-canonical-property.md)) enthalten ist. In der Regel haben aufgelöste Empfänger auch eine e-Mail-Adresse der **PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))-Eigenschaft. Die e-Mail-Adresse ist jedoch nicht erforderlich. **ADRLIST** -Strukturen werden zum Beispiel verwendet, um die Empfängerliste für eine ausgehende Nachricht und MAPI zum Anzeigen der Einträge im Adressbuch zu beschreiben. 
  
**ADRLIST** -Strukturen ähneln [SRowSet](srowset.md) Strukturen der Strukturen für die Darstellung von Zeilen in Tabellen verwendet. Tatsächlich sind diese beiden Strukturen so konzipiert, dass Sie synonym verwendet werden können. Beide enthalten ein Array von Strukturen, die eine Gruppe von Eigenschaften und die Anzahl der Werte im Array beschreiben. Während in der **ADRLIST** -Struktur das Array die [Miet](adrentry.md) Strukturen enthält, enthält das Array in der **SRowSet** -Struktur [SRow](srow.md) -Strukturen. **Miet** Strukturen und **SRow** -Strukturen sind im Layout identisch. Da **ADRLIST** -und **SRowSet** -Strukturen denselben Zuordnungsregeln folgen, kann eine **SRowSet** -Struktur, die aus der Inhaltstabelle eines Adressbuch Containers abgerufen wird, in eine **ADRLIST** -Struktur umgewandelt und unverändert verwendet werden. 
  
Die folgende Abbildung zeigt das Layout einer **ADRLIST** -Struktur. 
  
**ADRLIST-Komponenten**
  
![ADRLIST-Komponenten] (media/amapi_18.gif "ADRLIST-Komponenten")
  
Die **Miet** -und [SPropValue](spropvalue.md) -Teile in einer **ADRLIST** -Struktur müssen unabhängig von den anderen Teilen reserviert und freigegeben werden. Das heißt, jede **SPropValue** -Struktur muss einzeln zugeordnet werden, nachdem der Speicher für die **Miet** Struktur reserviert und freigegeben wurde, bevor die **Miet** Struktur freigegeben wird. Durch diese Unabhängigkeit im Umgang mit Arbeitsspeicher können Empfänger und einzelne Empfänger Eigenschaften in der Adressliste frei hinzugefügt oder gelöscht werden. 
  
Die [MAPIAllocateBuffer](mapiallocatebuffer.md) -und [mapifreebufferfreigegeben](mapifreebuffer.md) -Funktionen müssen verwendet werden, um die **ADRLIST** -Struktur und alle zugehörigen Komponenten zuzuweisen und freizugeben. 
  
Wenn eine Empfängerliste zu umfangreich ist, um Sie in den Arbeitsspeicher zu integrieren, können Clients die [IMessage:: ModifyRecipients](imessage-modifyrecipients.md) -Methode aufrufen, um mit einer Teilmenge der Liste zu arbeiten. In dieser Situation sollten Clients nicht die allgemeinen Dialogfelder des Adressbuchs verwenden. 
  
Weitere Informationen zum Zuweisen von Arbeitsspeicher für **Miet** Strukturen finden Sie unter [Managing Memory for ADRLIST and SRowSet Structures](managing-memory-for-adrlist-and-srowset-structures.md). 
  
## <a name="see-also"></a>Siehe auch

- [ADRENTRY](adrentry.md)  
- [CbNewADRLIST](cbnewadrlist.md) 
- [IMessage::ModifyRecipients](imessage-modifyrecipients.md) 
- [SRowSet](srowset.md)
- [MAPI-Strukturen](mapi-structures.md)

