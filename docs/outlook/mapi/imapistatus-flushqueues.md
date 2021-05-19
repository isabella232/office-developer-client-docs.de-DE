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
ms.openlocfilehash: 5f8396ca84192e485d33fb5a96f641361b717584
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432604"
---
# <a name="imapistatusflushqueues"></a>IMAPIStatus::FlushQueues

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Erzwingt, dass alle Nachrichten, die auf das Senden oder Empfangen warten, sofort hochgeladen oder heruntergeladen werden. Das MAPI-Spoolerstatusobjekt und die Statusobjekte, die von Transportanbietern implementiert werden, unterstützen diese Methode.
  
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
  
> [in] Ein Handle zum übergeordneten Fenster aller Dialogfelder oder Fenster, die von dieser Methode angezeigt werden.
    
 _cbTargetTransport_
  
> [in] Die Byteanzahl im Eintragsbezeichner, auf den der  _lpTargetTransport-Parameter_ verweist. Der  _cbTargetTransport-Parameter_ wird nur für Aufrufe des Statusobjekts des MAPI-Spoolers festgelegt. Für Anrufe an einen Transportanbieter ist  _der cbTargetTransport-Parameter_ auf 0 festgelegt. 
    
 _lpTargetTransport_
  
> [in] Ein Zeiger auf die Eintrags-ID des Transportanbieters, der seine Nachrichtenwarteschlangen leeren soll. Der  _lpTargetTransport-Parameter_ wird nur für Aufrufe des Statusobjekts des MAPI-Spoolers festgelegt. Für Anrufe an einen Transportanbieter ist  _der lpTargetTransport-Parameter_ auf NULL festgelegt. 
    
 _ulFlags_
  
> [in] Eine Bitmaske mit Flags, die den Leerungsvorgang steuert. Die folgenden Kennzeichen können festgelegt werden:
    
FLUSH_ASYNC_OK 
  
> Der Leerungsvorgang kann asynchron erfolgen. Dieses Flag gilt nur für das Statusobjekt des MAPI-Spoolers. 
    
FLUSH_DOWNLOAD 
  
> Die Warteschlangen für eingehende Nachrichten sollten geleert werden.
    
FLUSH_FORCE 
  
> Der Leerungsvorgang sollte unabhängig von der Wahrscheinlichkeit eines Leistungsrückgangs erfolgen. Dieses Flag muss festgelegt werden, wenn ein asynchroner Transportanbieter als Ziel festgelegt wird.
    
FLUSH_NO_UI 
  
> Das Statusobjekt sollte keine Statusanzeige anzeigen.
    
FLUSH_UPLOAD 
  
> Die Warteschlangen für ausgehende Nachrichten sollten geleert werden.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Leerungsvorgang war erfolgreich.
    
MAPI_E_BUSY 
  
> Ein weiterer Vorgang wird ausgeführt. Er sollte abgeschlossen oder beendet werden dürfen, bevor dieser Vorgang initiiert werden kann.
    
MAPI_E_NO_SUPPORT 
  
> Das status-Objekt unterstützt diesen Vorgang nicht, wie durch das Fehlen des STATUS_FLUSH_QUEUES-Flag in der **PR_RESOURCE_METHODS** ([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md))-Eigenschaft des Statusobjekts angegeben wird.
    
## <a name="remarks"></a>Hinweise

Die **IMAPIStatus::FlushQueues-Methode** fordert an, dass der MAPI-Spooler oder ein Transportanbieter sofort alle Nachrichten in der ausgehenden Warteschlange senden oder alle Nachrichten aus der eingehenden Warteschlange empfangen. **FlushQueues** wird nur vom MAPI-Spoolerstatusobjekt und von Statusobjekten implementiert, die von Transportanbietern zur Bereitstellung verwendet werden. 
  
MAPI_E_BUSY sollte für asynchrone Anforderungen zurückgegeben werden, damit Clients ihre Arbeit fortsetzen können. 
  
**FlushQueues** ist standardmäßig ein synchroner Vorgang. das Steuerelement wird erst wieder an den Anrufer zurück, wenn die Leerung abgeschlossen ist. Nur der vom #A0 ausgeführte Leervorgang kann asynchron sein. Clients fordern dieses Verhalten an, indem sie FLUSH_ASYNC_OK festlegen. 
  
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Die Implementierung von **FlushQueues** durch einen Remotetransportanbieter legt Bits in der **eigenschaft PR_STATUS_CODE** ([PidTagStatusCode](pidtagstatuscode-canonical-property.md)) in der Statuszeile des Anmeldeobjekts fest, um zu steuern, wie Warteschlangen geleert werden. Wenn ein Remoteanzeiger das FLUSH_UPLOAD übergibt, sollte die **FlushQueues-Methode** die STATUS_INBOUND_ENABLED und STATUS_INBOUND_ACTIVE festlegen. Wenn ein Remoteanzeiger das FLUSH_DOWNLOAD übergibt, sollte die **FlushQueues-Methode** die STATUS_OUTBOUND_ENABLED und STATUS_OUTBOUND_ACTIVE festlegen. **FlushQueues** sollte dann eine S_OK. Der MAPI-Spooler initiiert dann die entsprechenden Aktionen zum Hochladen und Herunterladen von Nachrichten. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Ein Aufruf des MAPI-Spoolerstatusobjekts ist eine Direktive zum Übertragen aller Nachrichten an oder vom entsprechenden Transportanbieter. Wenn Sie das Statusobjekt eines einzelnen Transportanbieters aufrufen, sind nur die Nachrichten für den jeweiligen Anbieter betroffen.
  
## <a name="see-also"></a>Siehe auch



[PidTagResourceMethods (kanonische Eigenschaft)](pidtagresourcemethods-canonical-property.md)
  
[PidTagStatusCode (kanonische Eigenschaft)](pidtagstatuscode-canonical-property.md)
  
[IMAPIStatus : IMAPIProp](imapistatusimapiprop.md)

