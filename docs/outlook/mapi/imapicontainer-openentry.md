---
title: IMAPIContainerOpenEntry
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIContainer.OpenEntry
api_type:
- COM
ms.assetid: 0c46c1fb-dd63-4ac5-960e-80f68e75d8f4
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 9598e0c90c16db14cdc3a46d2b2ae74e0d9a9300
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423636"
---
# <a name="imapicontaineropenentry"></a>IMAPIContainer::OpenEntry

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Öffnet ein Objekt im Container und gibt einen Schnittstellenzeiger für weiteren Zugriff zurück.
  
```cpp
HRESULT OpenEntry(
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  LPCIID lpInterface,
  ULONG ulFlags,
  ULONG FAR * lpulObjType,
  LPUNKNOWN FAR * lppUnk
);
```

## <a name="parameters"></a>Parameter

 _cbEntryID_
  
> [in] Die Byteanzahl im Eintragsbezeichner, auf den der  _lpEntryID-Parameter_ verweist. 
    
 _lpEntryID_
  
> [in] Ein Zeiger auf den Eintragsbezeichner des zu öffnende Objekts. Wenn  _lpEntryID_ auf NULL festgelegt ist, wird der Container auf oberster Ebene in der Containerhierarchie geöffnet. 
    
 _lpInterface_
  
> [in] Ein Zeiger auf die Schnittstellen-ID (Interface Identifier, IID), die die Schnittstelle darstellt, die für den Zugriff auf das Objekt verwendet werden soll. Das Übergeben von NULL führt dazu, dass der Bezeichner für die Standardschnittstelle des Objekts zurückgegeben wird. Für Nachrichten ist die Standardschnittstelle [IMAPIMessageSite : IUnknown](imapimessagesiteiunknown.md); für Ordner ist es [IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md). Die Standardschnittstellen für Adressbuchobjekte sind [IDistList : IMAPIContainer](idistlistimapicontainer.md) für eine Verteilerliste und [IMailUser : IMAPIProp](imailuserimapiprop.md) für einen Messagingbenutzer. 
    
 _ulFlags_
  
> [in] Eine Bitmaske mit Flags, die steuert, wie das Objekt geöffnet wird. Die folgenden Kennzeichen können festgelegt werden:
    
MAPI_BEST_ACCESS 
  
> Fordert an, dass das Objekt mit den maximal zulässigen Netzwerkberechtigungen für den Benutzer und dem maximalen Clientanwendungszugriff geöffnet wird. Wenn der Client beispielsweise über Lese-/Schreibberechtigungen verfügt, sollte das Objekt mit Lese-/Schreibberechtigung geöffnet werden. Wenn der Client über schreibgeschützten Zugriff verfügt, sollte das Objekt mit schreibgeschützten Zugriff geöffnet werden. 
    
MAPI_DEFERRED_ERRORS 
  
> Ermöglicht **openEntry** die erfolgreiche Rückgabe, möglicherweise bevor das Objekt vollständig für den aufrufenden Client verfügbar ist. Wenn das Objekt nicht verfügbar ist, kann durch einen nachfolgenden Objektaufruf ein Fehler verursacht werden. 
    
MAPI_MODIFY 
  
> Fordert Lese-/Schreibberechtigungen an. Standardmäßig werden Objekte mit schreibgeschützten Zugriff geöffnet, und Clients sollten nicht unter der Annahme funktionieren, dass Lese-/Schreibberechtigungen erteilt wurden. 
    
SHOW_SOFT_DELETES
  
> Zeigt Elemente an, die derzeit als "soft deleted" gekennzeichnet sind, d. h. sie befinden sich in der Aufbewahrungszeit für gelöschte Elemente.
    
 _lpulObjType_
  
> [out] Ein Zeiger auf den Typ des geöffneten Objekts.
    
 _lppUnk_
  
> [out] Ein Zeiger auf einen Zeiger auf die Schnittstellenimplementierung, die für den Zugriff auf das geöffnete Objekt verwendet werden soll.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Das Objekt wurde erfolgreich geöffnet.
    
MAPI_E_NO_ACCESS 
  
> Entweder verfügt der Benutzer nicht über ausreichende Berechtigungen zum Öffnen des Objekts, oder es wurde versucht, ein schreibgeschütztes Objekt mit Lese-/Schreibberechtigung zu öffnen.
    
MAPI_E_NOT_FOUND 
  
> Der von  _lpEntryID_ angegebene Eintragsbezeichner stellt kein Objekt dar. 
    
MAPI_E_UNKNOWN_ENTRYID 
  
> Der Eintragsbezeichner im  _lpEntryID-Parameter_ hat kein vom Container erkanntes Format. 
    
## <a name="remarks"></a>Hinweise

Die **IMAPIContainer::OpenEntry-Methode** öffnet ein Objekt in einem Container und gibt einen Zeiger auf eine Schnittstellenimplementierung zurück, die für weiteren Zugriff verwendet werden soll. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Da Dienstanbieter keine Schnittstellenimplementierung des typs zurückgeben müssen, der durch den Schnittstellenbezeichner im  _lpInterface-Parameter_ angegeben wird, überprüfen Sie den Wert, auf den der  _lpulObjType-Parameter_ verweist. Bei Bedarf wird der in  _lppUnk_ zurückgegebene Zeiger in einen Zeiger des entsprechenden Typs umgekippt. 
  
Standardmäßig öffnen Dienstanbieter Objekte mit schreibgeschützten Zugriffen, es sei denn, Sie legen MAPI_MODIFY oder MAPI_BEST_ACCESS ein. Wenn eines dieser Kennzeichen festgelegt ist, versuchen Dienstanbieter, ein veränderbares Objekt zurückzusenken. Gehen Sie jedoch nicht davon aus, dass das geöffnete Objekt über Lese-/Schreibberechtigungen verfügt, da Sie ein veränderbares Objekt angefordert haben. Planen Sie entweder, dass eine nachfolgende Änderung fehlschlägt, oder rufen Sie die **PR_ACCESS_LEVEL-Eigenschaft** des Objekts ab, um die von **OpenEntry** gewährte Zugriffsebene zu bestimmen.
  
## <a name="see-also"></a>Siehe auch



[IMAPIContainer : IMAPIProp](imapicontainerimapiprop.md)

