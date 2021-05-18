---
title: IAddrBookPrepareRecips
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IAddrBook.PrepareRecips
api_type:
- COM
ms.assetid: d423f7b5-23b8-44dd-bca3-6590182dc42d
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: db1c23f33e604d6aafdd8a046566c7390c281ad8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414277"
---
# <a name="iaddrbookpreparerecips"></a>IAddrBook::PrepareRecips

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Bereitet eine Empfängerliste für die spätere Verwendung durch das Messagingsystem vor. 
  
```cpp
HRESULT PrepareRecips(
  ULONG ulFlags,
  LPSPropTagArray lpSPropTagArray,
  LPADRLIST lpRecipList
);
```

## <a name="parameters"></a>Parameter

 _ulFlags_
  
> [in] Eine Bitmaske mit Flags, die steuert, wie der Eintrag geöffnet wird. Das folgende Flag kann festgelegt werden:
    
MAPI_CACHE_ONLY
  
> Verwenden Sie nur das Offlineadressbuch, um die Namensauflösung durchzuführen. Sie können dieses Flag beispielsweise verwenden, um einer Clientanwendung das Öffnen der globalen Adressliste (GLOBAL Address List, GAL) im zwischengespeicherten Exchange-Modus und den Zugriff auf einen Eintrag in diesem Adressbuch aus dem Cache zu ermöglichen, ohne Datenverkehr zwischen dem Client und dem Server zu erstellen. Dieses Flag wird nur vom adressbuchanbieter Exchange unterstützt.
    
 _lpSPropTagArray_
  
> [in] Ein Zeiger auf eine [SPropTagArray-Struktur,](sproptagarray.md) die ein Array von Eigenschaftstags enthält, die die Eigenschaften angeben, falls vorhanden, die aktualisiert werden müssen. Der  _lpSPropTagArray-Parameter_ kann NULL sein. 
    
 _lpRecipList_
  
> [in] Ein Zeiger auf eine [ADRLIST-Struktur,](adrlist.md) die die Liste der Empfänger enthält. 
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Die Empfängerliste wurde erfolgreich vorbereitet.
    
## <a name="remarks"></a>Hinweise

Clients und Dienstanbieter rufen die **PrepareRecips-Methode** auf, um folgendes zu tun: 
  
- Stellen Sie sicher, dass alle Empfänger im  _lpRecipList-Parameter_ über langfristige Eintragsbezeichner verfügen. 
    
- Stellen Sie sicher, dass jeder Empfänger im  _lpRecipList-Parameter_ über die im  _lpSPropTagArray-Parameter_ aufgeführten Eigenschaften verfügt und dass diese Eigenschaften am Anfang der Empfängerliste angezeigt werden. 
    
MAPI konvertiert die kurzfristigen Eintragsbezeichner jedes Empfängers in langfristige Eintragsbezeichner. Bei Bedarf werden die langfristigen Eintrags-IDs der Empfänger vom entsprechenden Adressbuchanbieter abgerufen, und es werden zusätzliche Eigenschaften angefordert.
  
In einem einzelnen Empfängereintrag werden die angeforderten Eigenschaften zuerst geordnet, gefolgt von allen Eigenschaften, die bereits für den Eintrag vorhanden waren. Wenn eine oder mehrere der angeforderten Eigenschaften im  _lpSPropTagArray-Parameter_ nicht vom entsprechenden Adressbuchanbieter verarbeitet werden, werden ihre Eigenschaftstypen auf PT_ERROR. Ihre Eigenschaftswerte werden entweder auf MAPI_E_NOT_FOUND oder auf einen anderen Wert festgelegt, der einen genaueren Grund dafür gibt, warum die Eigenschaften nicht verfügbar sind. Jede im _lpRecipList-Parameter_ enthaltene [SPropValue-Struktur](spropvalue.md) muss mithilfe der [Funktionen MAPIAllocateBuffer](mapiallocatebuffer.md) und [MAPIAllocateMore](mapiallocatemore.md) separat zugeordnet werden, damit sie einzeln frei werden kann. 
  
Weitere Informationen zu PT_ERROR finden Sie unter [Property Types](property-types.md).
  
## <a name="see-also"></a>Siehe auch



[ADRLIST](adrlist.md)
  
[IMAPIProp::GetProps](imapiprop-getprops.md)
  
[IMessage::ModifyRecipients](imessage-modifyrecipients.md)
  
[PidTagEntryId (kanonische Eigenschaft)](pidtagentryid-canonical-property.md)
  
[SPropValue](spropvalue.md)
  
[SRowSet](srowset.md)
  
[IAddrBook : IMAPIProp](iaddrbookimapiprop.md)

