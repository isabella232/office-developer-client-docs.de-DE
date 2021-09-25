---
title: IMAPIContainerOpenEntry
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPIContainer.OpenEntry
api_type:
- COM
ms.assetid: 0c46c1fb-dd63-4ac5-960e-80f68e75d8f4
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 4dc0784f5dec810abcd8bb763fbf1e1417d3446a
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59596372"
---
# <a name="imapicontaineropenentry"></a>IMAPIContainer::OpenEntry

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Öffnet ein Objekt im Container und gibt einen Schnittstellenzeiger für den weiteren Zugriff zurück.
  
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
  
> [in] Ein Zeiger auf den Eintragsbezeichner des zu öffnenden Objekts. Wenn  _lpEntryID_ auf NULL festgelegt ist, wird der Container auf oberster Ebene in der Containerhierarchie geöffnet. 
    
 _lpInterface_
  
> [in] Ein Zeiger auf den Schnittstellenbezeichner (IID), der die Schnittstelle darstellt, die für den Zugriff auf das Objekt verwendet werden soll. Wenn NULL übergeben wird, wird der Bezeichner für die Standardschnittstelle des Objekts zurückgegeben. Bei Nachrichten ist die Standardschnittstelle [IMAPIMessageSite : IUnknown](imapimessagesiteiunknown.md); für Ordner ist dies [IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md). Die Standardschnittstellen für Adressbuchobjekte sind [IDistList : IMAPIContainer](idistlistimapicontainer.md) für eine Verteilerliste und [IMailUser : IMAPIProp](imailuserimapiprop.md) für einen Messagingbenutzer. 
    
 _ulFlags_
  
> [in] Eine Bitmaske mit Flags, die steuert, wie das Objekt geöffnet wird. Die folgenden Flags können festgelegt werden:
    
MAPI_BEST_ACCESS 
  
> Fordert an, dass das Objekt mit den für den Benutzer maximal zulässigen Netzwerkberechtigungen und dem maximalen Clientanwendungszugriff geöffnet wird. Wenn der Client beispielsweise über Lese-/Schreibberechtigungen verfügt, sollte das Objekt mit Lese-/Schreibberechtigung geöffnet werden. Wenn der Client über schreibgeschützten Zugriff verfügt, sollte das Objekt mit schreibgeschütztem Zugriff geöffnet werden. 
    
MAPI_DEFERRED_ERRORS 
  
> Ermöglicht **OpenEntry** die erfolgreiche Rückgabe, möglicherweise bevor das Objekt für den aufrufenden Client vollständig verfügbar ist. Wenn das Objekt nicht verfügbar ist, kann das Ausführen eines nachfolgenden Objektaufrufs einen Fehler auslösen. 
    
MAPI_MODIFY 
  
> Fordert Lese-/Schreibberechtigung an. Standardmäßig werden Objekte mit schreibgeschütztem Zugriff geöffnet, und Clients sollten nicht unter der Annahme funktionieren, dass Lese-/Schreibberechtigungen erteilt wurden. 
    
SHOW_SOFT_DELETES
  
> Zeigt Elemente an, die derzeit als vorläufig gelöscht markiert sind, d. h., sie befinden sich in der Aufbewahrungszeitphase für gelöschte Elemente.
    
 _lpulObjType_
  
> [out] Ein Zeiger auf den Typ des geöffneten Objekts.
    
 _lppUnk_
  
> [out] Ein Zeiger auf einen Zeiger auf die Schnittstellenimplementierungen, die für den Zugriff auf das geöffnete Objekt verwendet werden sollen.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Das Objekt wurde erfolgreich geöffnet.
    
MAPI_E_NO_ACCESS 
  
> Entweder verfügt der Benutzer über unzureichende Berechtigungen zum Öffnen des Objekts, oder es wurde versucht, ein schreibgeschütztes Objekt mit Lese-/Schreibberechtigung zu öffnen.
    
MAPI_E_NOT_FOUND 
  
> Der durch  _lpEntryID_ angegebene Eintragsbezeichner stellt kein Objekt dar. 
    
MAPI_E_UNKNOWN_ENTRYID 
  
> Der Eintragsbezeichner im  _LpEntryID-Parameter_ weist kein vom Container erkanntes Format auf. 
    
## <a name="remarks"></a>HinwBemerkungeneise

Die **IMAPIContainer::OpenEntry-Methode** öffnet ein Objekt in einem Container und gibt einen Zeiger auf eine Schnittstellenimplementierung zurück, die für den weiteren Zugriff verwendet werden soll. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Da Dienstanbieter keine Schnittstellenimplementierungen des Typs zurückgeben müssen, der durch den Schnittstellenbezeichner im  _lpInterface-Parameter_ angegeben ist, überprüfen Sie den Wert, auf den der  _Parameter "lpulObjType"_ verweist. Wandeln Sie bei Bedarf den in  _lppUnk_ zurückgegebenen Zeiger in einen Zeiger des entsprechenden Typs um. 
  
Standardmäßig öffnen Dienstanbieter Objekte mit schreibgeschütztem Zugriff, es sei denn, Sie legen das Flag MAPI_MODIFY oder MAPI_BEST_ACCESS fest. Wenn eines dieser Flags festgelegt ist, versuchen Dienstanbieter, ein veränderbares Objekt zurückzugeben. Gehen Sie jedoch nicht davon aus, dass das geöffnete Objekt über Lese-/Schreibberechtigung verfügt, da Sie ein änderbares Objekt angefordert haben. Planen Sie entweder die Möglichkeit, dass eine nachfolgende Änderung fehlschlägt, oder rufen Sie die **PR_ACCESS_LEVEL** Eigenschaft des Objekts ab, um die von **OpenEntry** gewährte Zugriffsebene zu bestimmen.
  
## <a name="see-also"></a>Siehe auch



[IMAPIContainer : IMAPIProp](imapicontainerimapiprop.md)

