---
title: Outlook Fehlercodes für Connector für soziale Netzwerke
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 0799243e-ba92-44c4-b687-182e50b57cb7
description: Anbieter sollten Fehler an den Aufrufer zurückgeben, indem sie einen der fehlercodes in der folgenden Tabelle verwenden.
ms.openlocfilehash: 7b5dfc05f3b27549c7801cab5565838302532c4e
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59566143"
---
# <a name="outlook-social-connector-provider-error-codes"></a>Outlook Fehlercodes für Connector für soziale Netzwerke

Anbieter sollten Fehler an den Aufrufer zurückgeben, indem sie einen der fehlercodes in der folgenden Tabelle verwenden. 
  
|**Error**|**Fehlercode (hexadezimal)**|**Beschreibung**|
|:-----|:-----|:-----|
|OSC_E_AUTH_ERROR  <br/> |0x80041404  <br/> |Fehler bei der Authentifizierung im Netzwerk des Standorts des sozialen Netzwerks.  <br/> |
|OSC_E_COULDNOTCONNECT  <br/> |0x80041402  <br/> |Es ist keine Verbindung verfügbar, um eine Verbindung mit dem Standort des sozialen Netzwerks herzustellen.  <br/> |
|OSC_E_FAIL  <br/> |0x80004005  <br/> |Allgemeiner Fehlerfehler.  <br/> |
|OSC_E_INTERNAL_ERROR  <br/> |0x80041400  <br/> |Aufgrund eines ungültigen Vorgangs ist ein interner Fehler aufgetreten.  <br/> |
|OSC_E_INVALIDARG (E_INVALIDARG)  <br/> |0x80070057  <br/> |Ein ungültiges Argument wurde an eine Funktion übergeben.  <br/> |
|OSC_E_NO_CHANGES  <br/> |0x80041406  <br/> |Seit der letzten Synchronisierung sind keine Änderungen aufgetreten.  <br/> |
|OSC_E_NOT_FOUND  <br/> |0x80041405  <br/> |Eine Ressource konnte nicht gefunden werden.  <br/> |
|OSC_E_NOT_IMPLEMENTED (E_NOTIMPL)  <br/> |0x80004001  <br/> |Die Anforderung an den Standort des sozialen Netzwerks ist gültig, wurde jedoch nicht vom Standort des sozialen Netzwerks implementiert.  <br/> |
|OSC_E_OUT_OF_MEMORY (E_OUTOFMEMORY)  <br/> |0x8007000E  <br/> |Es ist ein Fehler aufgetreten, der nicht genügend Arbeitsspeicher aufweist.  <br/> |
|OSC_E_PERMISSION_DENIED  <br/> |0x80041403  <br/> |Der OSC-Anbieter hat die Berechtigung für die Ressource verweigert.  <br/> |
|OSC_E_SERVER_VERSION_NOT_SUPPORTED  <br/> |0x80041406  <br/> |Die Version des Servers zum Konfigurieren des Kontos für soziale Netzwerke wird nicht unterstützt.  <br/> |
|OSC_E_VERSION  <br/> |0x80041401  <br/> |Der Anbieter unterstützt diese Version der OSC-Anbietererweiterung nicht.  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Erfolgs-, Warnungs- und Fehlerwerte werden mithilfe einer 32-Bit-Zahl zurückgegeben, die als Ergebnishandle oder **HRESULT** bezeichnet wird. Ein **HRESULT** ist kein Handle für etwas; Es handelt sich lediglich um einen 32-Bit-Wert, der mehrere Felder enthält, die im Wert codiert sind. Ein positives Ergebnis bedeutet Erfolg mit Status, ein Nullergebnis bedeutet Erfolg ohne Status (S_OK), und ein negatives Ergebnis zeigt fehler an. 
  

