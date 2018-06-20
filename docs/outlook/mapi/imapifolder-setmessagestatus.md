---
title: IMAPIFolderSetMessageStatus
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFolder.SetMessageStatus
api_type:
- COM
ms.assetid: 42ffbbe0-d678-474a-a016-91c71255613e
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: fcca6a7e8fa70a2df9042e8b3c2b28825cee9a7b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792124"
---
# <a name="imapifoldersetmessagestatus"></a>IMAPIFolder::SetMessageStatus

  
  
**Betrifft**: Outlook 
  
Setzt den Status einer Nachricht zugeordneten (z. B., ob die Nachricht zum Löschen markiert ist).
  
```cpp
HRESULT SetMessageStatus(
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  ULONG ulNewStatus,
  ULONG ulNewStatusMask,
  ULONG FAR * lpulOldStatus
);
```

## <a name="parameters"></a>Parameter

 _cbEntryID_
  
> [in] Die Byteanzahl von in die Eintrags-ID auf den durch den Parameter _LpEntryID_ verwiesen. 
    
 _lpEntryID_
  
> [in] Ein Zeiger auf die Eintrags-ID für die Nachricht, deren Status festgelegt ist.
    
 _ulNewStatus_
  
> [in] Der neue Status zugewiesen werden soll. 
    
 _ulNewStatusMask_
  
> [in] Eine Bitmaske aus Flags, die auf den neuen Status angewendet wird und der zu protokollierenden festgelegt werden soll. Die folgenden Kennzeichen können festgelegt werden:
    
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
    
 _lpulOldStatus_
  
> [out] Ein Zeiger auf den vorherigen Status der Nachricht.
    
## <a name="return-value"></a>R�ckgabewert

S_OK 
  
> Der Nachrichtenstatus wurde erfolgreich festgelegt.
    
## <a name="remarks"></a>Hinweise

Die **IMAPIFolder::SetMessageStatus** -Methode wird die Nachricht den Status auf den Wert, der in dessen **PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md))-Eigenschaft gespeichert ist. 
  
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Wie die Nachricht Statusbits festgelegt, gelöscht und verwendet werden, hängt vollständig die Implementierung mit der Ausnahme, dass Bits 0 bis 15 reserviert sind und müssen null sein. 
  
Eine remote Adressbuchhierarchie Implementierung dieser Methode muss der hier beschriebenen Semantik folgen. Es gibt keine besondere Aspekte. Clients mit dieser Methode können Sie legen die Bits MSGSTATUS_REMOTE_DOWNLOAD und MSGSTATUS_REMOTE_DELETE, um anzugeben, dass eine bestimmte Nachricht wird heruntergeladen oder vom remote Nachrichtenspeicher gelöscht werden soll. Eine remote Adressbuchhierarchie hat keinen implementieren die verwandte [IMAPIFolder::GetMessageStatus](imapifolder-getmessagestatus.md) -Methode. Clients müssen Suchen in den Ordner Inhaltstabelle zum Bestimmen des Status einer Nachricht. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Die **PR_MSG_STATUS** -Eigenschaft einer Nachricht können Sie einen Nachricht Sperrung Vorgang mit anderen Clients aushandeln. Etwas als die Sperrung Bit bestimmen. Um zu bestimmen, ob das Sperrung Bit festgelegt wurde, untersuchen Sie den vorherigen Wert für Nachrichtenstatus im _LpulOldStatus_ -Parameter. Verwenden Sie die anderen Bits im _UlNewStatus_ -Parameter Nachrichtenstatus verfolgen, ohne eine Störung der Sperrung Bit. 
  
## <a name="see-also"></a>Siehe auch



[IMAPIFolder::GetMessageStatus](imapifolder-getmessagestatus.md)
  
[Kanonische PidTagMessageStatus-Eigenschaft](pidtagmessagestatus-canonical-property.md)
  
[IMAPIFolder: IMAPIContainer](imapifolderimapicontainer.md)

