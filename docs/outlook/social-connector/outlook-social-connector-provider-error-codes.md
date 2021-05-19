---
title: Outlook Fehlercodes des Anbieters für soziale Netzwerke
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 0799243e-ba92-44c4-b687-182e50b57cb7
description: Anbieter sollten Fehler mithilfe eines der in der folgenden Tabelle aufgeführten Fehlercodes an den Anrufer zurückgeben.
ms.openlocfilehash: 22a6e8d4ebf87157eaee630cc47f9f363150e839
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425351"
---
# <a name="outlook-social-connector-provider-error-codes"></a>Outlook Fehlercodes des Anbieters für soziale Netzwerke

Anbieter sollten Fehler mithilfe eines der in der folgenden Tabelle aufgeführten Fehlercodes an den Anrufer zurückgeben. 
  
|**Error**|**Fehlercode (hexadezimal)**|**Beschreibung**|
|:-----|:-----|:-----|
|OSC_E_AUTH_ERROR  <br/> |0x80041404  <br/> |Fehler bei der Authentifizierung im Netzwerk des Standorts für soziale Netzwerke.  <br/> |
|OSC_E_COULDNOTCONNECT  <br/> |0x80041402  <br/> |Es ist keine Verbindung verfügbar, um eine Verbindung mit dem Standort des sozialen Netzwerks herzustellen.  <br/> |
|OSC_E_FAIL  <br/> |0x80004005  <br/> |Allgemeiner Fehlerfehler.  <br/> |
|OSC_E_INTERNAL_ERROR  <br/> |0x80041400  <br/> |Aufgrund eines ungültigen Vorgangs ist ein interner Fehler aufgetreten.  <br/> |
|OSC_E_INVALIDARG (E_INVALIDARG)  <br/> |0x80070057  <br/> |Ein ungültiges Argument wurde an eine Funktion übergeben.  <br/> |
|OSC_E_NO_CHANGES  <br/> |0x80041406  <br/> |Seit der letzten Synchronisierung sind keine Änderungen aufgetreten.  <br/> |
|OSC_E_NOT_FOUND  <br/> |0x80041405  <br/> |Eine Ressource kann nicht gefunden werden.  <br/> |
|OSC_E_NOT_IMPLEMENTED (E_NOTIMPL)  <br/> |0x80004001  <br/> |Die Anforderung an den Standort für soziale Netzwerke ist gültig, wurde aber nicht vom Standort für soziale Netzwerke implementiert.  <br/> |
|OSC_E_OUT_OF_MEMORY (E_OUTOFMEMORY)  <br/> |0x8007000E  <br/> |Es ist ein Speicherfehler aufgetreten.  <br/> |
|OSC_E_PERMISSION_DENIED  <br/> |0x80041403  <br/> |Der OSC-Anbieter hat die Berechtigung für die Ressource verweigert.  <br/> |
|OSC_E_SERVER_VERSION_NOT_SUPPORTED  <br/> |0x80041406  <br/> |Die Version des Servers zum Konfigurieren des Kontos für soziale Netzwerke wird nicht unterstützt.  <br/> |
|OSC_E_VERSION  <br/> |0x80041401  <br/> |Der Anbieter unterstützt diese Version der Erweiterbarkeit des OSC-Anbieters nicht.  <br/> |
   
## <a name="remarks"></a>Hinweise

Erfolgs-, Warnungs- und Fehlerwerte werden mithilfe einer 32-Bit-Nummer zurückgegeben, die als Ergebnishandle oder **HRESULT bezeichnet wird.** Ein **HRESULT** ist kein Handle für etwas; Es handelt sich lediglich um einen 32-Bit-Wert mit mehreren Feldern, die im Wert codiert sind. Ein positives Ergebnis gibt den Erfolg mit dem Status an, ein Nullergebnis gibt den Erfolg ohne Status (S_OK) an, und ein negatives Ergebnis weist auf einen Fehler hin. 
  

