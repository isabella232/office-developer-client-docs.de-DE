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
ms.openlocfilehash: 004498ac94aadaa075d87d4dd3c675c8cd5f4feb
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22563877"
---
# <a name="iaddrbookpreparerecips"></a>IAddrBook::PrepareRecips

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Bereitet eine Empfängerliste zur späteren Verwendung von messaging-System. 
  
```cpp
HRESULT PrepareRecips(
  ULONG ulFlags,
  LPSPropTagArray lpSPropTagArray,
  LPADRLIST lpRecipList
);
```

## <a name="parameters"></a>Parameter

 _ulFlags_
  
> [in] Eine Bitmaske aus Flags, die steuert, wie der Eintrag geöffnet wird. Das folgende Flag kann festgelegt werden:
    
MAPI_CACHE_ONLY
  
> Verwenden Sie nur das Offlineadressbuch, um namensauflösung auszuführen. Dieses Kennzeichen können Sie beispielsweise um eine Clientanwendung aus die globalen Adressliste (GAL) im Exchange-Cache-Modus geöffnet und den Zugriff auf eines Eintrags in diesem Adressbuch aus dem Cache ohne Erstellen von Datenverkehr zwischen dem Client und dem Server zu ermöglichen. Dieses Kennzeichen werden nur von der Exchange-Adressbuchanbieter unterstützt.
    
 _lpSPropTagArray_
  
> [in] Ein Zeiger auf eine [SPropTagArray](sproptagarray.md) -Struktur, die ein Array von Eigenschaftentags enthält, die die Eigenschaften gegebenenfalls hinweisen, Aktualisierung erfordern. Der Parameter _LpSPropTagArray_ kann NULL sein. 
    
 _lpRecipList_
  
> [in] Ein Zeiger auf eine [ADRLIST](adrlist.md) -Struktur, die die Liste der Empfänger enthält. 
    
## <a name="return-value"></a>R�ckgabewert

S_OK 
  
> Die Empfängerliste wurde erfolgreich vorbereitet.
    
## <a name="remarks"></a>HinwBemerkungeneise

Clients und Dienstanbieter rufen Sie die **PrepareRecips** -Methode, um Folgendes auszuführen: 
  
- Stellen Sie sicher, dass alle Empfänger im Parameter _LpRecipList_ langfristige-Eintragsbezeichner verfügen. 
    
- Stellen Sie sicher, dass der Empfänger in der _LpRecipList_ -Parameter im Parameter _LpSPropTagArray_ aufgeführten Eigenschaften verfügt und dass diese Eigenschaften am Anfang der Empfängerliste angezeigt werden. 
    
MAPI konvertiert des Empfängers kurzfristige-Eintragsbezeichner langfristige-Eintragsbezeichner. Gegebenenfalls Empfänger langfristige-Eintragsbezeichner aus der entsprechenden Adressbuchanbieter abgerufen werden, und alle zusätzlichen Eigenschaften angefordert werden.
  
In einen einzelnen Empfänger Eintrag werden Sie zunächst die angeforderten Eigenschaften sortiert gefolgt von Eigenschaften, die bereits für den Eintrag vorhanden waren. Wenn eine oder mehrere der angeforderten Eigenschaften im _LpSPropTagArray_ -Parameter nicht durch die entsprechende Adressbuchanbieter behandelt werden, werden ihre Eigenschaftentypen auf PT_ERROR festgelegt werden. Die Eigenschaftswerte werden festgelegt werden MAPI_E_NOT_FOUND oder auf einen anderen Wert, der einen genauere Grund gibt, warum die Eigenschaften nicht verfügbar sind. Jede [SPropValue](spropvalue.md) -Struktur, die in der _LpRecipList_ -Parameter enthalten muss separat zugeordnet werden, mithilfe der Funktionen [MAPIAllocateBuffer](mapiallocatebuffer.md) und [MAPIAllocateMore](mapiallocatemore.md) , damit er einzeln freigegeben werden kann. 
  
Informationen zu PT_ERROR finden Sie unter [Eigenschaftentypen](property-types.md).
  
## <a name="see-also"></a>Siehe auch



[ADRLIST](adrlist.md)
  
[IMAPIProp::GetProps](imapiprop-getprops.md)
  
[IMessage::ModifyRecipients](imessage-modifyrecipients.md)
  
[PidTagEntryId (kanonische Eigenschaft)](pidtagentryid-canonical-property.md)
  
[SPropValue](spropvalue.md)
  
[SRowSet](srowset.md)
  
[IAddrBook : IMAPIProp](iaddrbookimapiprop.md)

