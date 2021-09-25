---
title: IMAPIStatusValidateState
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPIStatus.ValidateState
api_type:
- COM
ms.assetid: 036b9b15-86e1-4a37-8e4b-e37b2963d8fb
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 88615e91b89e667504b32ac8a255c6b8acd24752
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59596162"
---
# <a name="imapistatusvalidatestate"></a>IMAPIStatus::ValidateState

**Gilt für**: Outlook 2013 | Outlook 2016 
  
Bestätigt die für die MAPI-Ressource oder den Dienstanbieter verfügbaren externen Statusinformationen. Diese Methode wird in allen Statusobjekten unterstützt. 
  
```cpp
HRESULT ValidateState(
  ULONG_PTR ulUIParam,
  ULONG ulFlags
);
```

## <a name="parameters"></a>Parameter

_ulUIParam_
  
> [in] Ein Handle für das übergeordnete Fenster aller Dialogfelder oder Fenster, die von dieser Methode angezeigt werden.
    
_ulFlags_
  
> [in] Eine Bitmaske mit Flags, die die Überprüfung steuert. Die folgenden Flags können festgelegt werden:
    
ABORT_XP_HEADER_OPERATION
  
> Der Benutzer hat den Vorgang abgebrochen, in der Regel durch Klicken auf die Schaltfläche **Abbrechen** im entsprechenden Dialogfeld. Das Statusobjekt hat zwei Optionen: 
    
   - Fahren Sie mit der Arbeit an dem Vorgang fort.
    
   - Beenden Sie den Vorgang, und geben Sie MAPI_E_USER_CANCELED zurück.
    
CONFIG_CHANGED 
  
> Eine oder mehrere der Konfigurationseigenschaften des Statusobjekts wurden geändert. Clients können dieses Flag festlegen, damit der MAPI-Spooler kritische Transportanbieterfehler dynamisch korrigieren kann. 
    
FORCE_XP_CONNECT 
  
> Das Statusobjekt sollte eine Verbindung herstellen. Wenn dieses Flag mit dem flag REFRESH_XP_HEADER_CACHE oder PROCESS_XP_HEADER_CACHE verwendet wird, wird die Verbindung ohne Zwischenspeicherung hergestellt.
    
FORCE_XP_DISCONNECT 
  
> Das Statusobjekt sollte eine Trennungsoperation ausführen. Wenn dieses Flag mit dem flag REFRESH_XP_HEADER_CACHE oder PROCESS_XP_HEADER_CACHE verwendet wird, erfolgt die Trennung ohne Zwischenspeicherung.
    
PROCESS_XP_HEADER_CACHE 
  
> Einträge in der Headercachetabelle sollten verarbeitet werden, alle mit dem MSGSTATUS_REMOTE_DOWNLOAD Flag gekennzeichneten Nachrichten sollten heruntergeladen werden, und alle Nachrichten, die mit dem MSGSTATUS_REMOTE_DELETE Flag gekennzeichnet sind, sollten gelöscht werden. Nachrichten, für die sowohl MSGSTATUS_REMOTE_DOWNLOAD als auch MSGSTATUS_REMOTE_DELETE festgelegt sind, sollten verschoben werden.
    
REFRESH_XP_HEADER_CACHE 
  
> Für einen Remote-Transportanbieter sollte eine neue Liste der Nachrichtenkopfzeilen heruntergeladen werden, und alle Flags, die den Nachrichtenstatus markieren, sollten gelöscht werden.
    
SUPPRESS_UI 
  
> Verhindert, dass das Statusobjekt im Rahmen des Vorgangs eine Benutzeroberfläche anzeigt.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Die Überprüfung war erfolgreich.
    
MAPI_E_BUSY 
  
> Ein weiterer Vorgang wird ausgeführt. er sollte abgeschlossen werden dürfen oder beendet werden, bevor dieser Vorgang initiiert wird.
    
MAPI_E_NO_SUPPORT 
  
> Das Status-Objekt unterstützt die Überprüfungsmethode nicht, wie durch das Fehlen des STATUS_VALIDATE_STATE Flags in der **PR_RESOURCE_METHODS** ([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md)) -Eigenschaft angegeben.
    
MAPI_E_USER_CANCEL 
  
> Der Benutzer hat den Überprüfungsvorgang abgebrochen, in der Regel durch Klicken auf die Schaltfläche **Abbrechen** in einem Dialogfeld. Dieser Wert wird nur von Remote-Transportanbietern zurückgegeben. 
    
## <a name="remarks"></a>HinwBemerkungeneise

Die **IMAPIStatus::ValidateState-Methode** überprüft den Status einer Ressource, die einem Statusobjekt zugeordnet ist. **ValidateState** ist die einzige Methode in der [IMAPIStatus-Schnittstelle,](imapistatusimapiprop.md) die für alle Statusobjekte erforderlich ist. Das genaue Verhalten dieser Methode hängt von der Implementierung ab. In der folgenden Tabelle wird die Implementierung der einzelnen Typen von Statusobjekten beschrieben. 
  
|**Status-Objekt**|ValidateState**-Implementierung**|
|:-----|:-----|
|MAPI-Subsystem  <br/> |Überprüft den Status aller Ressourcen, die die derzeit aktiven Dienstanbieter und das Subsystem selbst besitzen.  <br/> |
|MAPI-Spooler  <br/> |Führt eine Anmeldung aller Transportanbieter aus, unabhängig davon, ob sie bereits angemeldet sind.  <br/> |
|MAPI-Adressbuch  <br/> |Überprüft die Einträge im Profilabschnitt.  <br/> |
|Dienstleister  <br/> |Die Implementierung hängt vom Anbietertyp und den im  _ulFlags-Parameter_ festgelegten Flags ab.  <br/> |
   
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Remoteclientanwendungen rufen die **ValidateState-Methode** auf, um die Remoteverarbeitung für verschiedene Aktionen zu starten. Diese Methode wird in erster Linie verwendet, um Statusbits für die Kommunikation mit dem MAPI-Spooler festzulegen, anstatt tatsächlich Eine Arbeit zu erledigen. In der Regel legt der Transportanbieter Flags in der Statuszeile fest, die dem MAPI-Spooler angeben, welche Aktionen initiiert werden müssen, um die Anforderung des Clients abzuschließen. 

In diesem Modell der Client-Transport-Spooler-Interaktion sind die vom Client angeforderten Aktionen asynchron, **sodass ValidateState** zurückgegeben wird, bevor die angeforderten Aktionen abgeschlossen sind. Aktionen, die nicht notwendigerweise das zugrunde liegende Messagingsystem oder eine transportspezifische Schnittstelle betreffen, können jedoch synchron sein. Die Clientanwendung übergibt eine Bitmaske der folgenden Flags, um anzugeben, welche Aktionen der Remote-Transportanbieter ausführen soll. 
  
ABORT_XP_HEADER_OPERATION 
  
> Wenn möglich, sollte der Remote-Transportanbieter alle Vorgänge abbrechen, die das Herunterladen von Headern umfassen. Hierzu muss der Transportanbieter die folgenden Eigenschaftswerte in der Statuszeile des Anmeldeobjekts festlegen:
    
   - Löschen Sie die STATUS_INBOUND_ENABLED und STATUS_INBOUND_ACTIVE Bits in der **Eigenschaft PR_STATUS_CODE** ([PidTagStatusCode](pidtagstatuscode-canonical-property.md)), um den MAPI-Spooler anzuhalten, den eingehenden Leerungsprozess für diesen Transportanbieter anzuhalten.
    
   - Legen Sie das STATUS_OFFLINE Bit in der **PR_STATUS_CODE-Eigenschaft fest.** 
    
   - Legen Sie die **eigenschaft PR_REMOTE_VALIDATE_OK** ([PidTagRemoteValidateOk](pidtagremotevalidateok-canonical-property.md)) auf TRUE fest.
    
   - Legen Sie die **Eigenschaft PR_STATUS_STRING** ([PidTagStatusString](pidtagstatusstring-canonical-property.md)) auf eine Zeichenfolge fest, die den Status des Transportanbieters für den Benutzer angibt.
    
   - Geben Sie S_OK zur�ck. Wenn der laufende Vorgang jedoch nicht abgebrochen werden kann, sollte **ValidateState** MAPI_E_BUSY zurückgeben. 
    
FORCE_XP_CONNECT 
  
> Ein Remote-Transport-Anbieter sollte niemals eine Verbindung mit einer freigegebenen Ressource (z. B. einem Modem oder COM-Port) außerhalb des Kontexts der MAPI-Spooler-Transport-Interaktion herstellen, die an der [IXPLogon::FlushQueues-Methode](ixplogon-flushqueues.md) beteiligt ist. Wenn **ValidateState** mit diesem Flag aufgerufen wird, sollte Ihr Transportanbieter Folgendes tun: 
    
   - Legen Sie ein internes Statuskennzeichen fest, um anzugeben, dass die Remoteverbindung hergestellt werden muss, wenn die **IXPLogon::FlushQueues-Methode** aufgerufen wird. 
    
   - Legen Sie die richtigen Werte in der Statustabelle fest, damit der MAPI-Spooler den Warteschlangen-Leerenvorgang initiiert.
    
   - Wenn das Leeren von Warteschlangen abgeschlossen ist, geben Sie die freigegebene Ressource frei.
    
   - Löschen Sie das STATUS_OFFLINE  Bit in der PR_STATUS_CODE-Eigenschaft. 
    
   - Geben Sie S_OK zur�ck.
    
FORCE_XP_DISCONNECT 
  
> Der Remotetransportanbieter sollte seine Verbindung mit den Messagingsystemressourcen freigeben. Danach sollte das STATUS_OFFLINE Bit in der **PR_STATUS_CODE-Eigenschaft** festgelegt und S_OK zurückgegeben werden. 
    
PROCESS_XP_HEADER_CACHE 
  
> Der Remotetransportanbieter sollte Remotenachrichten verarbeiten und alle Nachrichten hochladen, die zurückgestellt wurden. Hierzu muss der Transportanbieter die folgenden Eigenschaftswerte in der Statuszeile des Anmeldeobjekts festlegen:
    
   - Legen Sie die **PR_STATUS_STRING-Eigenschaft** auf eine Zeichenfolge fest, die den Status des Transportanbieters für den Benutzer angibt. 
    
   - Legen Sie die bits STATUS_OUTBOUND_ENABLED und STATUS_OUTBOUND_ACTIVE in der **PR_STATUS_CODE-Eigenschaft** fest. 
    
   - Legen Sie die **PR_REMOTE_VALIDATE_OK** Eigenschaft in der Statuszeile des Transportanbieters auf FALSE fest. 
    
   - Wenn beim Aufrufen von **ValidateState** ein anderer Vorgang ausgeführt wird (z. B. das Herunterladen von Headern), sollte **ValidateState** MAPI_E_BUSY zurückgeben. 
    
   - Führen Sie auch den Code für die Verarbeitung des REFRESH_XP_HEADER_CACHE Flags aus, um die Anforderungen des Microsoft Exchange-Clients zu erfüllen.
    
REFRESH_XP_HEADER_CACHE 
  
> Der Remote-Transportanbieter sollte alle neuen Nachrichtenkopfzeilen aus dem Messagingsystem abrufen. Hierzu muss der Transportanbieter Folgendes tun:
    
   - Legen Sie die **PR_STATUS_STRING-Eigenschaft** auf eine Zeichenfolge fest, die den Status des Transportanbieters für den Benutzer angibt. 
    
   - Legen Sie die bits STATUS_INBOUND_ENABLED und STATUS_INBOUND_ACTIVE in der **PR_STATUS_CODE-Eigenschaft** fest. 
    
   - Löschen Sie das STATUS_OFFLINE  Bit in der PR_STATUS_CODE-Eigenschaft. 
    
   - Legen Sie das STATUS_ONLINE Bit in der **PR_STATUS_CODE-Eigenschaft** fest. 
    
   - Legen Sie die **eigenschaft PR_REMOTE_VALIDATE_OK** in der Statuszeile des Transportanbieters auf FALSE fest. 
    
SHOW_XP_SESSION_UI 
  
> Wenn Ihr Transportanbieter über Teile der Benutzeroberfläche für die Verarbeitung der Nachrichtenkopfzeilen verfügt (z. B. ein Dialogfeld, das das Herunterladen von Nachrichten bestätigt), sollte dieses Dialogfeld angezeigt werden. Andernfalls kann **ValidateState** MAPI_E_NO_SUPPORT zurückgeben. 
    
Wenn andere Flags als diese übergeben werden, sollte **ValidateState** MAPI_E_UNKNOWN_FLAGS zurückgeben. 
  
Der Aufruf des Clients an den Transportanbieter erfolgt häufig über die **IMAPIStatus::ValidateState-Methode.** Während der Verarbeitung von **ValidateState** sollte der Transportanbieter keine Aktionen ausführen, die untergeordnete Systemressourcen, z. B. ein Modem oder einen COM-Port, zuordnen. Der Grund dafür ist, dass der MAPI-Spooler manchmal Warteschlangen auf mehreren Transportanbietern leeren muss. Der Client kann jedoch jederzeit die **ValidateState-Methode** eines beliebigen Transportanbieters aufrufen. Wenn Ihr Transportanbieter versucht, während der Verarbeitung von **ValidateState** eine fehlerhafte Ressource zuzuweisen, kann ein Fehler aufgrund eines Konflikts mit einem anderen Transportanbieter auftreten, den der MAPI-Spooler angewiesen hat, seine Warteschlangen zu leeren. Wenn Sie zulassen, dass alle Verteilungsressourcenzuweisungen unter der Richtung des MAPI-Spoolers erfolgen, können Sie solche Konflikte vermeiden. Ihr Transportanbieter sollte die **PR_REMOTE_VALIDATE_OK-Eigenschaft** unterstützen, damit Clientanwendungen erkennen können, wann Ihr Transportanbieter ausgelastet ist oder darauf wartet, dass der MAPI-Spooler eine Aktion initiiert. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Da diese Methode andere potenziell längere Aufrufe verursachen kann, kann **ValidateState** MAPI_E_BUSY zurückgeben, um Sie darüber zu informieren, dass diese Methode auf den Abschluss eines anderen Vorgangs wartet. Warten Sie, bis der ausstehende Vorgang abgeschlossen ist, bevor Sie eine andere Aufgabe ausführen. 
  
Sie haben die größte Kontrolle über Ihre Aufrufe von Transportanbieter-Statusobjekten. Sie können ein oder mehrere Flags an **ValidateState** übergeben, die sich auf die Vorgänge des Transportanbieters auswirken. Beispielsweise gibt die ABORT_XP_HEADER_OPERATION-Kennzeichnung an, dass der Benutzer die Überprüfung abgebrochen hat. Transportanbieter können entscheiden, abzubricht, MAPI_E_USER_CANCELED zurückzugeben, oder sie können fortfahren. 
  
Sie können das CONFIG_CHANGED Flag für einen Aufruf entweder an das Statusobjekt eines Dienstanbieters oder den MAPI-Spooler festlegen, um anzugeben, dass eine Konfigurationsoption geändert wurde. Sie können CONFIG_CHANGED verwenden, um einen Transportanbieter dynamisch neu zu konfigurieren. Wenn Sie CONFIG_CHANGED für einen Aufruf des Statusobjekts eines Dienstanbieters festlegen, antwortet der Anbieter mit einem Aufruf von [IMAPISupport::SpoolerNotify,](imapisupport-spoolernotify.md) um den MAPI-Spooler über die Änderung zu benachrichtigen. Wenn Sie CONFIG_CHANGED für einen Aufruf des Statusobjekts des MAPI-Spoolers festlegen, ruft der Spooler [IXPLogon::AddressTypes](ixplogon-addresstypes.md) für jeden aktiven Transportanbieter auf. **AddressTypes** informiert den MAPI-Spooler über die unterstützten Adresstypen eines Transports. Einige Dienstanbieter zeigen auch eine Statusanzeige an, wenn die Überprüfung voraussichtlich lange dauert. Das Anzeigen einer Statusanzeige ist hilfreich, aber nicht erforderlich. 
  
Wenn das SUPPRESS_UI-Kennzeichen festgelegt ist, können keines der Konfigurationseigenschaftenblätter oder Statusdialogfelder angezeigt werden. 
  
## <a name="see-also"></a>Siehe auch

- [IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md)
- [IXPLogon::AddressTypes](ixplogon-addresstypes.md)
- [IXPLogon::FlushQueues](ixplogon-flushqueues.md)
- [PidTagRemoteValidateOk (kanonische Eigenschaft)](pidtagremotevalidateok-canonical-property.md)
- [PidTagResourceMethods (kanonische Eigenschaft)](pidtagresourcemethods-canonical-property.md)
- [Kanonische PidTagStatusCode-Eigenschaft](pidtagstatuscode-canonical-property.md)
- [Kanonische PidTagStatusString-Eigenschaft](pidtagstatusstring-canonical-property.md)
- [IMAPIStatus : IMAPIProp](imapistatusimapiprop.md)

