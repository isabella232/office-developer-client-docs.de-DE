---
title: Fehlercodes für den Outlook Connector für soziale Netzwerke
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 0799243e-ba92-44c4-b687-182e50b57cb7
description: Anbieter sollten Fehler an den Aufrufer zurückgeben, indem Sie einen der in der folgenden Tabelle aufgeführten Fehlercodes verwenden.
ms.openlocfilehash: 22a6e8d4ebf87157eaee630cc47f9f363150e839
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359857"
---
# <a name="outlook-social-connector-provider-error-codes"></a>Fehlercodes für den Outlook Connector für soziale Netzwerke

Anbieter sollten Fehler an den Aufrufer zurückgeben, indem Sie einen der in der folgenden Tabelle aufgeführten Fehlercodes verwenden. 
  
|**Error**|**Fehlercode (hexadezimal)**|**Beschreibung**|
|:-----|:-----|:-----|
|OSC_E_AUTH_ERROR  <br/> |0x80041404  <br/> |Fehler bei der Authentifizierung im Netzwerk des sozialen Netzwerkstandorts.  <br/> |
|OSC_E_COULDNOTCONNECT  <br/> |0x80041402  <br/> |Es ist keine Verbindung mit dem sozialen Netzwerkstandort verfügbar.  <br/> |
|OSC_E_FAIL  <br/> |0x80004005  <br/> |Allgemeiner Fehler.  <br/> |
|OSC_E_INTERNAL_ERROR  <br/> |0x80041400  <br/> |Ein interner Fehler ist aufgrund eines ungültigen Vorgangs aufgetreten.  <br/> |
|OSC_E_INVALIDARG (E_INVALIDARG)  <br/> |0x80070057  <br/> |Ein ungültiges Argument wurde an eine Funktion übergeben.  <br/> |
|OSC_E_NO_CHANGES  <br/> |0x80041406  <br/> |Seit der letzten Synchronisierung sind keine Änderungen aufgetreten.  <br/> |
|OSC_E_NOT_FOUND  <br/> |0x80041405  <br/> |Eine Ressource wurde nicht gefunden.  <br/> |
|OSC_E_NOT_IMPLEMENTED (E_NOTIMPL)  <br/> |0x80004001  <br/> |Die Anforderung an den sozialen Netzwerkstandort ist gültig, wurde jedoch nicht vom sozialen Netzwerkstandort implementiert.  <br/> |
|OSC_E_OUT_OF_MEMORY (E_OUTOFMEMORY)  <br/> |0x8007000E  <br/> |Ein Speicherfehler ist aufgetreten.  <br/> |
|OSC_E_PERMISSION_DENIED  <br/> |0x80041403  <br/> |Der OSC-Anbieter hat die Berechtigung für die Ressource verweigert.  <br/> |
|OSC_E_SERVER_VERSION_NOT_SUPPORTED  <br/> |0x80041406  <br/> |Die Version des Servers zum Konfigurieren des Kontos für soziale Netzwerke wird nicht unterstützt.  <br/> |
|OSC_E_VERSION  <br/> |0x80041401  <br/> |Der Anbieter unterstützt diese Version der OSC-Anbieter Erweiterbarkeit nicht.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Erfolgs-, Warnungs-und Fehlerwerte werden mithilfe einer 32-Bit-Zahl zurückgegeben, die als Ergebnis-Handle oder als **HRESULT**bezeichnet wird. Ein **HRESULT** ist kein Handle für irgendetwas; Es handelt sich lediglich um einen 32-Bit-Wert, der mehrere Felder enthält, die im Wert codiert sind. Ein positives Ergebnis gibt den Erfolg mit Status an, ein NULL Ergebnis gibt den Erfolg ohne Status (S_OK) an, und ein negatives Ergebnis deutet auf einen Fehler hin. 
  

