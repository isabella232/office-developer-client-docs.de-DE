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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339221"
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
  
> in Eine Bitmaske von Flags, die steuert, wie der Eintrag geöffnet wird. Das folgende Flag kann festgelegt werden:
    
MAPI_CACHE_ONLY
  
> Verwenden Sie nur das Offlineadressbuch, um die Namensauflösung durchzuführen. Sie können dieses Flag beispielsweise verwenden, um einer Clientanwendung das Öffnen der globalen Adressliste (GAL) im Exchange-Cache-Modus zu gestatten und den Zugriff auf einen Eintrag in diesem Adressbuch aus dem Cache zu ermöglichen, ohne Datenverkehr zwischen dem Client und dem Server zu erstellen. Dieses Flag wird nur vom Exchange-Adressbuchanbieter unterstützt.
    
 _lpSPropTagArray_
  
> in Ein Zeiger auf eine [SPropTagArray](sproptagarray.md) -Struktur, die ein Array von Property-Tags enthält, die die Eigenschaften anzeigen, die aktualisiert werden müssen. Der _lpSPropTagArray_ -Parameter kann NULL sein. 
    
 _lpRecipList_
  
> in Ein Zeiger auf eine [ADRLIST](adrlist.md) -Struktur, die die Liste der Empfänger enthält. 
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Die Empfängerliste wurde erfolgreich vorbereitet.
    
## <a name="remarks"></a>Bemerkungen

Clients und Dienstanbieter rufen die **PrepareRecips** -Methode auf, um folgende Aktionen auszuführen: 
  
- Stellen Sie sicher, dass alle Empfänger im Parameter _lpRecipList_ langfristige Eintragsbezeichner aufweisen. 
    
- Stellen Sie sicher, dass jeder Empfänger im _lpRecipList_ -Parameter über die im Parameter _lpSPropTagArray_ aufgeführten Eigenschaften verfügt und diese Eigenschaften am Anfang der Empfängerliste angezeigt werden. 
    
MAPI konvertiert die kurzfristigen Eintragsbezeichner der einzelnen Empfänger in langfristige Eintrags-IDs. Bei Bedarf werden die langfristigen Eintragsbezeichner des Empfängers aus dem entsprechenden Adressbuchanbieter abgerufen, und zusätzliche Eigenschaften werden angefordert.
  
In einem einzelnen Empfängereintrag werden die angeforderten Eigenschaften zuerst sortiert, gefolgt von Eigenschaften, die bereits für den Eintrag vorhanden waren. Wenn eine oder mehrere der angeforderten Eigenschaften im _lpSPropTagArray_ -Parameter nicht vom entsprechenden Adressbuchanbieter verarbeitet werden, werden Ihre Eigenschaftentypen auf PT_ERROR festgelegt. Ihre Eigenschaftswerte werden auf MAPI_E_NOT_FOUND oder auf einen anderen Wert festgelegt, der einen spezifischeren Grund liefert, warum die Eigenschaften nicht verfügbar sind. Jede [SPropValue](spropvalue.md) -Struktur, die im _lpRecipList_ -Parameter enthalten ist, muss mithilfe der [MAPIAllocateBuffer](mapiallocatebuffer.md) -und [MAPIAllocateMore](mapiallocatemore.md) -Funktionen separat zugewiesen werden, damit Sie einzeln freigegeben werden kann. 
  
Weitere Informationen zu PT_ERROR finden Sie unter [Property Types](property-types.md).
  
## <a name="see-also"></a>Siehe auch



[ADRLIST](adrlist.md)
  
[IMAPIProp::GetProps](imapiprop-getprops.md)
  
[IMessage::ModifyRecipients](imessage-modifyrecipients.md)
  
[Kanonische PidTagEntryId-Eigenschaft](pidtagentryid-canonical-property.md)
  
[SPropValue](spropvalue.md)
  
[SRowSet](srowset.md)
  
[IAddrBook : IMAPIProp](iaddrbookimapiprop.md)

