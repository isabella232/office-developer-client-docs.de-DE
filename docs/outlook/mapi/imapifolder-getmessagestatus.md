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
ms.openlocfilehash: 8e5ccadbd6df664b6650487f340508ae4548a1c2
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22583267"
---
# <a name="imapifoldergetmessagestatus"></a>IMAPIFolder::GetMessageStatus

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Ruft den Status einer Nachricht in einem bestimmten Ordner zugeordnet, (z. B., ob die Nachricht zum Löschen markiert ist).
  
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
  
> [in] Die Byteanzahl von in die Eintrags-ID auf den durch den Parameter _LpEntryID_ verwiesen. 
    
 _lpEntryID_
  
> [in] Ein Zeiger auf die Eintrags-ID für die Nachricht, deren Status abgerufen wird.
    
 _ulFlags_
  
> [in] Reserviert. NULL muss sein.
    
 _lpulMessageStatus_
  
> [out] Ein Zeiger auf einen Zeiger auf eine Bitmaske aus Flags, die die Nachricht Status angeben. Bits 0 bis 15 sind reserviert und müssen null sein. 16 bis 31 Bits sind für die Verwendung von implementierungsspezifischen verfügbar. Die folgenden Kennzeichen können festgelegt werden:
    
MSGSTATUS_DELMARKED 
  
> Die Nachricht wurde zum Löschen markiert wurden.
    
MSGSTATUS_HIDDEN 
  
> Die Nachricht wird nicht angezeigt werden. 
    
MSGSTATUS_HIGHLIGHTED 
  
> Die Nachricht anzuzeigen ist hervorgehoben.
    
MSGSTATUS_REMOTE_DELETE 
  
> Die Nachricht wurde zum Löschen auf die entfernten Nachrichtenspeicher markiert, ohne dass auf dem lokalen Client heruntergeladen.
    
MSGSTATUS_REMOTE_DOWNLOAD 
  
> Die Nachricht wurde für das Herunterladen aus dem remote Nachrichtenspeicher auf dem lokalen Client markiert.
    
MSGSTATUS_TAGGED 
  
> Für einen Client definierten Zweck hat die Nachricht markiert wurde.
    
## <a name="return-value"></a>R�ckgabewert

S_OK 
  
> Die Nachricht den Status wurde erfolgreich abgerufen.
    
## <a name="remarks"></a>HinwBemerkungeneise

Die **IMAPIFolder::GetMessageStatus** -Methode gibt den Status einer Nachricht. Nachrichtenstatus wird in der Nachricht **PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md))-Eigenschaft gespeichert. 
  
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Wie die Nachricht Statusbits festgelegt, gelöscht und verwendet werden, hängt vollständig die Implementierung mit der Ausnahme, dass Bits 0 bis 15 reserviert sind und müssen null sein. Wenn Sie Nachrichten in der IPM-Unterstruktur speichern, reserviert MAPI Bits 16 bis 31 für die Verwendung durch Clients IPM. Wenn Sie Nachrichten in anderen Unterstrukturen speichern, können Sie Bits 16 bis 31 für eigene Zwecke.
  
## <a name="mfcmapi-reference"></a>MFCMAPI (engl.) (engl.)

Beispielcode MFCMAPI (engl.) finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|MyMAPIFormViewer.cpp  <br/> |CMyMAPIFormViewer::GetNextMessage  <br/> |MFCMAPI (engl.) verwendet die **IMAPIFolder::GetMessageStatus** -Methode, um den Status der nächsten Nachricht anzuzeigende abzurufen.  <br/> |
|MAPIFormFunctions.cpp  <br/> |OpenMessageNonModal und OpenMessageModal  <br/> |MFCMAPI (engl.) verwendet die **IMAPIFolder::GetMessageStatus** -Methode zum Abrufen des Status der Nachricht angezeigt werden, für den Betrachter Formular zu übergeben, CMyMAPIFormViewer oder [IMAPISession::ShowForm](imapisession-showform.md)ist.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[IMAPIFolder::SetMessageStatus](imapifolder-setmessagestatus.md)
  
[IMAPISession::ShowForm](imapisession-showform.md)
  
[PidTagMessageStatus (kanonische Eigenschaft)](pidtagmessagestatus-canonical-property.md)
  
[IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md)


[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)

