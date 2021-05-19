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
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: fbb05efff67fa90c68db86249d4657e489e7bd63
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417273"
---
# <a name="imapifoldersetmessagestatus"></a>IMAPIFolder::SetMessageStatus

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Legt den Status fest, der einer Nachricht zugeordnet ist (z. B. ob diese Nachricht zum Löschen markiert ist).
  
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
  
> [in] Die Byteanzahl im Eintragsbezeichner, auf den der  _lpEntryID-Parameter_ verweist. 
    
 _lpEntryID_
  
> [in] Ein Zeiger auf die Eintrags-ID für die Nachricht, deren Status festgelegt ist.
    
 _ulNewStatus_
  
> [in] Der neue Status, der zugewiesen werden soll. 
    
 _ulNewStatusMask_
  
> [in] Eine Bitmaske mit Flags, die auf den neuen Status angewendet wird und die festgelegten Flags angibt. Die folgenden Kennzeichen können festgelegt werden:
    
MSGSTATUS_DELMARKED 
  
> Die Nachricht wurde zum Löschen markiert.
    
MSGSTATUS_HIDDEN 
  
> Die Nachricht soll nicht angezeigt werden.
    
MSGSTATUS_HIGHLIGHTED 
  
> Die Nachricht soll hervorgehoben angezeigt werden.
    
MSGSTATUS_REMOTE_DELETE 
  
> Die Nachricht wurde zum Löschen im Remotenachrichtenspeicher ohne Download auf den lokalen Client markiert.
    
MSGSTATUS_REMOTE_DOWNLOAD 
  
> Die Nachricht wurde zum Herunterladen aus dem Remotenachrichtenspeicher auf den lokalen Client markiert.
    
MSGSTATUS_TAGGED 
  
> Die Nachricht wurde für einen clientdefinierten Zweck markiert.
    
 _lpulOldStatus_
  
> [out] Ein Zeiger auf den vorherigen Status der Nachricht.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Nachrichtenstatus wurde erfolgreich festgelegt.
    
## <a name="remarks"></a>Hinweise

Die **IMAPIFolder::SetMessageStatus-Methode** legt den Nachrichtenstatus auf den Wert fest, der in der PR_MSG_STATUS ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) **-Eigenschaft** gespeichert ist. 
  
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Wie die Nachrichtenstatusbits festgelegt, geräumt und verwendet werden, hängt vollständig von Ihrer Implementierung ab, mit der Ausnahme, dass bits 0 bis 15 reserviert sind und null sein müssen. 
  
Die Implementierung dieser Methode durch einen Remotetransportanbieter muss der hier beschriebenen Semantik folgen. Es gibt keine besonderen Überlegungen. Clients verwenden diese Methode, um die bits MSGSTATUS_REMOTE_DOWNLOAD und MSGSTATUS_REMOTE_DELETE anzugeben, dass eine bestimmte Nachricht heruntergeladen oder aus dem Remotenachrichtenspeicher gelöscht werden soll. Ein Remotetransportanbieter muss die zugehörige [IMAPIFolder::GetMessageStatus-Methode](imapifolder-getmessagestatus.md) nicht implementieren. Clients müssen in der Inhaltstabelle des Ordners suchen, um den Status einer Nachricht zu bestimmen. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Sie können die **PR_MSG_STATUS** einer Nachricht verwenden, um einen Nachrichtensperrungsvorgang mit anderen Clients auszuhandeln. Geben Sie ein Bit als Sperrbit an. Um zu ermitteln, ob das Sperrbit festgelegt wurde, untersuchen Sie den vorherigen Wert für den Nachrichtenstatus im _lpulOldStatus-Parameter._ Verwenden Sie die anderen Bits im  _ulNewStatus-Parameter,_ um den Nachrichtenstatus nachverfolgt zu haben, ohne das Sperrbit zu stören. 
  
## <a name="see-also"></a>Siehe auch



[IMAPIFolder::GetMessageStatus](imapifolder-getmessagestatus.md)
  
[PidTagMessageStatus (kanonische Eigenschaft)](pidtagmessagestatus-canonical-property.md)
  
[IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md)

