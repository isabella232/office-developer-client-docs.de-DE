---
title: IMAPIStatusFlushQueues
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIStatus.FlushQueues
api_type:
- COM
ms.assetid: d6b01a91-b452-4b2c-9802-698e7b0f4169
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 30aaaaa250155215149a941da7f7e528d65b8dc3
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22592199"
---
# <a name="imapistatusflushqueues"></a>IMAPIStatus::FlushQueues

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Erzwingt, dass alle Nachrichten gesendet oder empfangen, um sofort hoch- oder heruntergeladen werden. Die MAPI-Warteschlange Statusobjekt und die Status-Objekte, mit denen Transportanbieter implementiert unterstützt diese Methode auf.
  
```cpp
HRESULT FlushQueues(
  ULONG_PTR ulUIParam,
  ULONG cbTargetTransport,
  LPENTRYID lpTargetTransport,
  ULONG ulFlags
);
```

## <a name="parameters"></a>Parameter

 _ulUIParam_
  
> [in] Ein Handle für das übergeordnete Fenster für alle Dialogfelder oder Windows, die diese Methode anzeigt.
    
 _cbTargetTransport_
  
> [in] Die Byteanzahl von in die Eintrags-ID auf den durch den Parameter _LpTargetTransport_ verwiesen. Der Parameter _CbTargetTransport_ wird nur für Anrufe an die MAPI-Warteschlange Status-Objekts festgelegt. Für Anrufe eines Transportdienstes ist der Parameter _CbTargetTransport_ auf 0 festgelegt. 
    
 _lpTargetTransport_
  
> [in] Ein Zeiger auf die Eintrags-ID des Anbieters Transport, der seine Nachrichtenwarteschlangen zu leeren. Der Parameter _LpTargetTransport_ wird nur für Anrufe an die MAPI-Warteschlange Status-Objekts festgelegt. Für Anrufe eines Transportdienstes ist der _LpTargetTransport_ -Parameter auf NULL festgelegt. 
    
 _ulFlags_
  
> [in] Eine Bitmaske aus Flags, die die Schreibvorgang wurde steuert. Die folgenden Kennzeichen können festgelegt werden:
    
FLUSH_ASYNC_OK 
  
> Flush-Vorgang kann asynchron auftreten. Dieser Parameter gilt nur für die MAPI-Warteschlange Status-Objekt. 
    
FLUSH_DOWNLOAD 
  
> Die eingehende Nachrichtenwarteschlangen sollten entfernt werden.
    
FLUSH_FORCE 
  
> Der Schreibvorgang wurde sollte unabhängig davon, obwohl die Wahrscheinlichkeit, dass eine Beeinträchtigung der Systemleistung auftreten. Dieses Kennzeichen müssen festgelegt werden, wenn eine asynchrone Adressbuchhierarchie gerichtet ist.
    
FLUSH_NO_UI 
  
> Das Statusobjekt sollte eine Statusanzeige nicht angezeigt werden.
    
FLUSH_UPLOAD 
  
> Ausgehende Nachrichtenwarteschlangen sollten entfernt werden.
    
## <a name="return-value"></a>R�ckgabewert

S_OK 
  
> Der Schreibvorgang wurde erfolgreich war.
    
MAPI_E_BUSY 
  
> Ein anderer Vorgang ist in Bearbeitung. Es dürfen für die Durchführung, oder er angehalten werden sollte, bevor Sie diesen Vorgang initiiert werden kann.
    
MAPI_E_NO_SUPPORT 
  
> Das Statusobjekt unterstützt keine dieser Vorgang, wie durch die Abwesenheit des STATUS_FLUSH_QUEUES-Flags in den Status des Objekts **PR_RESOURCE_METHODS** ([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md))-Eigenschaft angegeben.
    
## <a name="remarks"></a>HinwBemerkungeneise

Die Methode **IMAPIStatus::FlushQueues** fordert an, dass die MAPI-Warteschlange oder eines Transportdienstes sofort alle Nachrichten in der Warteschlange für ausgehende Nachrichten senden oder empfangen alle aus der Warteschlange für eingehende. **FlushQueues** ist nur durch das MAPI-Warteschlange Status-Objekt und von Status-Objekten, die transport-Anbieter Kooperation implementiert. 
  
MAPI_E_BUSY sollten für asynchrone Anfragen zurückgegeben werden, damit Clients Arbeit fortgesetzt werden können. 
  
Standardmäßig ist **FlushQueues** eine synchrone Operation. Steuerelement gibt keine an den Anrufer zurück, bis der Löschvorgang abgeschlossen ist. Nur der flush durch die MAPI-Warteschlange ausgeführte Vorgang kann asynchrone sein. Clients fordern dieses Verhalten, indem Sie das FLUSH_ASYNC_OK-Flag festlegen. 
  
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Implementierung eines remote-Transport-Anbieters von **FlushQueues** legt Bits in der Eigenschaft **PR_STATUS_CODE** ([PidTagStatusCode](pidtagstatuscode-canonical-property.md)) in das Anmeldeobjekt Statuszeile steuern, wie Warteschlangen geleert werden. Wenn Sie ein remote-Viewer das Flag FLUSH_UPLOAD übergibt, sollte die **FlushQueues** -Methode die Bits STATUS_INBOUND_ENABLED und STATUS_INBOUND_ACTIVE festlegen. Wenn Sie ein remote-Viewer das Flag FLUSH_DOWNLOAD übergibt, sollte die **FlushQueues** -Methode die Bits STATUS_OUTBOUND_ENABLED und STATUS_OUTBOUND_ACTIVE festlegen. **FlushQueues** sollte dann S_OK zurückgegeben. Die MAPI-Warteschlange initiieren Sie dann die entsprechenden Aktionen zum Hoch- und Herunterladen von Nachrichten. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Ein Anruf an das MAPI-Warteschlange Status-Objekt ist eine Richtlinie auf alle Nachrichten oder von der entsprechenden Adressbuchhierarchie übertragen. Wenn Sie eine einzelne Adressbuchhierarchie Status-Objekts aufrufen, sind nur die Nachrichten für diesen Anbieter betroffen.
  
## <a name="see-also"></a>Siehe auch



[PidTagResourceMethods (kanonische Eigenschaft)](pidtagresourcemethods-canonical-property.md)
  
[PidTagStatusCode (kanonische Eigenschaft)](pidtagstatuscode-canonical-property.md)
  
[IMAPIStatus : IMAPIProp](imapistatusimapiprop.md)

