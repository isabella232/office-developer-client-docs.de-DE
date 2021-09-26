---
title: IMAPIFolderSetMessageStatus
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPIFolder.SetMessageStatus
api_type:
- COM
ms.assetid: 42ffbbe0-d678-474a-a016-91c71255613e
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 8514a24ebe56d1ae533b4f2b247a34a9f7d7c8e5
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59610636"
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
  
> [in] Ein Zeiger auf den Eintragsbezeichner für die Nachricht, deren Status festgelegt ist.
    
 _ulNewStatus_
  
> [in] Der neue Zuzuweisende Status. 
    
 _ulNewStatusMask_
  
> [in] Eine Bitmaske mit Flags, die auf den neuen Status angewendet wird und die festzulegenden Flags angibt. Die folgenden Flags können festgelegt werden:
    
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
    
 _lpulOldStatus_
  
> [out] Ein Zeiger auf den vorherigen Status der Nachricht.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Nachrichtenstatus wurde erfolgreich festgelegt.
    
## <a name="remarks"></a>HinwBemerkungeneise

The **IMAPIFolder::SetMessageStatus** method sets the message status to the value that is stored in its **PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) property. 
  
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Wie die Nachrichtenstatusbits festgelegt, gelöscht und verwendet werden, hängt vollständig von Ihrer Implementierung ab, mit der Ausnahme, dass die Bits 0 bis 15 reserviert sind und null sein müssen. 
  
Die Implementierung dieser Methode durch einen Remotetransportanbieter muss der hier beschriebenen Semantik entsprechen. Es gibt keine besonderen Überlegungen. Clients verwenden diese Methode, um die MSGSTATUS_REMOTE_DOWNLOAD und MSGSTATUS_REMOTE_DELETE Bits festzulegen, um anzugeben, dass eine bestimmte Nachricht aus dem Remotenachrichtenspeicher heruntergeladen oder gelöscht werden soll. Ein Remotetransportanbieter muss die zugehörige [IMAPIFolder::GetMessageStatus-Methode](imapifolder-getmessagestatus.md) nicht implementieren. Clients müssen in der Inhaltstabelle des Ordners suchen, um den Status einer Nachricht zu ermitteln. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Sie können die **PR_MSG_STATUS** Eigenschaft einer Nachricht verwenden, um einen Nachrichtensperrvorgang mit anderen Clients auszuhandeln. Legen Sie ein Bit als Sperrbit fest. Um festzustellen, ob das Sperrungsbit festgelegt wurde, überprüfen Sie den vorherigen Wert auf den Nachrichtenstatus im _Parameter "lpulOldStatus"._ Verwenden Sie die anderen Bits im  _ulNewStatus-Parameter,_ um den Nachrichtenstatus nachzuverfolgen, ohne das Sperrbit zu beeinträchtigen. 
  
## <a name="see-also"></a>Siehe auch



[IMAPIFolder::GetMessageStatus](imapifolder-getmessagestatus.md)
  
[PidTagMessageStatus (kanonische Eigenschaft)](pidtagmessagestatus-canonical-property.md)
  
[IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md)

