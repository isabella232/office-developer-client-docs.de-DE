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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: ab4a06a20c71943f9b649d8f22377f59223e9717
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430126"
---
# <a name="imapimessagesitegetsitestatus"></a>IMAPIMessageSite::GetSiteStatus

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Gibt Informationen von einem Nachrichtenwebsiteobjekt zu den Funktionen der Nachrichtenwebsite für die aktuelle Nachricht zurück.
  
```cpp
HRESULT GetSiteStatus(
  ULONG FAR * lpulStatus
);
```

## <a name="parameters"></a>Parameter

 _lpulStatus_
  
> [out] Ein Zeiger auf eine Bitmaske mit Flags, die Informationen zum Nachrichtenstatus enthält. Die folgenden Kennzeichen können festgelegt werden:
    
VCSTATUS_COPY 
  
> Die Nachricht kann kopiert werden. 
    
VCSTATUS_DELETE 
  
> Die Nachricht kann gelöscht werden.
    
VCSTATUS_DELETE_IS_MOVE 
  
> Beim Löschen wird eine Nachricht in einen Ordner **"Gelöschte** Elemente" im Nachrichtenspeicher verschoben, anstatt sofort aus dem Nachrichtenspeicher entfernt zu werden. 
    
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
    
## <a name="remarks"></a>Hinweise

Form-Objekte rufen die **IMAPIMessageSite::GetSiteStatus-Methode** auf, um die Funktionen des Nachrichtenwebsiteobjekts für die aktuelle Nachricht zu erhalten. Die im  _lpulStatus-Parameter_ zurückgegebenen Flags enthalten Informationen zur Nachrichtenwebsite. In der Regel aktiviert oder deaktiviert ein Formular Menübefehle, abhängig von den Informationen, die die Flags zu den Funktionen der Nachrichtenwebsiteimplementierung bereitstellen. Wenn eine neue Nachricht von der [IPersistMessage::SaveCompleted-Methode](ipersistmessage-savecompleted.md) oder der [IPersistMessage::Load-Methode](ipersistmessage-load.md) in ein Formular geladen wird, müssen die Statusflags überprüft werden. Einige Nachrichtenwebsiteobjekte, insbesondere schreibgeschützte Objekte, lassen das Speichern oder Löschen von Nachrichten nicht zu. 
  
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Die **IMAPIMessageSite::GetSiteStatus-Methode** erfordert möglicherweise, dass die Clientanwendung eine Berechnung vor sich hat, um zu bestimmen, welche Vorgänge für die aktuelle Nachricht ausgeführt werden können oder nicht. In der Regel umfasst dies das Überprüfen der Statuszeile für den Nachrichtenspeicheranbieter der aktuellen Nachricht oder das Abfragen des Speicheranbieters, um zu bestimmen, welche Aktionen die Clientanwendung mithilfe des Nachrichtenspeichers ausführen kann. Um z. B. zu ermitteln, ob das flag MAPI_DELETE_IS_MOVE zurückgeben soll, überprüfen Sie die **PR_IPM_WASTEBASKET_ENTRYID** ([PidTagIpmWastebasketEntryId](pidtagipmwastebasketentryid-canonical-property.md))-Eigenschaft des Nachrichtenspeicherobjekts, um festzustellen, ob im Nachrichtenspeicher ein Ordner **"Gelöschte** Elemente" enthalten ist. 
  
Eine Liste der Schnittstellen im Zusammenhang mit Formularservern finden Sie unter [MAPI Form Interfaces](mapi-form-interfaces.md).
  
## <a name="mfcmapi-reference"></a>MFCMAPI-Referenz

Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|MyMAPIFormViewer.cpp  <br/> |CMyMAPIFormViewer::GetSiteStatus  <br/> |MFCMAPI verwendet die **IMAPIMessageSite::GetSiteStatus-Methode,** um den Status der angegebenen Website zu erhalten. Es kann VCSTATUS_NEW_MESSAGE, VCSTATUS_SAVE oder VCSTATUS_SUBMIT.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[IPersistMessage::Load](ipersistmessage-load.md)
  
[IPersistMessage::SaveCompleted](ipersistmessage-savecompleted.md)
  
[PidTagIpmWastebasketEntryId (kanonische Eigenschaft)](pidtagipmwastebasketentryid-canonical-property.md)
  
[IMAPIMessageSite : IUnknown](imapimessagesiteiunknown.md)


[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)
  
[MAPI-Formularschnittstellen](mapi-form-interfaces.md)

