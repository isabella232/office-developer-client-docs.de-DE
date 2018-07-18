---
title: ADRENTRY
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ADRENTRY
api_type:
- COM
ms.assetid: 5fa091a4-3a84-4881-91b3-e34fd9ca6f38
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 4b6f850c8f88088863b37bd94de6b1f3d4c48d4f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/15/2018
ms.locfileid: "19791292"
---
# <a name="adrentry"></a>ADRENTRY

  
  
**Betrifft**: Outlook 
  
NULL oder mehrere Eigenschaften, die an einen Empfänger gehören beschrieben.
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapidefs.h  <br/> |
   
```cpp
typedef struct _ADRENTRY
{
  ULONG ulReserved1;
  ULONG cValues;
  LPSPropValue rgPropVals;
} ADRENTRY, FAR *LPADRENTRY;

```

## <a name="members"></a>Elemente

 **ulReserved1**
  
> Reserviert. NULL muss sein.
    
 **cValues**
  
> Anzahl der Eigenschaften im Array Wert-Eigenschaft auf den vom **RgPropVals** Member verwiesen. Der **cValues** -Member kann 0 (null) sein. 
    
 **rgPropVals**
  
> Zeiger auf ein Wertearray-Eigenschaft, beschreibt die Eigenschaften für den Empfänger. Der **RgPropVals** -Member kann NULL sein. 
    
## <a name="remarks"></a>Bemerkungen

Eine Struktur **ADRENTRY** beschreibt die Eigenschaften, die an einen einzelnen Empfänger gehören. Die folgenden: Eigenschaften, die in der Regel verwendet werden, um einen Empfänger zu beschreiben 
  
 **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))
  
 **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))
  
 **PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))
  
 **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))
  
Wenn eine Eintrags-ID oder **PR_ENTRYID** -Eigenschaft im Array [SPropValue](spropvalue.md) für einen Empfänger angezeigt wird, bedeutet dies, dass der Empfänger aufgelöst wurde. Clients rufen Sie die [IAddrBook::ResolveName](iaddrbook-resolvename.md) -Methode, um sicherzustellen, dass alle Empfänger in der Empfängerliste von ausgehenden Nachrichten behoben wurden. Nur aufgelösten Empfänger können mit Nachrichten gesendet werden. 
  
 **ADRENTRY** Strukturen werden in der Regel kombiniert, um ein Array für das **aEntries** Mitglied einer [ADRLIST](adrlist.md) -Struktur zu bilden. 
  
 **ADRENTRY** Strukturen und [SRow](srow.md) Strukturen sind identisch, da beide Mitglied reserviert, ein Array von Eigenschaftswerten und die Anzahl der Werte im Array enthalten. Während **ADRENTRY** Strukturen kombiniert werden, um das **aEntries** Mitglied einer **ADRLIST** -Struktur zu bilden, werden **SRow** Strukturen kombiniert, um die **aRow** Mitglied einer [SRowSet](srowset.md) Struktur bilden. Beide Arten von Strukturen führen Sie die gleichen Allocation-Regeln, sagen, dass eine **SRowSet** -Struktur, die aus der Inhaltstabelle einer Adressbuchcontainer abgerufen wird auf eine **ADRLIST** -Struktur umgewandelt und verwendet werden kann. 
  
Eine Struktur **ADRENTRY** kann leer sein. Beispielsweise kann eine **ADRENTRY** -Struktur, die in der **ADRLIST** -Struktur, die auf das durch den Parameter _LppAdrList_ in einem Aufruf von **IAddrBook::Address** enthalten ist leer sein, wenn ein Empfänger entfernt wird. 
  
Weitere Informationen zur Verwendung von Arbeitsspeicher für **ADRENTRY** Strukturen, finden Sie unter [Verwalten von Arbeitsspeicher für ADRLIST und SRowSet Strukturen](managing-memory-for-adrlist-and-srowset-structures.md).
  
## <a name="see-also"></a>Siehe auch



[IAddrBook::Address](iaddrbook-address.md)
  
[IMessage::ModifyRecipients](imessage-modifyrecipients.md)
  
[MAPIAllocateBuffer](mapiallocatebuffer.md)
  
[ADRLIST](adrlist.md)
  
[SRow](srow.md)
  
[SRowSet](srowset.md)


[MAPI-Strukturen](mapi-structures.md)

