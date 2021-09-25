---
title: IAddrBookPrepareRecips
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IAddrBook.PrepareRecips
api_type:
- COM
ms.assetid: d423f7b5-23b8-44dd-bca3-6590182dc42d
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 461cd536641e338cd29c849bb8069d3ac34f1667
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59613954"
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
  
> [in] Eine Bitmaske mit Flags, die steuert, wie der Eintrag geöffnet wird. Das folgende Kennzeichen kann festgelegt werden:
    
MAPI_CACHE_ONLY
  
> Verwenden Sie nur das Offlineadressbuch, um die Namensauflösung auszuführen. Beispielsweise können Sie dieses Flag verwenden, um einer Clientanwendung das Öffnen der globalen Adressliste (GAL) im Cache-Exchange-Modus und den Zugriff auf einen Eintrag in diesem Adressbuch aus dem Cache zu ermöglichen, ohne Datenverkehr zwischen dem Client und dem Server zu erstellen. Dieses Flag wird nur vom Exchange Adressbuchanbieter unterstützt.
    
 _lpSPropTagArray_
  
> [in] Ein Zeiger auf eine [SPropTagArray-Struktur,](sproptagarray.md) die ein Array von Eigenschaftstags enthält, die ggf. die Eigenschaften angeben, die aktualisiert werden müssen. Der  _LpSPropTagArray-Parameter_ kann NULL sein. 
    
 _lpRecipList_
  
> [in] Ein Zeiger auf eine [ADRLIST-Struktur,](adrlist.md) die die Liste der Empfänger enthält. 
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Die Empfängerliste wurde erfolgreich vorbereitet.
    
## <a name="remarks"></a>Bemerkungen

Clients und Dienstanbieter rufen die **PrepareRecips-Methode** auf, um Folgendes zu tun: 
  
- Stellen Sie sicher, dass alle Empfänger im  _Parameter lpRecipList_ langfristige Eintragsbezeichner haben. 
    
- Stellen Sie sicher, dass jeder Empfänger im  _LpRecipList-Parameter_ über die im  _LpSPropTagArray-Parameter_ aufgeführten Eigenschaften verfügt und dass diese Eigenschaften am Anfang der Empfängerliste angezeigt werden. 
    
Die MAPI konvertiert die bezeichner für den kurzfristigen Eintrag jedes Empfängers in langfristige Eintragsbezeichner. Bei Bedarf werden die langfristigen Eintragsbezeichner von Empfängern vom entsprechenden Adressbuchanbieter abgerufen, und alle zusätzlichen Eigenschaften werden angefordert.
  
In einem einzelnen Empfängereintrag werden die angeforderten Eigenschaften zuerst sortiert, gefolgt von allen Eigenschaften, die bereits für den Eintrag vorhanden waren. Wenn eine oder mehrere der angeforderten Eigenschaften im  _LpSPropTagArray-Parameter_ nicht vom entsprechenden Adressbuchanbieter verarbeitet werden, werden deren Eigenschaftstypen auf PT_ERROR festgelegt. Ihre Eigenschaftswerte werden entweder auf MAPI_E_NOT_FOUND oder auf einen anderen Wert festgelegt, der einen spezifischeren Grund dafür liefert, warum die Eigenschaften nicht verfügbar sind. Jede im _lpRecipList-Parameter_ [enthaltene SPropValue-Struktur](spropvalue.md) muss mithilfe der [MAPIAllocateBuffer-](mapiallocatebuffer.md) und [MAPIAllocateMore-Funktionen](mapiallocatemore.md) separat zugeordnet werden, damit sie einzeln freigegeben werden kann. 
  
Informationen zu PT_ERROR finden Sie unter [Eigenschaftstypen.](property-types.md)
  
## <a name="see-also"></a>Siehe auch



[ADRLIST](adrlist.md)
  
[IMAPIProp::GetProps](imapiprop-getprops.md)
  
[IMessage::ModifyRecipients](imessage-modifyrecipients.md)
  
[PidTagEntryId (kanonische Eigenschaft)](pidtagentryid-canonical-property.md)
  
[SPropValue](spropvalue.md)
  
[SRowSet](srowset.md)
  
[IAddrBook : IMAPIProp](iaddrbookimapiprop.md)

