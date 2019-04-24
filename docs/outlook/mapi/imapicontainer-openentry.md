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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32286932"
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
  
> in Die Anzahl der Bytes in der Eintrags-ID, auf die durch den _lpEntryID_ -Parameter verwiesen wird. 
    
 _lpEntryID_
  
> in Ein Zeiger auf die Eintrags-ID des zu öffnenden Objekts. Wenn _lpEntryID_ auf NULL festgelegt ist, wird der Container der obersten Ebene in der Hierarchie des Containers geöffnet. 
    
 _lpInterface_
  
> in Ein Zeiger auf die Schnittstellen-ID (IID), die die Schnittstelle darstellt, die für den Zugriff auf das Objekt verwendet werden soll. Das übergeben von NULL führt zu dem Bezeichner für die zurückgegebene Standardschnittstelle des Objekts. Bei Nachrichten lautet die Standardschnittstelle [IMAPIMessageSite: IUnknown](imapimessagesiteiunknown.md); für Ordner ist es [IMAPIFolder: IMAPIContainer](imapifolderimapicontainer.md). Die Standardschnittstellen für Adressbuch Objekte sind [IDistList: IMAPIContainer](idistlistimapicontainer.md) für eine Verteilerliste und [IMailUser: IMAPIProp](imailuserimapiprop.md) für einen Messagingbenutzer. 
    
 _ulFlags_
  
> in Eine Bitmaske von Flags, die steuert, wie das Objekt geöffnet wird. Die folgenden Flags können festgelegt werden:
    
MAPI_BEST_ACCESS 
  
> Fordert, dass das Objekt mit den maximal zulässigen Netzwerkberechtigungen für den Benutzer und dem maximalen Zugriff auf Clientanwendungen geöffnet wird. Wenn der Client beispielsweise über Lese-/Schreibzugriff verfügt, sollte das Objekt mit Lese-/Schreibzugriff geöffnet werden. Wenn der Client schreibgeschützten Zugriff hat, sollte das Objekt mit Schreibschutz geöffnet werden. 
    
MAPI_DEFERRED_ERRORS 
  
> Ermöglicht **** das erfolgreiche zurückgeben von OpenEntry, bevor das Objekt vollständig für den aufrufenden Client verfügbar ist. Wenn das Objekt nicht verfügbar ist, kann durch einen nachfolgenden Objektaufruf ein Fehler ausgelöst werden. 
    
MAPI_MODIFY 
  
> Fordert Lese-/Schreibzugriff-Berechtigung an. Standardmäßig werden Objekte mit Schreibschutz geöffnet, und Clients sollten nicht unter der Annahme arbeiten, dass die Berechtigung zum Lesen/Schreiben erteilt wurde. 
    
SHOW_SOFT_DELETES
  
> Zeigt Elemente an, die derzeit als weich gelöscht markiert sind, d. h., Sie befinden sich in der Aufbewahrungszeit für gelöschte Elemente.
    
 _lpulObjType_
  
> Out Ein Zeiger auf den Typ des geöffneten Objekts.
    
 _lppUnk_
  
> Out Ein Zeiger auf einen Zeiger auf die Schnittstellenimplementierung, die für den Zugriff auf das Open-Objekt verwendet werden soll.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Das Objekt wurde erfolgreich geöffnet.
    
MAPI_E_NO_ACCESS 
  
> Entweder hat der Benutzer unzureichende Berechtigungen zum Öffnen des Objekts oder es wurde versucht, ein schreibgeschütztes Objekt mit Lese-/Schreibzugriff zu öffnen.
    
MAPI_E_NOT_FOUND 
  
> Die durch _lpEntryID_ angegebene Eintrags-ID stellt kein Objekt dar. 
    
MAPI_E_UNKNOWN_ENTRYID 
  
> Die Eintrags-ID im _lpEntryID_ -Parameter weist kein Format auf, das vom Container erkannt wird. 
    
## <a name="remarks"></a>Bemerkungen

Die **IMAPIContainer:: OpenEntry** -Methode öffnet ein Objekt in einem Container und gibt einen Zeiger auf eine Schnittstellenimplementierung zurück, die für weiteren Zugriff verwendet werden soll. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Da es für Dienstanbieter nicht erforderlich ist, eine Schnittstellenimplementierung des durch den Schnittstellenbezeichner im _lpInterface_ -Parameter angegebenen Typs zurückzugeben, überprüfen Sie den Wert, der durch den _lpulObjType_ -Parameter verweist. Falls erforderlich, wandeln Sie den in _lppUnk_ zurückgegebenen Zeiger in einen Zeiger des entsprechenden Typs um. 
  
Standardmäßig öffnen Dienstanbieter Objekte mit schreibgeschütztem Zugriff, es sei denn, Sie legen das MAPI_MODIFY-oder MAPI_BEST_ACCESS-Flag fest. Wenn eines dieser Flags festgelegt ist, versuchen Dienstanbieter, ein änderbares Objekt zurückzugeben. Sie sollten jedoch nicht davon ausgehen, dass Sie ein änderbares Objekt angefordert haben, dass das geöffnete Objekt Lese-/Schreibzugriff hat. Planen Sie entweder, ob eine spätere Änderung fehlschlagen soll, oder rufen Sie die **PR_ACCESS_LEVEL** -Eigenschaft des Objekts ab, um die **** von OpenEntry erteilte Zugriffsebene zu bestimmen.
  
## <a name="see-also"></a>Siehe auch



[IMAPIContainer : IMAPIProp](imapicontainerimapiprop.md)

