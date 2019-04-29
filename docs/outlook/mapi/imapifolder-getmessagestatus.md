---
title: IMAPIFolderGetMessageStatus
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFolder.GetMessageStatus
api_type:
- COM
ms.assetid: 3ddbb129-5d6b-4eca-aba0-3620609ed0c1
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 621c20376cc671a2ff9d1406bfb6248846e1bc81
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418638"
---
# <a name="imapifoldergetmessagestatus"></a>IMAPIFolder::GetMessageStatus

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Ruft den Status ab, der einer Nachricht in einem bestimmten Ordner zugeordnet ist (beispielsweise, ob diese Nachricht zum Löschen markiert ist).
  
```cpp
HRESULT GetMessageStatus(
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  ULONG ulFlags,
  ULONG FAR * lpulMessageStatus
);
```

## <a name="parameters"></a>Parameter

 _cbEntryID_
  
> in Die Anzahl der Bytes in der Eintrags-ID, auf die durch den _lpEntryID_ -Parameter verwiesen wird. 
    
 _lpEntryID_
  
> in Ein Zeiger auf die Eintrags-ID für die Nachricht, deren Status abgerufen wird.
    
 _ulFlags_
  
> [in] Reserviert. NULL muss sein.
    
 _lpulMessageStatus_
  
> Out Ein Zeiger auf einen Zeiger auf eine Bitmaske von Flags, die den Status der Nachricht anzeigen. Die Bits 0 bis 15 sind reserviert und müssen NULL sein; Bits 16 bis 31 sind für die implementierungsspezifische Verwendung verfügbar. Die folgenden Flags können festgelegt werden:
    
MSGSTATUS_DELMARKED 
  
> Die Nachricht wurde zum Löschen markiert.
    
MSGSTATUS_HIDDEN 
  
> Die Nachricht soll nicht angezeigt werden. 
    
MSGSTATUS_HIGHLIGHTED 
  
> Die Nachricht wird hervorgehoben angezeigt.
    
MSGSTATUS_REMOTE_DELETE 
  
> Die Nachricht wurde zum Löschen im Remotenachrichtenspeicher markiert, ohne Sie auf den lokalen Client herunterzuladen.
    
MSGSTATUS_REMOTE_DOWNLOAD 
  
> Die Nachricht wurde zum Herunterladen aus dem Remotenachrichtenspeicher auf den lokalen Client markiert.
    
MSGSTATUS_TAGGED 
  
> Die Nachricht wurde für einen Client definierten Zweck markiert.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Nachrichtenstatus wurde erfolgreich abgerufen.
    
## <a name="remarks"></a>Bemerkungen

Die **IMAPIFolder:: GetMessageStatus** -Methode gibt den Status einer Nachricht zurück. Der Nachrichtenstatus wird in der **PR_MSG_STATUS** ([pidtagmessagestatus (](pidtagmessagestatus-canonical-property.md))-Eigenschaft der Nachricht gespeichert. 
  
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Wie die Nachrichtenstatus-Bits festgelegt, gelöscht und verwendet werden, hängt vollständig von der Implementierung ab, mit der Ausnahme, dass die Bits 0 bis 15 reserviert sind und 0 (null) sein müssen. Wenn Sie Nachrichten in der IPM-Unterstruktur speichern, werden die Bits 16 bis 31 für die Verwendung durch IPM-Clients reserviert. Wenn Sie Nachrichten in anderen unter Strukturen speichern, können Sie die Bits 16 bis 31 für eigene Zwecke verwenden.
  
## <a name="mfcmapi-reference"></a>MFCMAPI-Referenz

Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|MyMAPIFormViewer. cpp  <br/> |CMyMAPIFormViewer:: GetNextMessage  <br/> |MFCMAPI verwendet die **IMAPIFolder:: GetMessageStatus** -Methode, um den Status der nächsten Nachricht abzurufen, die angezeigt werden soll.  <br/> |
|MAPIFormFunctions. cpp  <br/> |OpenMessageNonModal und OpenMessageModal  <br/> |MFCMAPI verwendet die **IMAPIFolder:: GetMessageStatus** -Methode, um den Status der Meldung anzuzeigen, die an den Formular Betrachter weitergegeben werden soll, der entweder CMyMAPIFormViewer oder [IMAPISession:: ShowForm](imapisession-showform.md)ist.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[IMAPIFolder::SetMessageStatus](imapifolder-setmessagestatus.md)
  
[IMAPISession::ShowForm](imapisession-showform.md)
  
[Kanonische Pidtagmessagestatus (-Eigenschaft](pidtagmessagestatus-canonical-property.md)
  
[IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md)


[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)

