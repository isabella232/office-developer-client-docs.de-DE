---
title: IMAPIMessageSiteGetSiteStatus
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIMessageSite.GetSiteStatus
api_type:
- COM
ms.assetid: 02718898-7857-4e43-8f46-622269f812e6
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: ab4a06a20c71943f9b649d8f22377f59223e9717
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32355811"
---
# <a name="imapimessagesitegetsitestatus"></a>IMAPIMessageSite::GetSiteStatus

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Gibt Informationen aus einem Nachrichtenwebsite Objekt über die Funktionen der Nachrichtenwebsite für die aktuelle Nachricht zurück.
  
```cpp
HRESULT GetSiteStatus(
  ULONG FAR * lpulStatus
);
```

## <a name="parameters"></a>Parameter

 _lpulStatus_
  
> Out Ein Zeiger auf eine Bitmaske von Flags, die Informationen zum Status der Nachricht bereitstellt. Die folgenden Flags können festgelegt werden:
    
VCSTATUS_COPY 
  
> Die Nachricht kann kopiert werden. 
    
VCSTATUS_DELETE 
  
> Die Nachricht kann gelöscht werden.
    
VCSTATUS_DELETE_IS_MOVE 
  
> Nach dem Löschen wird eine Nachricht in einen Ordner " **Gelöschte Elemente** " im Nachrichtenspeicher verschoben, anstatt Sie sofort aus dem Nachrichtenspeicher zu entfernen. 
    
VCSTATUS_MOVE 
  
> Die Nachricht kann verschoben werden.
    
VCSTATUS_NEW_MESSAGE 
  
> Eine neue Nachricht kann erstellt werden.
    
VCSTATUS_SAVE 
  
> Die Nachricht kann gespeichert werden.
    
VCSTATUS_SUBMIT 
  
> Die Nachricht kann übermittelt werden.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.
    
## <a name="remarks"></a>Bemerkungen

Formularobjekte rufen die **IMAPIMessageSite:: GetSiteStatus** -Methode auf, um die Funktionen des Nachrichtenwebsite Objekts für die aktuelle Nachricht abzurufen. Die im Parameter _lpulStatus_ zurückgegebenen Flags enthalten Informationen zur Nachrichtenwebsite. In der Regel aktiviert oder deaktiviert ein Formular Menübefehle, je nachdem, welche Informationen die Flags über die Funktionen der Nachrichtenwebsite Implementierung bereitstellen. Wenn eine neue Nachricht von der [IPersistMessage:: SaveCompleted](ipersistmessage-savecompleted.md) -Methode oder der [IPersistMessage:: Laden](ipersistmessage-load.md) -Methode in ein Formular geladen wird, müssen die Status-Flags überprüft werden. Bei einigen Nachrichtenwebsite Objekten, insbesondere schreibgeschützten Objekten, können keine Nachrichten gespeichert oder gelöscht werden. 
  
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Die **IMAPIMessageSite:: GetSiteStatus** -Methode erfordert möglicherweise eine Berechnung der Clientanwendung, um zu bestimmen, welche Vorgänge für die aktuelle Nachricht ausgeführt werden können. In der Regel müssen Sie sich die Statuszeile des Nachrichtenspeicher Anbieters der aktuellen Nachricht ansehen oder den Speicheranbieter Abfragen, um zu bestimmen, welche Aktionen die Clientanwendung mithilfe des Nachrichtenspeichers ausführen kann. Um beispielsweise zu bestimmen, ob das MAPI_DELETE_IS_MOVE-Flag zurückgegeben werden soll, überprüfen Sie die **PR_IPM_WASTEBASKET_ENTRYID** ([pidtagipmwastebasketentryid (](pidtagipmwastebasketentryid-canonical-property.md))-Eigenschaft des Nachrichtenspeicher Objekts, um festzustellen, ob ein Ordner " **Gelöschte Elemente** " in der Nachrichtenspeicher. 
  
Eine Liste der Schnittstellen im Zusammenhang mit Formular Servern finden Sie unter [MAPI-Formular Schnittstellen](mapi-form-interfaces.md).
  
## <a name="mfcmapi-reference"></a>MFCMAPI-Referenz

Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|MyMAPIFormViewer. cpp  <br/> |CMyMAPIFormViewer:: GetSiteStatus  <br/> |MFCMAPI verwendet die **IMAPIMessageSite:: GetSiteStatus** -Methode, um den Status der angegebenen Website abzurufen. Es kann VCSTATUS_NEW_MESSAGE, VCSTATUS_SAVE oder VCSTATUS_SUBMIT zurückgeben.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[IPersistMessage::Load](ipersistmessage-load.md)
  
[IPersistMessage::SaveCompleted](ipersistmessage-savecompleted.md)
  
[Kanonische Pidtagipmwastebasketentryid (-Eigenschaft](pidtagipmwastebasketentryid-canonical-property.md)
  
[IMAPIMessageSite : IUnknown](imapimessagesiteiunknown.md)


[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)
  
[MAPI-Formular Schnittstellen](mapi-form-interfaces.md)

