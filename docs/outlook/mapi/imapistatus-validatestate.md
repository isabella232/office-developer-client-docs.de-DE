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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 3ff29ac7e7f9b7876bb678930390ca556351ecf6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792364"
---
# <a name="imapistatusvalidatestate"></a>IMAPIStatus::ValidateState

**Betrifft**: Outlook 
  
Bestätigen Sie die externen Statusinformationen für die MAPI-Ressource oder den Dienstanbieter. Diese Methode wird in allen Status-Objekten unterstützt. 
  
```cpp
HRESULT ValidateState(
  ULONG_PTR ulUIParam,
  ULONG ulFlags
);
```

## <a name="parameters"></a>Parameter

_ulUIParam_
  
> [in] Ein Handle für das übergeordnete Fenster für alle Dialogfelder oder Windows, die diese Methode anzeigt.
    
_ulFlags_
  
> [in] Eine Bitmaske aus Flags, die die Überprüfung steuert. Die folgenden Kennzeichen können festgelegt werden:
    
ABORT_XP_HEADER_OPERATION
  
> Der Benutzer hat den Vorgang in der Regel durch Klicken auf die Schaltfläche **Abbrechen** , in dem entsprechenden Dialogfeld abgebrochen. Das Statusobjekt besitzt zwei Optionen zur Verfügung: 
    
   - Fortsetzen Sie Arbeit an den Vorgang.
    
   - Beenden Sie den Vorgang, und geben Sie MAPI_E_USER_CANCELED zurück.
    
CONFIG_CHANGED 
  
> Eine oder mehrere der Eigenschaften von Konfiguration der Status des Objekts geändert. Clients können dieses Kennzeichen ermöglicht die MAPI-Warteschlange dynamisch kritische Transport Anbieter Fehler korrigieren festlegen. 
    
FORCE_XP_CONNECT 
  
> Das Statusobjekt sollte eine Verbindung ausführen. Wenn dieses Flag mit dem REFRESH_XP_HEADER_CACHE oder PROCESS_XP_HEADER_CACHE-Flag verwendet wird, tritt die Verbindung ohne Zwischenspeichern.
    
FORCE_XP_DISCONNECT 
  
> Das Statusobjekt sollte einen Trennvorgang auszuführen. Wenn dieses Flag mit dem REFRESH_XP_HEADER_CACHE oder PROCESS_XP_HEADER_CACHE-Flag verwendet wird, tritt das Trennen der Verbindung ohne Zwischenspeichern.
    
PROCESS_XP_HEADER_CACHE 
  
> Einträge in der Kopfzeile Cachetabelle verarbeitet werden soll, sollten alle Nachrichten mit dem MSGSTATUS_REMOTE_DOWNLOAD-Flag heruntergeladen werden und alle Nachrichten mit dem MSGSTATUS_REMOTE_DELETE-Flag gekennzeichnet gelöscht werden sollen. Nachrichten, die MSGSTATUS_REMOTE_DOWNLOAD und MSGSTATUS_REMOTE_DELETE festgelegt haben, sollten verschoben werden.
    
REFRESH_XP_HEADER_CACHE 
  
> Bei einem remote-Transport-Anbieter sollte eine neue Liste der Kopfzeilen heruntergeladen werden, und alle Flags, die die Nachricht den Status markieren sollte deaktiviert werden.
    
SUPPRESS_UI 
  
> Verhindert, dass das Statusobjekt eine Benutzeroberfläche als Teil des Vorgangs angezeigt.
    
## <a name="return-value"></a>R�ckgabewert

S_OK 
  
> Die Überprüfung war erfolgreich.
    
MAPI_E_BUSY 
  
> Ein anderer Vorgang ist in Bearbeitung. Es dürfen für die Durchführung, oder er angehalten werden sollte, bevor Sie diesen Vorgang gestartet wird.
    
MAPI_E_NO_SUPPORT 
  
> Das Statusobjekt unterstützt nicht die Methode für die Überprüfung, wie durch die Abwesenheit des STATUS_VALIDATE_STATE-Flags in der Eigenschaft **PR_RESOURCE_METHODS** ([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md)) angegeben.
    
MAPI_E_USER_CANCEL 
  
> Der Benutzer hat den Überprüfungsvorgang in der Regel durch Klicken auf die Schaltfläche " **Abbrechen** " in einem Dialogfeld abgebrochen. Dieser Wert wird nur von remote-Transport-Anbietern zurückgegeben. 
    
## <a name="remarks"></a>Bemerkungen

Die **IMAPIStatus::ValidateState** -Methode überprüft den Status einer Ressource, die ein Statusobjekt zugeordnet ist. **ValidateState** ist die einzige Methode in der [IMAPIStatus](imapistatusimapiprop.md) -Schnittstelle, die für alle Status erforderlich ist. Das genaue Verhalten dieser Methode hängt von der Implementierung. Die folgende Tabelle beschreibt die Implementierung der verschiedenen Arten von Status-Objekten. 
  
|**Statusobjekt**|ValidateState ** Implementierung **|
|:-----|:-----|
|MAPI-Subsystems  <br/> |Überprüft den Status aller Ressourcen, die die derzeit aktive-Dienstanbieter und Teilsystems selbst besitzen.  <br/> |
|MAPI-Warteschlange  <br/> |Führt eine Anmeldung aller Transport-Anbieter, unabhängig davon, ob sie bereits angemeldet sind.  <br/> |
|MAPI-Adressbuch  <br/> |Überprüft die Einträge in einem Profilabschnitt.  <br/> |
|Dienstanbieter  <br/> |Implementierung hängt die Art der Anbieter und die Kennzeichen, die im Parameter _UlFlags_ festgelegt.  <br/> |
   
## <a name="notes-to-implementers"></a>Hinweise für Implementierer

Remote-Clientanwendungen rufen Sie die **ValidateState** -Methode, um remote Verarbeitung für verschiedene Aktionen zu starten. Diese Methode vorhanden ist, in erster Linie um Statusbits der MAPI-Warteschlange, anstatt Kommunikation tatsächlich Arbeit leisten festgelegt. In der Regel wird der Adressbuchhierarchie Flags in der Statuszeile, die an die Warteschlange MAPI angeben, welche Aktionen initiiert werden, um die Anforderung des Clients abzuschließen müssen. 

In diesem Modell der Interaktion von Client-Transport-Warteschlange sind die Aktionen, die vom Client angeforderten asynchronen, **ValidateState** zurückgibt, bevor die angeforderten Aktionen abgeschlossen sind. Aktionen, die das zugrunde liegende messaging-System nicht unbedingt beinhalten oder bereit, die eine Schnittstelle Transport-spezifischen beinhalten, können jedoch synchrone sein. Die Client-Anwendung übergibt eine Bitmaske der folgenden Werte aus, um anzugeben, welche Aktivitäten der Adressbuchhierarchie remote ausgeführt werden soll. 
  
ABORT_XP_HEADER_OPERATION 
  
> Wenn möglich, sollte der remote Adressbuchhierarchie Vorgänge abzubrechen, die umfassen Kopfzeilen heruntergeladen. Hierzu muss der Adressbuchhierarchie die folgenden Eigenschaftswerte in der Statuszeile des Anmeldung-Objekts festgelegt:
    
   - Deaktivieren Sie die Bits STATUS_INBOUND_ENABLED und STATUS_INBOUND_ACTIVE in der Eigenschaft **PR_STATUS_CODE** ([PidTagStatusCode](pidtagstatuscode-canonical-property.md)) anzuweisen, die MAPI-Warteschlange den eingehenden flush-Prozess für diesen Transportanbieter anhalten.
    
   - Legen Sie die STATUS_OFFLINE bit in der **PR_STATUS_CODE** -Eigenschaft. 
    
   - Legen Sie die **PR_REMOTE_VALIDATE_OK** ([PidTagRemoteValidateOk](pidtagremotevalidateok-canonical-property.md))-Eigenschaft auf true fest.
    
   - Legen Sie die **PR_STATUS_STRING** ([PidTagStatusString](pidtagstatusstring-canonical-property.md))-Eigenschaft auf eine Zeichenfolge, die der Adressbuchhierarchie Status für den Benutzer angibt.
    
   - Geben Sie S_OK zur�ck. Wenn der Vorgang in Arbeit kann nicht abgebrochen werden, sollte **ValidateState** MAPI_E_BUSY zurückgegeben. 
    
FORCE_XP_CONNECT 
  
> Ein remote Transportdienstes richten Sie eine Verbindung mit einer freigegebenen Ressource (z. B. Modem oder COM-Anschluss) außerhalb des Kontexts der MAPI-Warteschlange-Transport-Aktivität beteiligt die [IXPLogon::FlushQueues](ixplogon-flushqueues.md) -Methode sollte niemals. Wenn dieses Flag **ValidateState** aufgerufen wird, sollte der Adressbuchhierarchie Folgendes ausführen: 
    
   - Legen Sie einen internen Status-Flag, um anzugeben, dass die Verbindung hergestellt werden muss, die **IXPLogon::FlushQueues** -Methode aufgerufen wird. 
    
   - Legen Sie die richtigen Werte in der Statustabelle ", die dazu führen, dass die MAPI-Warteschlange, die Warteschlange, die leeren Prozess zu initiieren.
    
   - Wenn das Leeren der Warteschlangen abgeschlossen ist, lassen Sie freigegebene Ressource.
    
   - Deaktivieren Sie das STATUS_OFFLINE bit in der **PR_STATUS_CODE** -Eigenschaft. 
    
   - Geben Sie S_OK zur�ck.
    
FORCE_XP_DISCONNECT 
  
> Der remote Adressbuchhierarchie sollte die Verbindung mit der messaging Systemressourcen freigeben. Nach dem auf diese Weise sollte es das STATUS_OFFLINE Bit in der **PR_STATUS_CODE** -Eigenschaft festgelegt und S_OK zurück. 
    
PROCESS_XP_HEADER_CACHE 
  
> Der remote Adressbuchhierarchie sollte remote-Nachrichten zu verarbeiten und Hochladen von Nachrichten, die zurückgestellt wurden. Hierzu muss der Adressbuchhierarchie die folgenden Eigenschaftswerte in der Statuszeile des Anmeldung-Objekts festgelegt:
    
   - Legen Sie die **PR_STATUS_STRING** -Eigenschaft auf eine Zeichenfolge, die der Adressbuchhierarchie Status für den Benutzer angibt. 
    
   - Legen Sie die STATUS_OUTBOUND_ENABLED und STATUS_OUTBOUND_ACTIVE Bits in der **PR_STATUS_CODE** -Eigenschaft. 
    
   - Legen Sie die **PR_REMOTE_VALIDATE_OK** -Eigenschaft in der Adressbuchhierarchie Statuszeile auf false festgelegt. 
    
   - Wenn ein anderer Vorgang in Arbeit (beispielsweise Kopfzeilen herunterladen) wird **ValidateState** aufgerufen wird, sollte **ValidateState** MAPI_E_BUSY zurückgegeben. 
    
   - Führen Sie den Code für die Verarbeitung der REFRESH_XP_HEADER_CACHE-Flag, um Anforderungen des Microsoft Exchange-Clients zu erfüllen.
    
REFRESH_XP_HEADER_CACHE 
  
> Der remote-Transport-Anbieter sollten alle neuen Nachrichtenkopfzeilen von messaging-System abrufen. Zu diesem Zweck muss der Adressbuchhierarchie Folgendes ausführen:
    
   - Legen Sie die **PR_STATUS_STRING** -Eigenschaft auf eine Zeichenfolge, die der Adressbuchhierarchie Status für den Benutzer angibt. 
    
   - Legen Sie die STATUS_INBOUND_ENABLED und STATUS_INBOUND_ACTIVE Bits in der **PR_STATUS_CODE** -Eigenschaft. 
    
   - Deaktivieren Sie das STATUS_OFFLINE bit in der **PR_STATUS_CODE** -Eigenschaft. 
    
   - Legen Sie die STATUS_ONLINE bit in der **PR_STATUS_CODE** -Eigenschaft. 
    
   - Legen Sie die **PR_REMOTE_VALIDATE_OK** -Eigenschaft in der Adressbuchhierarchie Statuszeile auf false festgelegt. 
    
SHOW_XP_SESSION_UI 
  
> Verfügt Ihre Adressbuchhierarchie alle Teile der Benutzeroberfläche für die Verarbeitung der Nachrichtenkopfzeilen (beispielsweise ein Dialogfeld, das bestätigt das Herunterladen von Nachrichten), sollte das Dialogfeld angezeigt. Andernfalls können **ValidateState** MAPI_E_NO_SUPPORT zurück. 
    
Wenn alle Flags als diese übergeben werden, sollte **ValidateState** MAPI_E_UNKNOWN_FLAGS zurückgegeben. 
  
Aufruf der Adressbuchhierarchie des Clients werden häufig an die **IMAPIStatus::ValidateState** -Methode. Während der Verarbeitung der **ValidateState**, sollte der Adressbuchhierarchie keine Aktionen ausführen, die anderen Komponenten um knappe Systemressourcen, wie ein Modem oder COM-Port zuweisen. Dies ist, da die MAPI-Warteschlange manchmal zum Leeren der Warteschlangen auf mehreren Adressbuchhierarchie benötigen. Der Client kann jedoch Adressbuchhierarchie **ValidateState** -Methode können Sie jederzeit aufrufen. Wenn Ihre Adressbuchhierarchie versucht, eine wertvolle Ressource während der Verarbeitung der **ValidateState**zugewiesen werden, kann ein Fehler aufgrund eines Konflikts mit einem anderen Adressbuchhierarchie führen, die die MAPI-Warteschlange angewiesen hat, um Warteschlangen zu leeren. Wenn Sie alle anderen Komponenten um knappe Ressourcen Zuweisungen unter die Richtung der die MAPI-Warteschlange erfolgt zulassen, können Sie solche Konflikte vermeiden. Der Transportdienst sollte die **PR_REMOTE_VALIDATE_OK** -Eigenschaft unterstützen, damit Clientanwendungen erkennen können, wenn Ihre Adressbuchhierarchie ausgelastet oder wartet die MAPI-Warteschlange zum Initiieren einer Aktion ist. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Da diese Methode anderen potenziell langen Aufrufe erfolgen auftreten kann, können **ValidateState** MAPI_E_BUSY zu informieren, wenn diese Methode auf den Abschluss einer anderen Operation wartet zurück. Warten Sie, bis der ausstehende Vorgang abgeschlossen ist, bevor Sie versuchen, einer anderen Aufgabe. 
  
Sie haben die größte Kontrolle über Ihre Anrufe transport-Anbieter Status Objekte. Sie können eine oder mehrere Flags an **ValidateState** , die der Adressbuchhierarchie Vorgänge betreffen übergeben. Das Flag ABORT_XP_HEADER_OPERATION gibt beispielsweise an, dass der Benutzer die Überprüfung abgebrochen. Transportanbieter können entscheiden, um den Vorgang abzubrechen, MAPI_E_USER_CANCELED, zurückgeben oder fortfahren können. 
  
Klicken Sie auf einen Anruf an das Statusobjekt einem Dienstanbieter oder die MAPI-Warteschlange, um anzugeben, dass eine Konfigurationsoption geändert wurde, können Sie die CONFIG_CHANGED-Flag festlegen. CONFIG_CHANGED können Sie dynamisch eine Transportdienst neu konfigurieren. Wenn Sie CONFIG_CHANGED auf einen Anruf an einem Dienstanbieter Status-Objekt festlegen, reagiert der Anbieter mit einem Aufruf von [IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md) zu warnen, die MAPI-Warteschlange der Änderung. Wenn Sie CONFIG_CHANGED auf einen Anruf an die MAPI-Warteschlange Status-Objekt festlegen, ruft die Warteschlange [IXPLogon::AddressTypes](ixplogon-addresstypes.md) für jeden Anbieter aktiven Transport. **AddressTypes** informiert die MAPI-Warteschlange von unterstützten Adresstypen einen Transport. Einige Dienstanbieter können auch eine Statusanzeige angezeigt, wenn die Überprüfung voraussichtlich dauert sehr lange. Eine Statusanzeige anzeigen ist hilfreich, aber nicht erforderlich. 
  
Wenn das Flag SUPPRESS_UI festgelegt ist, können keines der Eigenschaftenseiten Konfiguration oder Fortschritt Dialogfelder angezeigt werden. 
  
## <a name="see-also"></a>Siehe auch

- [IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md)
- [IXPLogon::AddressTypes](ixplogon-addresstypes.md)
- [IXPLogon::FlushQueues](ixplogon-flushqueues.md)
- [PidTagRemoteValidateOk (kanonische Eigenschaft)](pidtagremotevalidateok-canonical-property.md)
- [PidTagResourceMethods (kanonische Eigenschaft)](pidtagresourcemethods-canonical-property.md)
- [PidTagStatusCode (kanonische Eigenschaft)](pidtagstatuscode-canonical-property.md)
- [PidTagStatusString (kanonische Eigenschaft)](pidtagstatusstring-canonical-property.md)
- [IMAPIStatus : IMAPIProp](imapistatusimapiprop.md)

