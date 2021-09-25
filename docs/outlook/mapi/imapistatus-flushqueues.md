---
title: IMAPIStatusFlushQueues
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPIStatus.FlushQueues
api_type:
- COM
ms.assetid: d6b01a91-b452-4b2c-9802-698e7b0f4169
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 5f85765a2440be83a5aafa900b686b2f6de84aa6
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59584402"
---
# <a name="imapistatusflushqueues"></a>IMAPIStatus::FlushQueues

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Erzwingt, dass alle Nachrichten, die auf das Senden oder Empfangen warten, sofort hochgeladen oder heruntergeladen werden. Das MAPI-Spoolerstatusobjekt und Statusobjekte, die Von Transportanbietern implementiert werden, unterstützen diese Methode.
  
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
  
> [in] Ein Handle für das übergeordnete Fenster aller Dialogfelder oder Fenster, die von dieser Methode angezeigt werden.
    
 _cbTargetTransport_
  
> [in] Die Byteanzahl im Eintragsbezeichner, auf den der  _lpTargetTransport-Parameter_ verweist. Der  _cbTargetTransport-Parameter_ wird nur für Aufrufe des Statusobjekts des MAPI-Spoolers festgelegt. Für Aufrufe an einen Transportanbieter wird der  _cbTargetTransport-Parameter_ auf 0 festgelegt. 
    
 _lpTargetTransport_
  
> [in] Ein Zeiger auf den Eintragsbezeichner des Transportanbieters, der die Nachrichtenwarteschlangen leeren soll. Der  _Parameter lpTargetTransport_ wird nur für Aufrufe des Statusobjekts des MAPI-Spoolers festgelegt. Für Aufrufe an einen Transportanbieter wird der  _Parameter lpTargetTransport_ auf NULL festgelegt. 
    
 _ulFlags_
  
> [in] Eine Bitmaske mit Flags, die den Leerungsvorgang steuert. Die folgenden Flags können festgelegt werden:
    
FLUSH_ASYNC_OK 
  
> Der Leerungsvorgang kann asynchron ausgeführt werden. Dieses Kennzeichen gilt nur für das Statusobjekt des MAPI-Spoolers. 
    
FLUSH_DOWNLOAD 
  
> Die Warteschlangen für eingehende Nachrichten sollten geleert werden.
    
FLUSH_FORCE 
  
> Der Leerungsvorgang sollte unabhängig davon erfolgen, ob die Leistung beeinträchtigt werden kann. Dieses Flag muss festgelegt werden, wenn ein asynchroner Transportanbieter zielgerichtet ist.
    
FLUSH_NO_UI 
  
> Das Statusobjekt sollte keine Statusanzeige anzeigen.
    
FLUSH_UPLOAD 
  
> Die Warteschlangen für ausgehende Nachrichten sollten geleert werden.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Leerungsvorgang war erfolgreich.
    
MAPI_E_BUSY 
  
> Ein weiterer Vorgang wird ausgeführt. Er sollte abgeschlossen werden können oder beendet werden, bevor dieser Vorgang initiiert werden kann.
    
MAPI_E_NO_SUPPORT 
  
> Das Statusobjekt unterstützt diesen Vorgang nicht, wie durch das Fehlen des STATUS_FLUSH_QUEUES Flags in der **eigenschaft PR_RESOURCE_METHODS** ([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md)) des Statusobjekts angegeben.
    
## <a name="remarks"></a>HinwBemerkungeneise

Die **IMAPIStatus::FlushQueues-Methode** fordert an, dass der MAPI-Spooler oder ein Transportanbieter sofort alle Nachrichten in der ausgehenden Warteschlange sendet oder alle Nachrichten aus der eingehenden Warteschlange empfängt. **FlushQueues** wird nur vom MAPI-Spoolerstatusobjekt und von Statusobjekten implementiert, die von Transportanbietern bereitgestellt werden. 
  
MAPI_E_BUSY sollte für asynchrone Anforderungen zurückgegeben werden, damit Clients ihre Arbeit fortsetzen können. 
  
Standardmäßig ist **FlushQueues** ein synchroner Vorgang. das Steuerelement kehrt erst zum Aufrufer zurück, wenn die Leerung abgeschlossen ist. Nur der vom MAPI-Spooler ausgeführte Leerungsvorgang kann asynchron sein. clients request this behavior by setting the FLUSH_ASYNC_OK flag. 
  
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Die Implementierung von **FlushQueues** durch einen Remotetransportanbieter legt Bits in der **eigenschaft PR_STATUS_CODE** ([PidTagStatusCode](pidtagstatuscode-canonical-property.md)) in der Statuszeile des Anmeldeobjekts fest, um zu steuern, wie Warteschlangen geleert werden. Wenn ein Remoteviewer das Flag FLUSH_UPLOAD übergibt, sollte die **FlushQueues-Methode** die STATUS_INBOUND_ENABLED und STATUS_INBOUND_ACTIVE Bits festlegen. Wenn ein Remoteviewer das Flag FLUSH_DOWNLOAD übergibt, sollte die **FlushQueues-Methode** die STATUS_OUTBOUND_ENABLED und STATUS_OUTBOUND_ACTIVE Bits festlegen. **FlushQueues** sollte dann S_OK zurückgeben. Der MAPI-Spooler initiiert dann die entsprechenden Aktionen zum Hochladen und Herunterladen von Nachrichten. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Ein Aufruf des MAPI-Spoolerstatusobjekts ist eine Direktive zum Übertragen aller Nachrichten an oder vom entsprechenden Transportanbieter. Wenn Sie das Statusobjekt eines einzelnen Transportanbieters aufrufen, sind nur die Nachrichten für diesen Anbieter betroffen.
  
## <a name="see-also"></a>Siehe auch



[PidTagResourceMethods (kanonische Eigenschaft)](pidtagresourcemethods-canonical-property.md)
  
[Kanonische PidTagStatusCode-Eigenschaft](pidtagstatuscode-canonical-property.md)
  
[IMAPIStatus : IMAPIProp](imapistatusimapiprop.md)

