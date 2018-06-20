---
title: Outlook Connector für soziale Netzwerke Anbieter-Fehlercodes
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 0799243e-ba92-44c4-b687-182e50b57cb7
description: Provider sollten Fehler an den Anrufer zurückgeben, mithilfe der Fehlercodes in der folgenden Tabelle dargestellt.
ms.openlocfilehash: 9e9abfda5930926a873ac37d3372eff7100be8a3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19796080"
---
# <a name="outlook-social-connector-provider-error-codes"></a>Outlook Connector für soziale Netzwerke Anbieter-Fehlercodes

Provider sollten Fehler an den Anrufer zurückgeben, mithilfe der Fehlercodes in der folgenden Tabelle dargestellt. 
  
|**Fehler**|**Fehlercode (hexadezimal)**|**Beschreibung**|
|:-----|:-----|:-----|
|OSC_E_AUTH_ERROR  <br/> |0x80041404  <br/> |Fehler bei der Authentifizierung im Netzwerk der Website für soziale Netzwerke.  <br/> |
|OSC_E_COULDNOTCONNECT  <br/> |0x80041402  <br/> |Es ist keine Verbindung für eine Verbindung zu der Website für soziale Netzwerke verfügbar.  <br/> |
|OSC_E_FAIL  <br/> |0 x 80004005  <br/> |Allgemeine Fehler.  <br/> |
|OSC_E_INTERNAL_ERROR  <br/> |0x80041400  <br/> |Aufgrund einer ungültigen Vorgang ist ein interner Fehler aufgetreten.  <br/> |
|OSC_E_INVALIDARG (E_INVALIDARG)  <br/> |0 x 80070057  <br/> |Ein ungültiges Argument wurde an eine Funktion übergeben.  <br/> |
|OSC_E_NO_CHANGES  <br/> |0x80041406  <br/> |Es sind keine Änderungen seit der letzten Synchronisierung aufgetreten.  <br/> |
|OSC_E_NOT_FOUND  <br/> |0x80041405  <br/> |Eine Ressource kann nicht gefunden werden.  <br/> |
|OSC_E_NOT_IMPLEMENTED (E_NOTIMPL)  <br/> |0x80004001  <br/> |Die Anforderung an die Website für soziale Netzwerke ist gültig, aber nicht von der Website für soziale Netzwerke implementiert wurde.  <br/> |
|OSC_E_OUT_OF_MEMORY (E_OUTOFMEMORY)  <br/> |0x8007000E  <br/> |Ein Out-of-Memory-Fehler aufgetreten.  <br/> |
|OSC_E_PERMISSION_DENIED  <br/> |0x80041403  <br/> |Der OSC-Anbieter verweigerte Berechtigung für die Ressource.  <br/> |
|OSC_E_SERVER_VERSION_NOT_SUPPORTED  <br/> |0x80041406  <br/> |Die Version des Servers, das Konto für soziale Netzwerke konfigurieren wird nicht unterstützt.  <br/> |
|OSC_E_VERSION  <br/> |0x80041401  <br/> |Der Anbieter unterstützt diese Version von OSC-anbietererweiterung nicht.  <br/> |
   
## <a name="remarks"></a>Hinweise

Erfolg, Warnung und Fehlerwerte werden anhand einer 32-Bit-Zahl, die ein Ergebnis Handle oder **HRESULT**aufgerufen wird zurückgegeben. Ein **HRESULT** ist kein Handle auf einen anderen Wert; Es wird lediglich eine 32-Bit-Wert, der mehrere Felder in den Wert codiert wurde. Ein positives Ergebnis gibt an, mit dem Status Erfolg, ein NULL-Ergebnis zeigt Erfolg ohne Status (S_OK) und ein negatives Ergebnis Fehler anzeigt. 
  

