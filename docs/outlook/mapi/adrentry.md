---
title: ADRENTRY
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- ADRENTRY
api_type:
- COM
ms.assetid: 5fa091a4-3a84-4881-91b3-e34fd9ca6f38
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: e9b2f73b6f70eea353a023a7285d210e508d6e6b
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59551863"
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

## <a name="members"></a>Members

 **ulReserved1**
  
> Reserviert; muss Null sein.
    
 **cValues**
  
> Anzahl der Eigenschaften im Eigenschaftswertarray, auf das der **rgPropVals-Member** verweist. Der **cValues-Member** kann Null sein. 
    
 **rgPropVals**
  
> Zeiger auf ein Eigenschaftenwertarray, das die Eigenschaften für den Empfänger beschreibt. Der **rgPropVals-Member** kann NULL sein. 
    
## <a name="remarks"></a>HinwBemerkungeneise

Eine **ADRENTRY-Struktur** beschreibt Eigenschaften, die zu einem einzelnen Empfänger gehören. Zu den Eigenschaften, die in der Regel zum Beschreiben eines Empfängers verwendet werden, gehören folgende: 
  
 **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))
  
 **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))
  
 **PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))
  
 **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))
  
Wenn ein Eintragsbezeichner oder **eine PR_ENTRYID** Eigenschaft im [SPropValue-Array](spropvalue.md) für einen Empfänger angezeigt wird, bedeutet dies, dass der Empfänger aufgelöst wurde. Clients rufen die [IAddrBook::ResolveName-Methode](iaddrbook-resolvename.md) auf, um sicherzustellen, dass alle Empfänger in der Empfängerliste einer ausgehenden Nachricht aufgelöst wurden. Nur aufgelöste Empfänger können mit Nachrichten gesendet werden. 
  
 **ADRENTRY-Strukturen** werden in der Regel kombiniert, um ein Array für das **aEntries-Element** einer [ADRLIST-Struktur](adrlist.md) zu bilden. 
  
 **ADRENTRY-Strukturen** und [SRow-Strukturen](srow.md) sind identisch, da beide ein reserviertes Element, ein Array von Eigenschaftswerten und eine Anzahl von Werten im Array enthalten. Während **ADRENTRY-Strukturen** kombiniert werden, um **das Mitglied aEntries** einer **ADRLIST-Struktur** zu bilden, werden **SRow-Strukturen** kombiniert, um das **aRow-Element** einer [SRowSet-Struktur](srowset.md) zu bilden. Beide Arten von Strukturen folgen den gleichen Zuordnungsregeln, was bedeutet, dass eine **SRowSet-Struktur,** die aus dem Inhaltsverzeichnis eines Adressbuchcontainers abgerufen wird, in eine **ADRLIST-Struktur** umgewandelt und unverändert verwendet werden kann. 
  
Eine **ADRENTRY-Struktur** kann leer sein. Beispielsweise kann eine **ADRENTRY-Struktur,** die in der **ADRLIST-Struktur** enthalten ist, auf die der  _lppAdrList-Parameter_ in einem Aufruf von **IAddrBook::Address** verweist, leer sein, wenn ein Empfänger entfernt wird. 
  
Weitere Informationen zum Zuordnen von Speicher für **ADRENTRY-Strukturen** finden Sie unter [Managing Memory for ADRLIST and SRowSet Structures](managing-memory-for-adrlist-and-srowset-structures.md).
  
## <a name="see-also"></a>Siehe auch



[IAddrBook::Address](iaddrbook-address.md)
  
[IMessage::ModifyRecipients](imessage-modifyrecipients.md)
  
[MAPIAllocateBuffer](mapiallocatebuffer.md)
  
[ADRLIST](adrlist.md)
  
[SRow](srow.md)
  
[SRowSet](srowset.md)


[MAPI-Strukturen](mapi-structures.md)

