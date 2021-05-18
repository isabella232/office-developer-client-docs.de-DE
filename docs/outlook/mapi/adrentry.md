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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 36e0218c9e4e312a138bef7517242f74079212c4
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421438"
---
# <a name="adrentry"></a>ADRENTRY

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Beschreibt null oder mehr Eigenschaften, die zu einem Empfänger gehören.
  
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
  
> Reserviert; muss null sein.
    
 **cValues**
  
> Anzahl der Eigenschaften im Eigenschaftenwertarray, auf das das **rgPropVals-Element verweist.** Das **cValues-Element** kann null sein. 
    
 **rgPropVals**
  
> Zeiger auf ein Eigenschaftenwertarray, das die Eigenschaften für den Empfänger beschreibt. Das **rgPropVals-Element** kann NULL sein. 
    
## <a name="remarks"></a>Hinweise

Eine **ADRENTRY-Struktur** beschreibt Eigenschaften, die zu einem einzelnen Empfänger gehören. Zu den Eigenschaften, die in der Regel zur Beschreibung eines Empfängers verwendet werden, gehören die folgenden: 
  
 **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))
  
 **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))
  
 **PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))
  
 **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))
  
Wenn eine Eintrags-ID **oder PR_ENTRYID** im [SPropValue-Array](spropvalue.md) für einen Empfänger angezeigt wird, bedeutet dies, dass der Empfänger aufgelöst wurde. Clients rufen die [IAddrBook::ResolveName-Methode](iaddrbook-resolvename.md) auf, um sicherzustellen, dass alle Empfänger in der Empfängerliste einer ausgehenden Nachricht aufgelöst wurden. Nur aufgelöste Empfänger können mit Nachrichten gesendet werden. 
  
 **ADRENTRY-Strukturen** werden in der Regel kombiniert, um ein Array für das **aEntries-Mitglied** einer [ADRLIST-Struktur zu](adrlist.md) bilden. 
  
 **ADRENTRY-Strukturen** und [SRow-Strukturen](srow.md) sind identisch, da sie beide ein reserviertes Element, ein Array von Eigenschaftswerten und eine Anzahl von Werten im Array enthalten. Während **ADRENTRY-Strukturen** kombiniert werden, um das **aEntries-Mitglied** einer **ADRLIST-Struktur** zu bilden, werden **SRow-Strukturen** kombiniert, um das **aRow-Element** einer [SRowSet-Struktur zu](srowset.md) bilden. Beide Arten von Strukturen folgen denselben Zuweisungsregeln, was bedeutet, dass eine **SRowSet-Struktur,** die aus dem Inhaltsverzeichnis eines Adressbuchcontainers abgerufen wird, in eine **ADRLIST-Struktur** umstrukturiert und wie gewohnt verwendet werden kann. 
  
Eine **ADRENTRY-Struktur** kann leer sein. Beispielsweise kann eine **ADRENTRY-Struktur,** die in der **ADRLIST-Struktur** enthalten ist, auf die der  _lppAdrList-Parameter_ in einem Aufruf von **IAddrBook::Address** verweist, leer sein, wenn ein Empfänger entfernt wird. 
  
Weitere Informationen zum Zuordnen von Arbeitsspeicher für **ADRENTRY-Strukturen** finden Sie unter [Managing Memory for ADRLIST and SRowSet Structures](managing-memory-for-adrlist-and-srowset-structures.md).
  
## <a name="see-also"></a>Siehe auch



[IAddrBook::Address](iaddrbook-address.md)
  
[IMessage::ModifyRecipients](imessage-modifyrecipients.md)
  
[MAPIAllocateBuffer](mapiallocatebuffer.md)
  
[ADRLIST](adrlist.md)
  
[SRow](srow.md)
  
[SRowSet](srowset.md)


[MAPI-Strukturen](mapi-structures.md)

