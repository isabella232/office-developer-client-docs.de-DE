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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 319c932862615e063a02ffac07e5541b1b20ac7e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415915"
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

## <a name="members"></a>Elemente

**cEntries**
  
> Anzahl der Einträge im vom **aEntries-Element angegebenen** Array. 
    
**aEntries**
  
> Array von [ADRENTRY-Strukturen,](adrentry.md) eine Struktur für jeden Empfänger. 
    
## <a name="remarks"></a>Hinweise

Eine **ADRLIST-Struktur** enthält eine oder mehrere **ADRENTRY-Strukturen,** die jeweils die Eigenschaften eines Empfängers beschreiben. Ein Empfänger kann nicht aufgelöst werden. Dies bedeutet, dass ihm ein Eintragsbezeichner im Array der Eigenschaftswerte fehlt. Ein aufgelöster Empfänger bedeutet, dass die **PR \_ ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) -Eigenschaft enthalten ist. In der Regel verfügen aufgelöste Empfänger auch über eine E-Mail-Adresse PR_EMAIL_ADDRESS **(** [PidTagEmailAddress](pidtagemailaddress-canonical-property.md)) -Eigenschaft. Die E-Mail-Adresse ist jedoch nicht erforderlich. **ADRLIST-Strukturen** werden z. B. verwendet, um die Empfängerliste für eine ausgehende Nachricht und die MAPI zu beschreiben, um die Einträge im Adressbuch anzuzeigen. 
  
**ADRLIST-Strukturen** ähneln [SRowSet-Strukturen,](srowset.md) die zum Darstellen von Zeilen in Tabellen verwendet werden. Tatsächlich sind diese beiden Strukturen so konzipiert, dass sie austauschbar verwendet werden können. Beide enthalten ein Array von Strukturen, die eine Gruppe von Eigenschaften beschreiben, und eine Anzahl der Werte im Array. Während das Array in der **ADRLIST-Struktur** [ADRENTRY-Strukturen](adrentry.md) enthält, enthält das Array in der **SRowSet-Struktur** [SRow-Strukturen.](srow.md) **ADRENTRY-Strukturen** und **SRow-Strukturen** sind im Layout identisch. Da **ADRLIST-** und **SRowSet-Strukturen** dieselben Zuweisungsregeln befolgen, kann eine **SRowSet-Struktur,** die aus dem Inhaltsverzeichnis eines Adressbuchcontainers abgerufen wird, in eine **ADRLIST-Struktur** umstrukturiert und wie gewohnt verwendet werden. 
  
Die folgende Abbildung zeigt das Layout einer **ADRLIST-Struktur.** 
  
**ADRLIST-Komponenten**
  
![ADRLIST-Komponenten](media/amapi_18.gif "ADRLIST-Komponenten")
  
Die **TEILE ADRENTRY** und [SPropValue](spropvalue.md) in einer **ADRLIST-Struktur** müssen unabhängig von den anderen Teilen zugewiesen und frei werden. Das heißt, jede **SPropValue-Struktur** muss einzeln zugewiesen werden, nachdem der Arbeitsspeicher für die **ADRENTRY-Struktur** zugewiesen und frei wird, bevor die **ADRENTRY-Struktur** frei wird. Diese Unabhängigkeit beim Behandeln des Arbeitsspeichers ermöglicht es Empfängern und einzelnen Empfängereigenschaften, frei aus der Adressliste hinzugefügt oder gelöscht zu werden. 
  
Die [Funktionen MAPIAllocateBuffer](mapiallocatebuffer.md) und [MAPIFreeBuffer](mapifreebuffer.md) müssen verwendet werden, um die **ADRLIST-Struktur** und alle ihre Teile zuzuordnen und frei zu geben. 
  
Wenn eine Empfängerliste zu groß ist, um in den Arbeitsspeicher zu passen, können Clients die [IMessage::ModifyRecipients-Methode](imessage-modifyrecipients.md) aufrufen, um mit einer Teilmenge der Liste zu arbeiten. Clients sollten in dieser Situation nicht die allgemeinen Dialogfelder des Adressbuchs verwenden. 
  
Weitere Informationen zum Zuordnen von Arbeitsspeicher für **ADRENTRY-Strukturen** finden Sie unter [Managing Memory for ADRLIST and SRowSet Structures](managing-memory-for-adrlist-and-srowset-structures.md). 
  
## <a name="see-also"></a>Siehe auch

- [ADRENTRY](adrentry.md)  
- [CbNewADRLIST](cbnewadrlist.md) 
- [IMessage::ModifyRecipients](imessage-modifyrecipients.md) 
- [SRowSet](srowset.md)
- [MAPI-Strukturen](mapi-structures.md)

