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
ms.openlocfilehash: 7d81533b13f4f44a0644215e009dc3477717e9a2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792215"
---
# <a name="imapimessagesitegetsitestatus"></a>IMAPIMessageSite::GetSiteStatus

  
  
**Betrifft**: Outlook 
  
Gibt Informationen aus einem Objekt "Message" Website zur Nachricht der Website Funktionen für die aktuelle Nachricht zurück.
  
```cpp
HRESULT GetSiteStatus(
  ULONG FAR * lpulStatus
);
```

## <a name="parameters"></a>Parameter

 _lpulStatus_
  
> [out] Ein Zeiger auf eine Bitmaske aus Flags, die Informationen zum Nachrichtenstatus bereitstellt. Die folgenden Kennzeichen können festgelegt werden:
    
VCSTATUS_COPY 
  
> Die Nachricht kann kopiert werden. 
    
VCSTATUS_DELETE 
  
> Die Nachricht kann gelöscht werden.
    
VCSTATUS_DELETE_IS_MOVE 
  
> Wenn gelöscht, wird eine Meldung in einem Ordner **Gelöschte Elemente** in den Nachrichtenspeicher anstelle von den Nachrichtenspeicher sofort entfernt wird verschoben. 
    
VCSTATUS_MOVE 
  
> Die Nachricht kann verschoben werden.
    
VCSTATUS_NEW_MESSAGE 
  
> Eine neue Nachricht kann erstellt werden.
    
VCSTATUS_SAVE 
  
> Die Nachricht kann gespeichert werden.
    
VCSTATUS_SUBMIT 
  
> Die Nachricht kann gesendet werden.
    
## <a name="return-value"></a>R�ckgabewert

S_OK 
  
> Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.
    
## <a name="remarks"></a>Hinweise

Formularobjekte Aufrufen die **IMAPIMessageSite::GetSiteStatus** -Methode, um die Nachricht Standortobjekt Funktionen für die aktuelle Nachricht zu erhalten. Die Kennzeichen, die in der _LpulStatus_ -Parameter zurückgegeben liefern Informationen zur Nachricht-Website. In der Regel ein Formular aktiviert oder deaktiviert die Menübefehle, je nach Informationen, die die Kennzeichen bereitstellen zu den Funktionen der Nachricht Website-Implementierung. Wenn eine neue Nachricht durch die [IPersistMessage::SaveCompleted](ipersistmessage-savecompleted.md) -Methode oder die [IPersistMessage::Load](ipersistmessage-load.md) -Methode in einem Formular geladen wird, müssen die Status-Kennzeichen überprüft werden soll. Einige Nachricht Websiteobjekte, insbesondere schreibgeschützt, lassen Sie nicht Nachrichten gespeichert oder gelöscht werden soll. 
  
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Die Methode **IMAPIMessageSite::GetSiteStatus** erfordern möglicherweise die Client-Anwendung, um zu bestimmen, welche Vorgänge können oder nicht auf die aktuelle Nachricht durchgeführt werden einige Berechnung ausführen. In der Regel, die umfasst die Statuszeile für die aktuelle Nachricht Nachricht Speicheranbieter betrachten oder den Anbieter anmelden, um zu bestimmen, welche Aktionen Abfragen kann die Client-Anwendung mithilfe des Nachrichtenspeichers ausführen. Überprüfen Sie beispielsweise um festzustellen, ob das Flag MAPI_DELETE_IS_MOVE zurückzugeben, das Nachricht Store-Objekt **PR_IPM_WASTEBASKET_ENTRYID** ([PidTagIpmWastebasketEntryId](pidtagipmwastebasketentryid-canonical-property.md))-Eigenschaft, um festzustellen, ob es ein Ordner **Gelöschte Elemente** in ist der Nachrichtenspeicher. 
  
Eine Liste der Schnittstellen im Zusammenhang mit der Formular-Servern finden Sie unter [MAPI-Formulars Schnittstellen](mapi-form-interfaces.md).
  
## <a name="mfcmapi-reference"></a>MFCMAPI (engl.) (engl.)

Beispielcode MFCMAPI (engl.) finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|MyMAPIFormViewer.cpp  <br/> |CMyMAPIFormViewer::GetSiteStatus  <br/> |MFCMAPI (engl.) verwendet die **IMAPIMessageSite::GetSiteStatus** -Methode, um den Status der angegebenen Website zu erhalten. Es kann VCSTATUS_NEW_MESSAGE, VCSTATUS_SAVE oder VCSTATUS_SUBMIT zurückgeben.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[IPersistMessage::Load](ipersistmessage-load.md)
  
[IPersistMessage::SaveCompleted](ipersistmessage-savecompleted.md)
  
[Kanonische PidTagIpmWastebasketEntryId-Eigenschaft](pidtagipmwastebasketentryid-canonical-property.md)
  
[IMAPIMessageSite: IUnknown](imapimessagesiteiunknown.md)


[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)
  
[MAPI-Formulars Schnittstellen](mapi-form-interfaces.md)

