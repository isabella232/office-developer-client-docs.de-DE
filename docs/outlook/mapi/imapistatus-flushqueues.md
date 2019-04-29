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
  
ErZwingt, dass alle Nachrichten, die darauf warten, gesendet oder empfangen werden, sofort hochgeladen oder heruntergeladen werden. Das MAPI-Spooler-Statusobjekt und die Statusobjekte, die von Transportanbietern implementiert werden, unterstützen diese Methode.
  
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
  
> in Ein Handle für das übergeordnete Fenster aller von dieser Methode angezeigten Dialogfelder oder Fenster.
    
 _cbTargetTransport_
  
> in Die Anzahl der Bytes in der Eintrags-ID, auf die durch den _lpTargetTransport_ -Parameter verwiesen wird. Der _cbTargetTransport_ -Parameter wird nur bei Aufrufen des Status-Objekts des MAPI-Spoolers festgelegt. Bei Aufrufen eines Transportanbieters wird der Parameter _cbTargetTransport_ auf 0 festgelegt. 
    
 _lpTargetTransport_
  
> in Ein Zeiger auf die Eintrags-ID des Transportanbieters, der die Nachrichtenwarteschlangen leeren soll. Der _lpTargetTransport_ -Parameter wird nur bei Aufrufen des Status-Objekts des MAPI-Spoolers festgelegt. Bei Aufrufen eines Transportanbieters wird der Parameter _lpTargetTransport_ auf NULL festgelegt. 
    
 _ulFlags_
  
> in Eine Bitmaske von Flags, die den Flush-Vorgang steuert. Die folgenden Flags können festgelegt werden:
    
FLUSH_ASYNC_OK 
  
> Der Flush-Vorgang kann asynchron ausgeführt werden. Dieses Flag gilt nur für das Statusobjekt des MAPI-Spoolers. 
    
FLUSH_DOWNLOAD 
  
> Die Warteschlangen für eingehende Nachrichten sollten geleert werden.
    
FLUSH_FORCE 
  
> Der Flush-Vorgang sollte unabhängig von der Wahrscheinlichkeit einer Leistungsminderung auftreten. Dieses Flag muss festgelegt werden, wenn ein asynchroner Transportanbieter zielgerichtet ist.
    
FLUSH_NO_UI 
  
> Das Status-Objekt sollte keine Statusanzeige anzeigen.
    
FLUSH_UPLOAD 
  
> Die Warteschlangen für ausgehende Nachrichten sollten geleert werden.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Flush-Vorgang war erfolgreich.
    
MAPI_E_BUSY 
  
> Ein anderer Vorgang wird ausgeführt; Es sollte zugelassen werden, oder es sollte beendet werden, bevor dieser Vorgang eingeleitet werden kann.
    
MAPI_E_NO_SUPPORT 
  
> Das Status-Objekt unterstützt diesen Vorgang nicht, wie durch das Fehlen des STATUS_FLUSH_QUEUES-Flags in der **PR_RESOURCE_METHODS** ([pidtagresourcemethods (](pidtagresourcemethods-canonical-property.md))-Eigenschaft des Status-Objekts angegeben.
    
## <a name="remarks"></a>Bemerkungen

Die **IMAPIStatus:: FlushQueues** -Methode fordert, dass der MAPI-Spooler oder ein Transportanbieter sofort alle Nachrichten in der ausgehenden Warteschlange sendet oder alle Nachrichten von der eingehenden Warteschlange empfängt. **FlushQueues** wird nur vom MAPI-Spooler-Statusobjekt und von Statusobjekten implementiert, die von den Transportanbietern bereitstellen. 
  
MAPI_E_BUSY sollte für asynchrone Anforderungen zurückgegeben werden, damit Clients weiterhin arbeiten können. 
  
Standardmäßig ist **FlushQueues** eine synchrone Operation; die Steuerung kehrt erst dann zum Aufrufer zurück, wenn der Flush abgeschlossen wurde. Nur der Flush-Vorgang, der vom MAPI-Spooler ausgeführt wird, kann asynchron sein; Clients fordern dieses Verhalten, indem Sie das FLUSH_ASYNC_OK-Flag festlegen. 
  
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Die Implementierung eines Remote Transportanbieters von **FlushQueues** legt Bits in der **PR_STATUS_CODE** ([pidtagstatuscode (](pidtagstatuscode-canonical-property.md))-Eigenschaft in der Status Zeile des LOGON-Objekts fest, um zu steuern, wie Warteschlangen geleert werden. Wenn ein Remote Viewer das FLUSH_UPLOAD-Flag übergibt, sollte die **FlushQueues** -Methode die Bits STATUS_INBOUND_ENABLED und STATUS_INBOUND_ACTIVE festlegen. Wenn ein Remote Viewer das FLUSH_DOWNLOAD-Flag übergibt, sollte die **FlushQueues** -Methode die Bits STATUS_OUTBOUND_ENABLED und STATUS_OUTBOUND_ACTIVE festlegen. **FlushQueues** sollte dann S_OK zurückgeben. Der MAPI-Spooler startet dann die entsprechenden Aktionen, um Nachrichten hoch-und herunterzuladen. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Ein Aufruf des MAPI-Spooler-Status Objekts ist eine Direktive, mit der alle Nachrichten an den oder vom entsprechenden Transportanbieter übertragen werden. Wenn Sie das Status-Objekt eines einzelnen Transportanbieters aufrufen, sind nur die Nachrichten für diesen Anbieter betroffen.
  
## <a name="see-also"></a>Siehe auch



[Kanonische Pidtagresourcemethods (-Eigenschaft](pidtagresourcemethods-canonical-property.md)
  
[Kanonische Pidtagstatuscode (-Eigenschaft](pidtagstatuscode-canonical-property.md)
  
[IMAPIStatus : IMAPIProp](imapistatusimapiprop.md)

