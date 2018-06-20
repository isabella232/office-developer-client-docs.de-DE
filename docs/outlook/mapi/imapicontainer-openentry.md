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
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: c13ab9ce9c2564c39bfe9b2689f05439bc7b74ff
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792068"
---
# <a name="imapicontaineropenentry"></a>IMAPIContainer::OpenEntry

  
  
**Betrifft**: Outlook 
  
Öffnet ein Objekt im Container einen Schnittstellenzeiger für den weiteren Zugriff zurückgibt.
  
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
  
> [in] Die Byteanzahl von in die Eintrags-ID auf den durch den Parameter _LpEntryID_ verwiesen. 
    
 _lpEntryID_
  
> [in] Ein Zeiger auf die Eintrags-ID des Objekts zu öffnen. Wenn _LpEntryID_ auf NULL festgelegt ist, wird der Container der obersten Ebene in der Hierarchie des Containers geöffnet. 
    
 _lpInterface_
  
> [in] Ein Zeiger auf die Schnittstelle-ID (IID), die die Schnittstelle verwendet werden, Zugriff auf das Objekt darstellt. Bei Übergabe von NULL führt den Bezeichner für das Objekt Standardschnittstelle zurückgegeben wird. Für Nachrichten, die standard-Schnittstelle ist [IMAPIMessageSite: IUnknown](imapimessagesiteiunknown.md); für Ordner, es ist [IMAPIFolder: IMAPIContainer](imapifolderimapicontainer.md). Der Standard-Schnittstellen für Address Book-Objekten sind [IDistList: IMAPIContainer](idistlistimapicontainer.md) für eine Verteilerliste und [IMailUser: IMAPIProp](imailuserimapiprop.md) für ein messaging-Benutzer. 
    
 _ulFlags_
  
> [in] Eine Bitmaske aus Flags, die steuert, wie das Objekt geöffnet wird. Die folgenden Kennzeichen können festgelegt werden:
    
MAPI_BEST_ACCESS 
  
> Fordert an, dass das Objekt mit den maximale Netzwerkberechtigungen für den Benutzer und die maximale Anwendung Clientzugriff zulässig geöffnet wird. Beispielsweise sollte der Client Lese-/Schreibberechtigung verfügt, das Objekt mit Lese-/Schreibzugriff geöffnet werden; Wenn der Client schreibgeschützten Zugriff hat, sollte das Objekt mit schreibgeschützten Zugriff geöffnet werden. 
    
MAPI_DEFERRED_ERRORS 
  
> Ermöglicht **OpenEntry** erfolgreich, möglicherweise beendet, bevor das Objekt an den aufrufenden Client vollständig verfügbar ist. Wenn das Objekt nicht verfügbar ist, kann die nachfolgenden Objekt Anrufen ein Fehler ausgelöst. 
    
MAPI_MODIFY 
  
> Anfragen Lese-/Schreibberechtigung. Standardmäßig werden Objekte mit schreibgeschützten Zugriff geöffnet, und Clients sollte nicht verwendet werden, unter der Voraussetzung, die Lese-/Schreibzugriff, dass die Berechtigung erteilt wurde. 
    
SHOW_SOFT_DELETES
  
> Zeigt Elemente, die derzeit als soft gekennzeichnet sind gelöscht – d. h., sie sind in der Aufbewahrungszeit für gelöschte Elemente Zeit Phase.
    
 _lpulObjType_
  
> [out] Ein Zeiger auf die geöffnete Objekttyp.
    
 _lppUnk_
  
> [out] Ein Zeiger auf einen Zeiger auf die Implementierung eines verwenden, um das geöffnete Objekt zuzugreifen.
    
## <a name="return-value"></a>R�ckgabewert

S_OK 
  
> Das Objekt wurde erfolgreich geöffnet.
    
MAPI_E_NO_ACCESS 
  
> Der Benutzer verfügt nicht über ausreichende Berechtigungen zum Öffnen des Objekts oder es wurde versucht, ein nur-Lese-Objekt mit Lese-/Schreibzugriff zu öffnen.
    
MAPI_E_NOT_FOUND 
  
> Die _LpEntryID_ angegebene Eintrags-ID stellt kein Objekts dar. 
    
MAPI_E_UNKNOWN_ENTRYID 
  
> Die Eintrags-ID in der _LpEntryID_ -Parameter ist nicht vom durch das Container erkanntes Format. 
    
## <a name="remarks"></a>Hinweise

Die **IMAPIContainer::OpenEntry** -Methode öffnet ein Objekt in der gesamten ein Container und gibt einen Zeiger auf eine Implementierung für weitere Access verwenden. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Da Dienstanbieter nicht erforderlich sind, um eine Implementierung der von der Schnittstelle-ID in der _LpInterface_ -Parameter angegebenen Typs zurückzugeben, überprüfen Sie den Wert, der auf den durch den Parameter _LpulObjType_ . Wandeln Sie den Zeiger auf einen Zeiger des entsprechenden Typs in _LppUnk_ zurückgegeben. 
  
Standardmäßig öffnen Dienstanbieter Objekte mit schreibgeschützten Zugriff, es sei denn, Sie entweder die MAPI_MODIFY oder MAPI_BEST_ACCESS-Flag festlegen. Wenn eine der folgenden Werte festgelegt ist, versuchen Dienstanbieter, ein änderbare-Objekt zurückzugeben. Allerdings nehmen Sie nicht an, die, da Sie ein Objekt geändert werden, dass das geöffnete Objekt Lese-/Schreibberechtigung hat angefordert haben. Entweder die Möglichkeit der Änderung einer nachfolgenden fehl, oder rufen Sie das Objekt **PR_ACCESS_LEVEL** -Eigenschaft, gewährt durch **OpenEntry**Zugriffsstufe planen.
  
## <a name="see-also"></a>Siehe auch



[IMAPIContainer: IMAPIProp](imapicontainerimapiprop.md)

