---
title: ADRLIST
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- ADRLIST
api_type:
- COM
ms.assetid: 85f0d8a5-6dd3-4f33-b31a-246d286d6286
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 2fdcc3d343eaabf0b34ae9e82099f9c467772868
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59572123"
---
# <a name="adrlist"></a>ADRLIST

**Gilt für**: Outlook 2013 | Outlook 2016 
  
Beschreibt null oder mehr Eigenschaften, die zu einem oder mehreren Empfängern gehören. 
  
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
  
> Anzahl der Einträge im Array, das durch das **Element aEntries** angegeben wird. 
    
**aEntries**
  
> Array von [ADRENTRY-Strukturen,](adrentry.md) eine Struktur für jeden Empfänger. 
    
## <a name="remarks"></a>HinwBemerkungeneise

Eine **ADRLIST-Struktur** enthält eine oder mehrere **ADRENTRY-Strukturen,** die jeweils die Eigenschaften eines Empfängers beschreiben. Ein Empfänger kann nicht aufgelöst werden. Dies bedeutet, dass ein Eintragsbezeichner in seinem Array von Eigenschaftswerten nicht vorhanden ist. Ein aufgelöster Empfänger bedeutet, dass die **PR \_ ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) -Eigenschaft enthalten ist. In der Regel verfügen aufgelöste Empfänger auch über eine E-Mail-Adresse der **eigenschaft PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)). Die E-Mail-Adresse ist jedoch nicht erforderlich. **ADRLIST-Strukturen** werden beispielsweise verwendet, um die Empfängerliste für eine ausgehende Nachricht zu beschreiben, und von MAPI, um die Einträge im Adressbuch anzuzeigen. 
  
**ADRLIST-Strukturen** ähneln [SRowSet-Strukturen,](srowset.md) die zum Darstellen von Zeilen in Tabellen verwendet werden. Tatsächlich sind diese beiden Strukturen so konzipiert, dass sie austauschbar verwendet werden können. Beide enthalten ein Array von Strukturen, die eine Gruppe von Eigenschaften beschreiben, und eine Anzahl der Werte im Array. Während in der **ADRLIST-Struktur** das Array [ADRENTRY-Strukturen](adrentry.md) enthält, enthält das Array in der **SRowSet-Struktur** [SRow-Strukturen.](srow.md) **ADRENTRY-Strukturen** und **SRow-Strukturen** sind im Layout identisch. Da **ADRLIST-** und **SRowSet-Strukturen** den gleichen Zuordnungsregeln folgen, kann eine **SRowSet-Struktur,** die aus dem Inhaltsverzeichnis eines Adressbuchcontainers abgerufen wird, in eine **ADRLIST-Struktur** umgewandelt und unverändert verwendet werden. 
  
Die folgende Abbildung zeigt das Layout einer **ADRLIST-Struktur.** 
  
**ADRLIST-Komponenten**
  
![ADRLIST-Komponenten](media/amapi_18.gif "ADRLIST-Komponenten")
  
Die **ADRENTRY-** und [SPropValue-Teile](spropvalue.md) in einer **ADRLIST-Struktur** müssen unabhängig von den anderen Teilen zugewiesen und freigegeben werden. Das heißt, jede **SPropValue-Struktur** muss einzeln zugewiesen werden, nachdem Speicher für die **ADRENTRY-Struktur** zugewiesen und freigegeben wurde, bevor die **ADRENTRY-Struktur** freigegeben wird. Diese Eigenständigkeit bei der Verarbeitung des Arbeitsspeichers ermöglicht es Empfängern und einzelnen Empfängereigenschaften, der Adressliste frei hinzugefügt oder aus ihr gelöscht zu werden. 
  
Die [FUNKTIONEN MAPIAllocateBuffer](mapiallocatebuffer.md) und [MAPIFreeBuffer](mapifreebuffer.md) müssen verwendet werden, um die **ADRLIST-Struktur** und alle ihre Teile zuzuordnen und freizugeben. 
  
Wenn eine Empfängerliste zu groß ist, um in den Arbeitsspeicher zu passen, können Clients die [IMessage::ModifyRecipients-Methode](imessage-modifyrecipients.md) aufrufen, um mit einer Teilmenge der Liste zu arbeiten. Clients sollten in dieser Situation keine allgemeinen Dialogfelder des Adressbuchs verwenden. 
  
Weitere Informationen zum Zuordnen von Speicher für **ADRENTRY-Strukturen** finden Sie unter [Managing Memory for ADRLIST and SRowSet Structures](managing-memory-for-adrlist-and-srowset-structures.md). 
  
## <a name="see-also"></a>Siehe auch

- [ADRENTRY](adrentry.md)  
- [CbNewADRLIST](cbnewadrlist.md) 
- [IMessage::ModifyRecipients](imessage-modifyrecipients.md) 
- [SRowSet](srowset.md)
- [MAPI-Strukturen](mapi-structures.md)

