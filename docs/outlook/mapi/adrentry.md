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
  
Beschreibt NULL oder mehr Eigenschaften, die zu einem Empfänger gehören.
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapidefs. h  <br/> |
   
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
  
> Reserviert muss NULL sein.
    
 **cValues**
  
> Die Anzahl der Eigenschaften im Eigenschafts Wertarray, auf die durch das **rgPropVals** -Element verwiesen wird. Das **cValues** -Element kann NULL sein. 
    
 **rgPropVals**
  
> Zeiger auf ein Eigenschaftswert Array, das die Eigenschaften für den Empfänger beschreibt. Das **rgPropVals** -Element kann NULL sein. 
    
## <a name="remarks"></a>Bemerkungen

In einer **Miet** Struktur werden Eigenschaften beschrieben, die zu einem einzelnen Empfänger gehören. Zu den Eigenschaften, die in der Regel zur Beschreibung eines Empfängers verwendet werden, gehören die folgenden: 
  
 **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))
  
 **PR_ADDRTYPE** ([Pidtagaddresstype (](pidtagaddresstype-canonical-property.md))
  
 **PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))
  
 **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))
  
Wenn im [SPropValue](spropvalue.md) -Array für einen Empfänger eine Eintrags-ID oder eine **PR_ENTRYID** -Eigenschaft angezeigt wird, bedeutet dies, dass der Empfänger aufgelöst wurde. Clients rufen die [IAddrBook::](iaddrbook-resolvename.md) ResolveName-Methode auf, um sicherzustellen, dass alle Empfänger in der Empfängerliste einer ausgehenden Nachricht aufgelöst wurden. Nur aufgelöste Empfänger können mit Nachrichten gesendet werden. 
  
 **Miet** Strukturen werden in der Regel kombiniert, um ein Array für das **aEntries** -Element einer [ADRLIST](adrlist.md) -Struktur zu bilden. 
  
 **Miet** Strukturen und [SRow](srow.md) -Strukturen sind identisch, da Sie sowohl ein reserviertes Element, ein Array mit Eigenschaftswerten als auch eine Anzahl von Werten im Array enthalten. Während die **Miet** Strukturen zu dem **aEntries** -Element einer **ADRLIST** -Struktur kombiniert werden, werden **SRow** -Strukturen kombiniert, um das **aRow** -Element einer [SRowSet](srowset.md) -Struktur zu bilden. Beide Arten von Strukturen folgen den gleichen Zuordnungsregeln, was bedeutet, dass eine **SRowSet** -Struktur, die aus der Inhaltstabelle eines Adressbuch Containers abgerufen wird, in eine **ADRLIST** -Struktur umgewandelt und unverändert verwendet werden kann. 
  
Eine **Miet** Struktur kann leer sein. Beispielsweise kann eine in der **ADRLIST** -Struktur enthaltene **Miet** Struktur, auf die durch den _lppAdrList_ -Parameter in einem Aufruf von **IAddrBook:: Address** verwiesen wird, leer sein, wenn ein Empfänger entfernt wird. 
  
Weitere Informationen zum Zuweisen von Arbeitsspeicher für **Miet** Strukturen finden Sie unter [Managing Memory for ADRLIST and SRowSet Structures](managing-memory-for-adrlist-and-srowset-structures.md).
  
## <a name="see-also"></a>Siehe auch



[IAddrBook::Address](iaddrbook-address.md)
  
[IMessage::ModifyRecipients](imessage-modifyrecipients.md)
  
[MAPIAllocateBuffer](mapiallocatebuffer.md)
  
[ADRLIST](adrlist.md)
  
[SRow](srow.md)
  
[SRowSet](srowset.md)


[MAPI-Strukturen](mapi-structures.md)

