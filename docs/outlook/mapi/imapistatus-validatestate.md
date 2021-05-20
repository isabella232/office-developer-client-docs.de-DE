---
title: IMAPIStatusValidateState
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIStatus.ValidateState
api_type:
- COM
ms.assetid: 036b9b15-86e1-4a37-8e4b-e37b2963d8fb
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: adcdf04653f8c9fed2ecc6520648abd3acd36134
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438148"
---
# <a name="imapistatusvalidatestate"></a>IMAPIStatus::ValidateState

**Gilt für**: Outlook 2013 | Outlook 2016 
  
Bestätigt die externen Statusinformationen, die für die MAPI-Ressource oder den Dienstanbieter verfügbar sind. Diese Methode wird in allen Statusobjekten unterstützt. 
  
```cpp
HRESULT ValidateState(
  ULONG_PTR ulUIParam,
  ULONG ulFlags
);
```

## <a name="parameters"></a>Parameter

_ulUIParam_
  
> [in] Ein Handle zum übergeordneten Fenster aller Dialogfelder oder Fenster, die von dieser Methode angezeigt werden.
    
_ulFlags_
  
> [in] Eine Bitmaske mit Flags, die die Überprüfung steuert. Die folgenden Kennzeichen können festgelegt werden:
    
ABORT_XP_HEADER_OPERATION
  
> Der Benutzer hat den Vorgang abgebrochen, in der Regel durch Klicken auf die **Schaltfläche** Abbrechen im entsprechenden Dialogfeld. Das status-Objekt verfügt über zwei Optionen: 
    
   - Arbeiten Sie weiter an dem Vorgang.
    
   - Beenden Sie den Vorgang, und geben Sie MAPI_E_USER_CANCELED.
    
CONFIG_CHANGED 
  
> Eine oder mehrere Konfigurationseigenschaften des Statusobjekts wurden geändert. Clients können dieses Kennzeichen festlegen, damit der MAPI-Spooler kritische Fehler des Transportanbieters dynamisch korrigieren kann. 
    
FORCE_XP_CONNECT 
  
> Das status-Objekt sollte eine Verbindung ausführen. Wenn dieses Flag mit dem REFRESH_XP_HEADER_CACHE- oder PROCESS_XP_HEADER_CACHE verwendet wird, erfolgt die Verbindung ohne Zwischenspeicherung.
    
FORCE_XP_DISCONNECT 
  
> Das status-Objekt sollte einen Verbindungstrennungsvorgang ausführen. Wenn dieses Flag mit dem REFRESH_XP_HEADER_CACHE- oder PROCESS_XP_HEADER_CACHE verwendet wird, erfolgt die Trennung ohne Zwischenspeicherung.
    
PROCESS_XP_HEADER_CACHE 
  
> Einträge in der Kopfzeilencachetabelle sollten verarbeitet werden, alle nachrichten, die mit dem flag MSGSTATUS_REMOTE_DOWNLOAD gekennzeichnet sind, heruntergeladen werden, und alle Nachrichten, die mit dem MSGSTATUS_REMOTE_DELETE gekennzeichnet sind, sollten gelöscht werden. Nachrichten, die sowohl MSGSTATUS_REMOTE_DOWNLOAD als auch MSGSTATUS_REMOTE_DELETE festgelegt sind, sollten verschoben werden.
    
REFRESH_XP_HEADER_CACHE 
  
> Für einen Remotetransportanbieter sollte eine neue Liste von Nachrichtenkopfzeilen heruntergeladen werden, und alle Kennzeichen, die den Nachrichtenstatus markieren, sollten entfernt werden.
    
SUPPRESS_UI 
  
> Verhindert, dass das Statusobjekt eine Benutzeroberfläche im Rahmen des Vorgangs angezeigt.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Die Überprüfung war erfolgreich.
    
MAPI_E_BUSY 
  
> Ein weiterer Vorgang wird ausgeführt. Er sollte abgeschlossen oder beendet werden dürfen, bevor dieser Vorgang initiiert wird.
    
MAPI_E_NO_SUPPORT 
  
> Das status-Objekt unterstützt die Überprüfungsmethode nicht, wie durch das Fehlen des STATUS_VALIDATE_STATE-Flag in der **PR_RESOURCE_METHODS** ([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md)) -Eigenschaft angegeben.
    
MAPI_E_USER_CANCEL 
  
> Der Benutzer hat den Überprüfungsvorgang abgebrochen, in der Regel durch Klicken auf die **Schaltfläche** Abbrechen in einem Dialogfeld. Dieser Wert wird nur von Remote-Transport-Anbietern zurückgegeben. 
    
## <a name="remarks"></a>Hinweise

Die **IMAPIStatus::ValidateState-Methode** überprüft den Status einer Ressource, die einem Statusobjekt zugeordnet ist. **ValidateState** ist die einzige Methode in der [IMAPIStatus-Schnittstelle,](imapistatusimapiprop.md) die für alle Statusobjekte erforderlich ist. Das genaue Verhalten dieser Methode hängt von der Implementierung ab. In der folgenden Tabelle wird die Implementierung der einzelnen Typen von Statusobjekten beschrieben. 
  
|**Status-Objekt**|ValidateState**-Implementierung**|
|:-----|:-----|
|MAPI-Subsystem  <br/> |Überprüft den Status aller Ressourcen, die die derzeit aktiven Dienstanbieter und das Subsystem selbst besitzen.  <br/> |
|MAPI-Spooler  <br/> |Führt eine Anmeldung aller Transportanbieter aus, unabhängig davon, ob sie bereits angemeldet sind.  <br/> |
|MAPI-Adressbuch  <br/> |Überprüft die Einträge im Profilabschnitt.  <br/> |
|Dienstanbieter  <br/> |Die Implementierung hängt vom Typ des Anbieters und den im  _ulFlags-Parameter festgelegten Flags_ ab.  <br/> |
   
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Remoteclientanwendungen rufen die **ValidateState-Methode** auf, um die Remoteverarbeitung für verschiedene Aktionen zu starten. Diese Methode ist in erster Linie zum Festlegen von Statusbits für die Kommunikation mit dem MAPI-Spooler vorhanden, anstatt tatsächlich arbeit zu tun. In der Regel legt der Transportanbieter Flags in seiner Statuszeile fest, die dem MAPI-Spooler angeben, welche Aktionen zum Abschließen der Clientanforderung initiiert werden müssen. 

In diesem Modell der Client-Transport-Spooler-Interaktion sind die vom Client angeforderten Aktionen asynchron, da **ValidateState** zurückgibt, bevor die angeforderten Aktionen abgeschlossen sind. Aktionen, die nicht unbedingt das zugrunde liegende Messagingsystem oder eine transportspezifische Schnittstelle betreffen, können jedoch synchron sein. Die Clientanwendung übergibt eine Bitmaske der folgenden Flags, um anzugeben, welche Aktionen der Remotetransportanbieter ausführen soll. 
  
ABORT_XP_HEADER_OPERATION 
  
> Wenn möglich, sollte der Remotetransportanbieter alle Vorgänge abbrechen, die das Herunterladen von Kopfzeilen beinhalten. Dazu muss der Transportanbieter die folgenden Eigenschaftswerte in der Statuszeile des Anmeldeobjekts festlegen:
    
   - Löschen Sie STATUS_INBOUND_ENABLED und STATUS_INBOUND_ACTIVE bits in der **PR_STATUS_CODE** ([PidTagStatusCode](pidtagstatuscode-canonical-property.md)) -Eigenschaft, um den #A0 anzuhalten, den eingehenden Leervorgang für diesen Transportanbieter zu stoppen.
    
   - Legen Sie STATUS_OFFLINE-Bit in der **PR_STATUS_CODE-Eigenschaft.** 
    
   - Legen Sie **PR_REMOTE_VALIDATE_OK** ([PidTagRemoteValidateOk](pidtagremotevalidateok-canonical-property.md)) -Eigenschaft auf TRUE.
    
   - Legen Sie **PR_STATUS_STRING** ([PidTagStatusString](pidtagstatusstring-canonical-property.md)) -Eigenschaft auf eine Zeichenfolge fest, die den Status des Transportanbieters für den Benutzer angibt.
    
   - Geben Sie S_OK zur�ck. Wenn der ausgeführte Vorgang jedoch nicht abgebrochen werden kann, sollte **ValidateState** MAPI_E_BUSY. 
    
FORCE_XP_CONNECT 
  
> Ein Remote-Transport-Anbieter sollte nie eine Verbindung mit einer freigegebenen Ressource (z. B. einem Modem oder EINEM COM-Port) außerhalb des Kontexts der MAPI-Spooler-Transport-Interaktion herstellen, die an der [IXPLogon::FlushQueues-Methode](ixplogon-flushqueues.md) beteiligt ist. Wenn **ValidateState** mit diesem Flag aufgerufen wird, sollte Ihr Transportanbieter die folgenden Schritte unternehmen: 
    
   - Legen Sie ein internes Statusflag fest, um anzugeben, dass die Remoteverbindung hergestellt werden muss, wenn die **IXPLogon::FlushQueues-Methode** aufgerufen wird. 
    
   - Legen Sie die richtigen Werte in der Statustabelle so ein, dass der MAPI-Spooler den Warteschlangenleervorgang initiiert.
    
   - Wenn das Leeren von Warteschlangen abgeschlossen ist, geben Sie die freigegebene Ressource frei.
    
   - Löschen Sie STATUS_OFFLINE-Bit in  der PR_STATUS_CODE-Eigenschaft. 
    
   - Geben Sie S_OK zur�ck.
    
FORCE_XP_DISCONNECT 
  
> Der Remotetransportanbieter sollte seine Verbindung zu den Messagingsystemressourcen frei geben. Anschließend sollte das STATUS_OFFLINE-Bit in der **PR_STATUS_CODE-Eigenschaft** festgelegt und S_OK. 
    
PROCESS_XP_HEADER_CACHE 
  
> Der Remotetransportanbieter sollte Remotenachrichten verarbeiten und alle zurückgestellten Nachrichten hochladen. Dazu muss der Transportanbieter die folgenden Eigenschaftswerte in der Statuszeile des Anmeldeobjekts festlegen:
    
   - Legen Sie **PR_STATUS_STRING** auf eine Zeichenfolge fest, die den Status des Transportanbieters für den Benutzer angibt. 
    
   - Legen Sie die STATUS_OUTBOUND_ENABLED und STATUS_OUTBOUND_ACTIVE in der **PR_STATUS_CODE-Eigenschaft.** 
    
   - Legen Sie **PR_REMOTE_VALIDATE_OK** eigenschaft in der Statuszeile des Transportanbieters auf FALSE. 
    
   - Wenn ein anderer Vorgang ausgeführt wird (z. B. das Herunterladen von Kopfzeilen), wenn **ValidateState** aufgerufen wird, sollte **ValidateState** MAPI_E_BUSY. 
    
   - Führen Sie den Code für die Verarbeitung des REFRESH_XP_HEADER_CACHE aus, um die Anforderungen des Microsoft-Exchange erfüllen.
    
REFRESH_XP_HEADER_CACHE 
  
> Der Remotetransportanbieter sollte alle neuen Nachrichtenkopfzeilen aus dem Messagingsystem abrufen. Dazu muss der Transportanbieter die folgenden Schritte tun:
    
   - Legen Sie **PR_STATUS_STRING** auf eine Zeichenfolge fest, die den Status des Transportanbieters für den Benutzer angibt. 
    
   - Legen Sie die STATUS_INBOUND_ENABLED und STATUS_INBOUND_ACTIVE in der **PR_STATUS_CODE-Eigenschaft.** 
    
   - Löschen Sie STATUS_OFFLINE-Bit in  der PR_STATUS_CODE-Eigenschaft. 
    
   - Legen Sie STATUS_ONLINE-Bit in der **PR_STATUS_CODE-Eigenschaft.** 
    
   - Legen Sie **PR_REMOTE_VALIDATE_OK** eigenschaft in der Statuszeile des Transportanbieters auf FALSE. 
    
SHOW_XP_SESSION_UI 
  
> Wenn Ihr Transportanbieter über eine Benutzeroberfläche für die Verarbeitung der Nachrichtenkopfzeilen verfügt (z. B. ein Dialogfeld, das das Herunterladen von Nachrichten bestätigt), sollte dieses Dialogfeld angezeigt werden. Andernfalls **kann ValidateState** MAPI_E_NO_SUPPORT. 
    
Wenn andere Kennzeichen als diese übergeben werden, sollte **ValidateState** MAPI_E_UNKNOWN_FLAGS. 
  
Der Clientaufruf an den Transportanbieter wird häufig an die **IMAPIStatus::ValidateState-Methode** gesendet. Während der Verarbeitung von **ValidateState** sollte der Transportanbieter keine Aktionen ausführen, die knappe Systemressourcen zuweisen, z. B. ein Modem oder einen COM-Port. Dies liegt daran, dass der MAPI-Spooler manchmal Warteschlangen für mehrere Transportanbieter leeren muss. Der Client kann jedoch jederzeit die **ValidateState-Methode** eines beliebigen Transportanbieters aufrufen. Wenn Ihr Transportanbieter versucht, während der Verarbeitung von **ValidateState** eine knappe Ressource zuzuordnen, kann ein Fehler aufgrund eines Konflikts mit einem anderen Transportanbieter verursacht werden, den der MAPI-Spooler angewiesen hat, seine Warteschlangen zu leeren. Wenn Sie zulassen, dass alle knappen Ressourcenzuweisungen unter der Richtung des MAPI-Spoolers erfolgen, können Sie solche Konflikte vermeiden. Ihr Transportanbieter sollte die **PR_REMOTE_VALIDATE_OK-Eigenschaft** unterstützen, damit Clientanwendungen erkennen können, wann Ihr Transportanbieter ausgelastet ist oder darauf wartet, dass der MAPI-Spooler eine Aktion initiiert. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Da diese Methode dazu führen kann, dass andere potenziell langwierige Aufrufe vorgenommen werden, kann **ValidateState** MAPI_E_BUSY zurückgeben, um Sie darüber zu informieren, dass diese Methode auf den Abschluss eines anderen Vorgangs wartet. Sie sollten warten, bis der ausstehende Vorgang abgeschlossen ist, bevor Sie eine andere Aufgabe versuchen. 
  
Sie haben die größte Kontrolle über Ihre Aufrufe an Statusobjekte des Transportanbieters. Sie können ein oder mehrere Flags an **ValidateState** übergeben, die sich auf die Vorgänge des Transportanbieters auswirken. Das Flag ABORT_XP_HEADER_OPERATION z. B. an, dass der Benutzer die Überprüfung abgebrochen hat. Transportanbieter können sich für einen Abbruch entscheiden, MAPI_E_USER_CANCELED zurückgeben oder fortfahren. 
  
Sie können das CONFIG_CHANGED für einen Aufruf des Statusobjekts eines Dienstanbieters oder des MAPI-Spoolers festlegen, um anzugeben, dass eine Konfigurationsoption geändert wurde. Sie können die CONFIG_CHANGED verwenden, um einen Transportanbieter dynamisch neu zu konfigurieren. Wenn Sie CONFIG_CHANGED einem Aufruf des Statusobjekts eines Dienstanbieters festlegen, antwortet der Anbieter mit einem Aufruf von [IMAPISupport::SpoolerNotify,](imapisupport-spoolernotify.md) um den MAPI-Spooler über die Änderung zu warnen. Wenn Sie CONFIG_CHANGED Aufruf des Statusobjekts des MAPI-Spoolers festlegen, ruft der Spooler [IXPLogon::AddressTypes](ixplogon-addresstypes.md) für jeden aktiven Transportanbieter auf. **AddressTypes** informiert den MAPI-Spooler über die unterstützten Adresstypen eines Transports. Einige Dienstanbieter zeigen auch einen Fortschrittsindikator an, wenn die Überprüfung voraussichtlich sehr lange dauert. Das Anzeigen eines Statusindikators ist hilfreich, aber nicht erforderlich. 
  
Wenn das SUPPRESS_UI festgelegt ist, können keines der Konfigurationseigenschaftsblätter oder Statusdialogfelder angezeigt werden. 
  
## <a name="see-also"></a>Siehe auch

- [IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md)
- [IXPLogon::AddressTypes](ixplogon-addresstypes.md)
- [IXPLogon::FlushQueues](ixplogon-flushqueues.md)
- [PidTagRemoteValidateOk (kanonische Eigenschaft)](pidtagremotevalidateok-canonical-property.md)
- [PidTagResourceMethods (kanonische Eigenschaft)](pidtagresourcemethods-canonical-property.md)
- [PidTagStatusCode (kanonische Eigenschaft)](pidtagstatuscode-canonical-property.md)
- [PidTagStatusString (kanonische Eigenschaft)](pidtagstatusstring-canonical-property.md)
- [IMAPIStatus : IMAPIProp](imapistatusimapiprop.md)

