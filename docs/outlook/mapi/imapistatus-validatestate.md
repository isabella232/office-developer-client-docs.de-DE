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
  
Bestätigt die externen Statusinformationen für die MAPI-Ressource oder den Dienstanbieter. Diese Methode wird in allen Status-Objekten unterstützt. 
  
```cpp
HRESULT ValidateState(
  ULONG_PTR ulUIParam,
  ULONG ulFlags
);
```

## <a name="parameters"></a>Parameter

_ulUIParam_
  
> in Ein Handle für das übergeordnete Fenster aller von dieser Methode angezeigten Dialogfelder oder Fenster.
    
_ulFlags_
  
> in Eine Bitmaske von Flags, die die Validierung steuert. Die folgenden Flags können festgelegt werden:
    
ABORT_XP_HEADER_OPERATION
  
> Der Benutzer hat den Vorgang abgebrochen, indem er in der Regel auf die Schaltfläche **Abbrechen** im entsprechenden Dialogfeld geklickt hat. Das Status-Objekt verfügt über zwei Optionen: 
    
   - Arbeiten Sie weiterhin an dem Vorgang.
    
   - Beenden Sie den Vorgang, und geben Sie MAPI_E_USER_CANCELED.
    
CONFIG_CHANGED 
  
> Eine oder mehrere der Konfigurationseigenschaften des Status-Objekts wurden geändert. Clients können dieses Flag festlegen, um zu ermöglichen, dass der MAPI-Spooler kritische Transportanbieter Fehler dynamisch korrigiert. 
    
FORCE_XP_CONNECT 
  
> Das Status-Objekt sollte eine Verbindung herstellen. Wenn dieses Flag mit dem REFRESH_XP_HEADER_CACHE-oder PROCESS_XP_HEADER_CACHE-Flag verwendet wird, erfolgt die Verbindung ohne Zwischenspeicherung.
    
FORCE_XP_DISCONNECT 
  
> Das Status-Objekt sollte einen Disconnect-Vorgang ausführen. Wenn dieses Flag mit dem REFRESH_XP_HEADER_CACHE-oder PROCESS_XP_HEADER_CACHE-Flag verwendet wird, erfolgt die Trennung ohne Zwischenspeicherung.
    
PROCESS_XP_HEADER_CACHE 
  
> Einträge in der Kopfzeile-Cache-Tabelle sollten verarbeitet werden, alle Nachrichten, die mit dem MSGSTATUS_REMOTE_DOWNLOAD-Flag gekennzeichnet sind, sollten heruntergeladen werden, und alle Nachrichten, die mit dem MSGSTATUS_REMOTE_DELETE-Flag gekennzeichnet sind, sollten gelöscht werden. Nachrichten, die sowohl MSGSTATUS_REMOTE_DOWNLOAD als auch MSGSTATUS_REMOTE_DELETE festgelegt haben, sollten verschoben werden.
    
REFRESH_XP_HEADER_CACHE 
  
> Bei einem Remote Transportanbieter sollte eine neue Liste mit Nachrichtenkopfzeilen heruntergeladen werden, und alle Kennzeichnungen, die den Nachrichtenstatus markieren, sollten gelöscht werden.
    
SUPPRESS_UI 
  
> Verhindert, dass das Statusobjekt eine Benutzeroberfläche als Teil des Vorgangs anzeigt.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Die Überprüfung war erfolgreich.
    
MAPI_E_BUSY 
  
> Ein anderer Vorgang wird ausgeführt; Sie sollte zugelassen werden, oder Sie sollte beendet werden, bevor dieser Vorgang eingeleitet wird.
    
MAPI_E_NO_SUPPORT 
  
> Das Status-Objekt unterstützt die Validierungsmethode nicht, wie durch das Fehlen des STATUS_VALIDATE_STATE-Flags in der **PR_RESOURCE_METHODS** ([pidtagresourcemethods (](pidtagresourcemethods-canonical-property.md))-Eigenschaft angegeben.
    
MAPI_E_USER_CANCEL 
  
> Der Benutzer hat den Validierungsvorgang abgebrochen, indem er in einem Dialogfeld auf die Schaltfläche **Abbrechen** geklickt hat. Dieser Wert wird nur von Remote Transportanbietern zurückgegeben. 
    
## <a name="remarks"></a>Bemerkungen

Die **IMAPIStatus:: ValidateState** -Methode überprüft den Status einer Ressource, die einem Statusobjekt zugeordnet ist. **ValidateState** ist die einzige Methode in der [IMAPIStatus](imapistatusimapiprop.md) -Schnittstelle, die für alle Status-Objekte erforderlich ist. Das genaue Verhalten dieser Methode hängt von der Implementierung ab. In der folgenden Tabelle wird die Implementierung der einzelnen Arten von Statusobjekten beschrieben. 
  
|**Status-Objekt**|ValidateState * * Implementierung * *|
|:-----|:-----|
|MAPI-Subsystem  <br/> |Überprüft den Status aller Ressourcen, die die derzeit aktiven Dienstanbieter und das Subsystem selbst besitzen.  <br/> |
|MAPI-Spooler  <br/> |Führt eine Anmeldung aller Transportanbieter aus, unabhängig davon, ob Sie bereits angemeldet sind.  <br/> |
|MAPI-Adressbuch  <br/> |Überprüft die Einträge im Profil Abschnitt.  <br/> |
|Dienstanbieter  <br/> |Die Implementierung hängt vom Anbietertyp und den im _ulFlags_ -Parameter festgelegten Flags ab.  <br/> |
   
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Remote Clientanwendungen rufen die **ValidateState** -Methode auf, um die Remoteverarbeitung für verschiedene Aktionen zu starten. Diese Methode besteht hauptsächlich darin, Statusbits für die Kommunikation mit dem MAPI-Spooler festzulegen, statt tatsächlich arbeiten auszuführen. In der Regel legt der Transportanbieter Flags in der Statuszeile fest, die dem MAPI-Spooler zeigen, welche Aktionen initiiert werden müssen, um die Anforderung des Clients abzuschließen. 

In diesem Modell der Client-Transport-Spooler-Interaktion sind die vom Client angeforderten Aktionen asynchron, da **ValidateState** zurückgegeben wird, bevor die angeforderten Aktionen abgeschlossen sind. Aktionen, die nicht notwendigerweise das zugrunde liegende Messagingsystem oder eine transportspezifische Schnittstelle beinhalten, können jedoch synchron sein. Die Clientanwendung übergibt eine Bitmaske der folgenden Flags, um anzugeben, welche Aktionen vom Remote Transportanbieter ausgeführt werden sollen. 
  
ABORT_XP_HEADER_OPERATION 
  
> Wenn möglich, sollte der Remote Transportanbieter alle Vorgänge abbrechen, die das Herunterladen von Kopfzeilen beinhalten. Hierzu muss der Transportanbieter die folgenden Eigenschaftswerte in der Statuszeile des LOGON-Objekts festlegen:
    
   - Löschen Sie die STATUS_INBOUND_ENABLED-und STATUS_INBOUND_ACTIVE-Bits in der **PR_STATUS_CODE** ([pidtagstatuscode (](pidtagstatuscode-canonical-property.md))-Eigenschaft, um dem MAPI-Spooler mitzuteilen, dass der Prozess für eingehende Flush für diesen Transportanbieter angehalten werden soll.
    
   - Legen Sie das STATUS_OFFLINE-Bit in der **PR_STATUS_CODE** -Eigenschaft fest. 
    
   - Legen Sie die **PR_REMOTE_VALIDATE_OK** ([pidtagremotevalidateok (](pidtagremotevalidateok-canonical-property.md))-Eigenschaft auf true fest.
    
   - Legen Sie die **PR_STATUS_STRING** ([pidtagstatusstring (](pidtagstatusstring-canonical-property.md))-Eigenschaft auf eine Zeichenfolge fest, die den Status des Transportanbieters für den Benutzer angibt.
    
   - Geben Sie S_OK zur�ck. Wenn jedoch der laufende Vorgang nicht abgebrochen werden kann, sollte **VALIDATESTATE** MAPI_E_BUSY zurückgeben. 
    
FORCE_XP_CONNECT 
  
> Ein Remote Transportanbieter sollte niemals eine Verbindung zu einer freigegebenen Ressource (beispielsweise einem Modem oder COM-Anschluss) außerhalb des Kontexts der MAPI-Spooler-Transport Interaktion herstellen, die an der [IXPLogon:: FlushQueues](ixplogon-flushqueues.md) -Methode beteiligt ist. Wenn **ValidateState** mit diesem Flag aufgerufen wird, sollte der Transportanbieter folgende Schritte ausführen: 
    
   - Legen Sie ein internes Statuskennzeichen fest, um anzugeben, dass die Remoteverbindung hergestellt werden muss, wenn die **IXPLogon:: FlushQueues** -Methode aufgerufen wird. 
    
   - Legen Sie die richtigen Werte in der Statustabelle fest, damit der MAPI-Spooler den Prozess der Warteschlangen Bereinigung initiiert.
    
   - Wenn das Leeren der Warteschlangen abgeschlossen ist, lassen Sie die freigegebene Ressource frei.
    
   - Löschen Sie das STATUS_OFFLINE-Bit in der **PR_STATUS_CODE** -Eigenschaft. 
    
   - Geben Sie S_OK zur�ck.
    
FORCE_XP_DISCONNECT 
  
> Der Remote Transportanbieter sollte seine Verbindung mit den Messagingsystem Ressourcen freigeben. Anschließend sollte das STATUS_OFFLINE-Bit in der **PR_STATUS_CODE** -Eigenschaft festgelegt und S_OK zurückgegeben werden. 
    
PROCESS_XP_HEADER_CACHE 
  
> Der Remote Transportanbieter sollte Remotenachrichten verarbeiten und alle verzögerten Nachrichten hochladen. Hierzu muss der Transportanbieter die folgenden Eigenschaftswerte in der Statuszeile des LOGON-Objekts festlegen:
    
   - Legen Sie die **PR_STATUS_STRING** -Eigenschaft auf eine Zeichenfolge fest, die den Status des Transportanbieters für den Benutzer angibt. 
    
   - Legen Sie die STATUS_OUTBOUND_ENABLED-und STATUS_OUTBOUND_ACTIVE-Bits in der **PR_STATUS_CODE** -Eigenschaft fest. 
    
   - Legen Sie die **PR_REMOTE_VALIDATE_OK** -Eigenschaft in der Statuszeile des Transportanbieters auf false fest. 
    
   - Wenn ein anderer Vorgang ausgeführt wird (beispielsweise das Herunterladen von Kopfzeilen), wenn **ValidateState** aufgerufen wird, sollte **ValidateState** MAPI_E_BUSY zurückgeben. 
    
   - Führen Sie den Code für die Verarbeitung des REFRESH_XP_HEADER_CACHE-Flags aus, um die Anforderungen des Microsoft Exchange-Clients zu erfüllen.
    
REFRESH_XP_HEADER_CACHE 
  
> Der Remote Transportanbieter sollte neue Nachrichtenkopfzeilen aus dem Messagingsystem abrufen. Hierzu muss der Transportanbieter folgende Schritte ausführen:
    
   - Legen Sie die **PR_STATUS_STRING** -Eigenschaft auf eine Zeichenfolge fest, die den Status des Transportanbieters für den Benutzer angibt. 
    
   - Legen Sie die STATUS_INBOUND_ENABLED-und STATUS_INBOUND_ACTIVE-Bits in der **PR_STATUS_CODE** -Eigenschaft fest. 
    
   - Löschen Sie das STATUS_OFFLINE-Bit in der **PR_STATUS_CODE** -Eigenschaft. 
    
   - Legen Sie das STATUS_ONLINE-Bit in der **PR_STATUS_CODE** -Eigenschaft fest. 
    
   - Legen Sie die **PR_REMOTE_VALIDATE_OK** -Eigenschaft in der Statuszeile des Transportanbieters auf false fest. 
    
SHOW_XP_SESSION_UI 
  
> Wenn Ihr Transportanbieter über Teile der Benutzeroberfläche für die Verarbeitung der Nachrichtenkopfzeilen verfügt (beispielsweise ein Dialogfeld, das das Herunterladen von Nachrichten bestätigt), sollte dieses Dialogfeld angezeigt werden. Andernfalls kann **VALIDATESTATE** MAPI_E_NO_SUPPORT zurückgeben. 
    
Wenn andere Flags als diese übergeben werden, sollte **VALIDATESTATE** MAPI_E_UNKNOWN_FLAGS zurückgeben. 
  
Der Aufruf des Clients an den Transportanbieter erfolgt häufig über die **IMAPIStatus:: ValidateState** -Methode. Während der Verarbeitung von **ValidateState**sollte der Transportanbieter keine Aktionen ausführen, die knappe Systemressourcen wie ein Modem oder einen COM-Anschluss zuweisen. Der Grund dafür ist, dass der MAPI-Spooler manchmal Warteschlangen für mehrere Transportanbieter leeren muss. Der Client kann jedoch jederzeit die **ValidateState** -Methode eines beliebigen Transportanbieters aufrufen. Wenn Ihr Transportanbieter versucht, eine knappe Ressource während der Verarbeitung von **ValidateState**zu reservieren, kann ein Fehler aufgrund eines Konflikts mit einem anderen Transportanbieter verursacht werden, den der MAPI-Spooler angewiesen hat, seine Warteschlangen zu leeren. Wenn Sie zulassen, dass alle knappen Ressourcenzuordnungen unter der Richtung des MAPI-Spoolers auftreten, können Sie solche Konflikte vermeiden. Der Transportanbieter sollte die **PR_REMOTE_VALIDATE_OK** -Eigenschaft unterstützen, damit Clientanwendungen feststellen können, ob der Transportanbieter ausgelastet ist oder darauf wartet, dass der MAPI-Spooler eine Aktion initiiert. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Da diese Methode andere potenziell langwierige Aufrufe auslösen kann, kann **VALIDATESTATE** MAPI_E_BUSY zurückgeben, um Sie darüber zu informieren, dass diese Methode auf den Abschluss eines anderen Vorgangs wartet. Sie sollten warten, bis der ausstehende Vorgang abgeschlossen ist, bevor Sie eine andere Aufgabe ausführen. 
  
Sie haben die größte Kontrolle über Ihre Aufrufe an Transportanbieter Status-Objekte. Sie können ein oder mehrere Flags an **ValidateState** , die sich auf die Vorgänge des Transportanbieters auswirken. Das ABORT_XP_HEADER_OPERATION-Flag gibt beispielsweise an, dass der Benutzer die Validierung abgebrochen hat. Transport Anbieter können entscheiden, ob Sie abgebrochen werden, MAPI_E_USER_CANCELED zurückgeben oder fortfahren können. 
  
Sie können das CONFIG_CHANGED-Flag für einen Aufruf entweder an das Status-Objekt eines Dienstanbieters oder an den MAPI-Spooler festlegen, um anzugeben, dass eine Konfigurationsoption geändert wurde. Sie können CONFIG_CHANGED verwenden, um einen Transportanbieter dynamisch neu zu konfigurieren. Wenn Sie CONFIG_CHANGED für einen Aufruf des Status Objekts eines Dienstanbieters festlegen, antwortet der Anbieter mit einem Aufruf von [IMAPISupport:: SpoolerNotify](imapisupport-spoolernotify.md) , um den MAPI-Spooler der Änderung zu benachrichtigen. Wenn Sie CONFIG_CHANGED für einen Aufruf des Status Objekts des MAPI-Spoolers festlegen, ruft der Spooler [IXPLogon:: AddressTypes](ixplogon-addresstypes.md) für jeden aktiven Transportanbieter auf. **AddressTypes** informiert den MAPI-Spooler über die unterstützten Adresstypen eines Transports. Einige Dienstanbieter zeigen auch eine Statusanzeige an, wenn die Überprüfung sehr lange dauern wird. Das Anzeigen einer Statusanzeige ist hilfreich, aber nicht erforderlich. 
  
Wenn das SUPPRESS_UI-Flag festgelegt ist, können keine der Konfigurationseigenschaften Blätter oder Fortschritts Dialogfelder angezeigt werden. 
  
## <a name="see-also"></a>Siehe auch

- [IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md)
- [IXPLogon::AddressTypes](ixplogon-addresstypes.md)
- [IXPLogon::FlushQueues](ixplogon-flushqueues.md)
- [Kanonische Pidtagremotevalidateok (-Eigenschaft](pidtagremotevalidateok-canonical-property.md)
- [Kanonische Pidtagresourcemethods (-Eigenschaft](pidtagresourcemethods-canonical-property.md)
- [Kanonische Pidtagstatuscode (-Eigenschaft](pidtagstatuscode-canonical-property.md)
- [Kanonische Pidtagstatusstring (-Eigenschaft](pidtagstatusstring-canonical-property.md)
- [IMAPIStatus : IMAPIProp](imapistatusimapiprop.md)

