---
title: IMAPIFolderGetMessageStatus
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPIFolder.GetMessageStatus
api_type:
- COM
ms.assetid: 3ddbb129-5d6b-4eca-aba0-3620609ed0c1
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 762935b5e569dd63399862f32945599c0dc5df09
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59571807"
---
# <a name="imapifoldergetmessagestatus"></a>IMAPIFolder::GetMessageStatus

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Ruft den Status ab, der einer Nachricht in einem bestimmten Ordner zugeordnet ist (z. B. ob diese Nachricht zum Löschen markiert ist).
  
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
  
> [in] Die Byteanzahl im Eintragsbezeichner, auf den der  _lpEntryID-Parameter_ verweist. 
    
 _lpEntryID_
  
> [in] Ein Zeiger auf den Eintragsbezeichner für die Nachricht, deren Status abgerufen wird.
    
 _ulFlags_
  
> [in] Reserviert. NULL muss sein.
    
 _lpulMessageStatus_
  
> [out] Ein Zeiger auf einen Zeiger auf eine Bitmaske mit Flags, die den Status der Nachricht angeben. Bits 0 bis 15 sind reserviert und müssen null sein; Die Bits 16 bis 31 stehen für die implementierungsspezifische Verwendung zur Verfügung. Die folgenden Flags können festgelegt werden:
    
MSGSTATUS_DELMARKED 
  
> Die Nachricht wurde zum Löschen markiert.
    
MSGSTATUS_HIDDEN 
  
> Die Meldung soll nicht angezeigt werden. 
    
MSGSTATUS_HIGHLIGHTED 
  
> Die Meldung wird hervorgehoben angezeigt.
    
MSGSTATUS_REMOTE_DELETE 
  
> Die Nachricht wurde für den Löschvorgang im Remotenachrichtenspeicher markiert, ohne sie auf den lokalen Client herunterzuladen.
    
MSGSTATUS_REMOTE_DOWNLOAD 
  
> Die Nachricht wurde zum Herunterladen aus dem Remotenachrichtenspeicher auf den lokalen Client markiert.
    
MSGSTATUS_TAGGED 
  
> Die Nachricht wurde für einen clientdefinierten Zweck markiert.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Nachrichtenstatus wurde erfolgreich abgerufen.
    
## <a name="remarks"></a>HinwBemerkungeneise

Die **IMAPIFolder::GetMessageStatus-Methode** gibt den Status einer Nachricht zurück. Der Nachrichtenstatus wird in der **eigenschaft PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) der Nachricht gespeichert. 
  
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Wie die Nachrichtenstatusbits festgelegt, gelöscht und verwendet werden, hängt vollständig von Ihrer Implementierung ab, mit der Ausnahme, dass die Bits 0 bis 15 reserviert sind und null sein müssen. Wenn Sie Nachrichten in der IPM-Unterstruktur speichern, reserviert MAPI bits 16 bis 31 für die Verwendung durch IPM-Clients. Wenn Sie Nachrichten in anderen Unterstrukturen speichern, können Sie die Bits 16 bis 31 für Eigene Zwecke verwenden.
  
## <a name="mfcmapi-reference"></a>MFCMAPI-Referenz

Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|MyMAPIFormViewer.cpp  <br/> |CMyMAPIFormViewer::GetNextMessage  <br/> |MFCMAPI verwendet die **IMAPIFolder::GetMessageStatus-Methode,** um den Status der nächsten anzuzeigenden Nachricht abzurufen.  <br/> |
|MAPIFormFunctions.cpp  <br/> |OpenMessageNonModal und OpenMessageModal  <br/> |MFCMAPI verwendet die **IMAPIFolder::GetMessageStatus-Methode,** um den Status der anzuzeigenden Nachricht abzurufen, die an die Formularanzeige übergeben werden soll, bei der es sich entweder um CMyMAPIFormViewer oder [IMAPISession::ShowForm handelt.](imapisession-showform.md)  <br/> |
   
## <a name="see-also"></a>Siehe auch



[IMAPIFolder::SetMessageStatus](imapifolder-setmessagestatus.md)
  
[IMAPISession::ShowForm](imapisession-showform.md)
  
[PidTagMessageStatus (kanonische Eigenschaft)](pidtagmessagestatus-canonical-property.md)
  
[IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md)


[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)

