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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342777"
---
# <a name="imapifoldersetmessagestatus"></a>IMAPIFolder::SetMessageStatus

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Legt den Status fest, der einer Nachricht zugeordnet ist (beispielsweise, ob diese Nachricht zum Löschen markiert ist).
  
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
  
> in Die Anzahl der Bytes in der Eintrags-ID, auf die durch den _lpEntryID_ -Parameter verwiesen wird. 
    
 _lpEntryID_
  
> in Ein Zeiger auf die Eintrags-ID für die Nachricht, deren Status festgelegt ist.
    
 _ulNewStatus_
  
> in Der neue Status, der zugewiesen werden soll. 
    
 _ulNewStatusMask_
  
> in Eine Bitmaske von Flags, die auf den neuen Status angewendet wird und die festzulegenden Flags angibt. Die folgenden Flags können festgelegt werden:
    
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
    
 _lpulOldStatus_
  
> Out Ein Zeiger auf den vorherigen Status der Nachricht.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Nachrichtenstatus wurde erfolgreich festgelegt.
    
## <a name="remarks"></a>Bemerkungen

Die **IMAPIFolder:: SetMessageStatus** -Methode legt den Status der Nachricht auf den Wert fest, der in seiner **PR_MSG_STATUS** ([pidtagmessagestatus (](pidtagmessagestatus-canonical-property.md))-Eigenschaft gespeichert ist. 
  
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Wie die Nachrichtenstatus-Bits festgelegt, gelöscht und verwendet werden, hängt vollständig von der Implementierung ab, mit der Ausnahme, dass die Bits 0 bis 15 reserviert sind und 0 (null) sein müssen. 
  
Die Implementierung dieser Methode durch einen Remote Transportanbieter muss die hier beschriebene Semantik befolgen. Besondere Überlegungen sind nicht möglich. Clients verwenden diese Methode, um die Bits MSGSTATUS_REMOTE_DOWNLOAD und MSGSTATUS_REMOTE_DELETE festzulegen, um anzugeben, dass eine bestimmte Nachricht heruntergeladen oder aus dem Remote Nachrichtenspeicher gelöscht werden soll. Ein Remote Transportanbieter muss die zugehörige [IMAPIFolder:: GetMessageStatus](imapifolder-getmessagestatus.md) -Methode nicht implementieren. Clients müssen in der Tabelle Inhalt des Ordners suchen, um den Status einer Nachricht zu bestimmen. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Sie können die **PR_MSG_STATUS** -Eigenschaft einer Nachricht verwenden, um einen Nachrichten Sperrvorgang mit anderen Clients auszuhandeln. Benennen Sie ein Bit als Lockout-Bit. Um zu bestimmen, ob das Lockout-Bit festgelegt wurde, überprüfen Sie den vorherigen Wert für Nachrichtenstatus im _lpulOldStatus_ -Parameter. Verwenden Sie die anderen Bits im _ulNewStatus_ -Parameter, um den Nachrichtenstatus nachzuverfolgen, ohne das Lockout-Bit zu stören. 
  
## <a name="see-also"></a>Siehe auch



[IMAPIFolder::GetMessageStatus](imapifolder-getmessagestatus.md)
  
[Kanonische Pidtagmessagestatus (-Eigenschaft](pidtagmessagestatus-canonical-property.md)
  
[IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md)

