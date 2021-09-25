---
title: MAPILogonEx
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPILogonEx
api_type:
- HeaderDef
ms.assetid: 98091e5b-1abd-4814-9c7a-583b420ee11d
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 1a37ad43414efc82cd2418fcaa848a354d116a62
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59556070"
---
# <a name="mapilogonex"></a>MAPILogonEx

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Protokolliert eine Clientanwendung bei einer Sitzung mit dem Messagingsystem. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapix.h  <br/> |
|Implementiert von:  <br/> |MAPI  <br/> |
|Aufgerufen von:  <br/> |Clientanwendungen  <br/> |
   
```cpp
HRESULT MAPILogonEx(
  ULONG_PTR ulUIParam,
  LPSTR lpszProfileName,
  LPSTR lpszPassword,
  FLAGS flFlags,
  LPMAPISESSION FAR * lppSession
);
```

## <a name="parameters"></a>Parameter

 _ulUIParam_
  
> [in] Handle to the window to which the logon dialog box is modal. Wenn während des Aufrufs kein Dialogfeld angezeigt wird, wird der  _ulUIParam-Parameter_ ignoriert. Dieser Parameter kann Null sein. 
    
 _lpszProfileName_
  
> [in] Zeiger auf eine Zeichenfolge, die den Namen des Profils enthält, das beim Anmelden des Benutzers verwendet werden soll. Diese Zeichenfolge ist auf 64 Zeichen beschränkt.
    
 _lpszPassword_
  
> [in] Zeiger auf eine Zeichenfolge, die das Kennwort des Profils enthält. Der  _lpszPassword-Parameter_ muss NULL sein. 
    
 _flFlags_
  
> [in] Bitmaske mit Flags, die zum Steuern der Anmeldung verwendet werden. Die folgenden Flags können festgelegt werden:
    
MAPI_ALLOW_OTHERS 
  
> Die freigegebene Sitzung sollte zurückgegeben werden, sodass spätere Clients die Sitzung ohne Benutzeranmeldeinformationen abrufen können. 
    
MAPI_BG_SESSION
  
> Melden Sie sich bei einer Sitzung an, und führen Sie alle Vorgänge im Hintergrund aus. Wenn ein Client die Verarbeitung in einem Hintergrundthread oder in einem separaten Prozess in einer Weise durchführen möchte, die für den Vordergrundthread unaufdringlich ist, sollte er im Allgemeinen mit dem MAPI_BG_SESSION Flag aufgerufen werden. Eine Clientanwendung wie ein Indizierungsmodul oder das Öffnen einer persönlichen Ordnerdatei (Personal Folders File, PST) für den Zugriff auf den Hintergrundtyp sind einige Beispiele für die Verwendung von MAPI_BG_SESSION. MAPILogonEx.
    
MAPI_EXPLICIT_PROFILE 
  
> Das Standardprofil sollte nicht verwendet werden, und der Benutzer muss ein Profil angeben. 
    
MAPI_EXTENDED 
  
> Melden Sie sich mit erweiterten Funktionen an. Dieses Kennzeichen sollte immer festgelegt werden.
    
MAPI_FORCE_DOWNLOAD 
  
> Es sollte versucht werden, alle Nachrichten des Benutzers herunterzuladen, bevor sie zurückgegeben werden. Wenn das MAPI_FORCE_DOWNLOAD Flag nicht festgelegt ist, können Nachrichten im Hintergrund heruntergeladen werden, nachdem der Aufruf von MAPILogonEx zurückgegeben wurde. 
    
MAPI_LOGON_UI 
  
> Es sollte ein Dialogfeld angezeigt werden, in dem der Benutzer bei Bedarf zur Eingabe von Anmeldeinformationen aufgefordert wird. Wenn das flag MAPI_LOGON_UI nicht festgelegt ist, zeigt der aufrufende Client kein Anmeldedialogfeld an und gibt einen Fehlerwert zurück, wenn der Benutzer nicht angemeldet ist.
    
MAPI_NEW_SESSION 
  
> Es sollte versucht werden, eine neue MAPI-Sitzung zu erstellen, anstatt die freigegebene Sitzung zu erwerben. Wenn das MAPI_NEW_SESSION Flag nicht festgelegt ist, verwendet MAPILogonEx eine vorhandene freigegebene Sitzung, auch wenn der  _Parameter lpszprofileName_ nicht NULL ist. 
    
MAPI_NO_MAIL 
  
> Die MAPI sollte den MAPI-Spooler nicht über das Vorhandensein der Sitzung informieren. Das Ergebnis ist, dass keine Nachrichten in der Sitzung gesendet oder empfangen werden können, außer über ein eng gekoppeltes Speicher- und Transportpaar. Ein aufrufender Client legt dieses Kennzeichen fest, wenn er als Agent fungiert, Konfigurationsarbeiten ausgeführt werden müssen oder wenn der Client die verfügbaren Nachrichtenspeicher durchbrochen. 
    
MAPI_NT_SERVICE 
  
> Der Aufrufer wird als Windows Dienst ausgeführt. Aufrufer, die nicht als Windows Dienst ausgeführt werden, sollten dieses Flag nicht festlegen. Aufrufer, die als Dienst ausgeführt werden, müssen dieses Flag festlegen. 
    
MAPI_SERVICE_UI_ALWAYS 
  
> MAPILogonEx sollte ein Konfigurationsdialogfeld für jeden Nachrichtendienst im Profil anzeigen. Die Dialogfelder werden angezeigt, nachdem das Profil ausgewählt wurde, aber bevor ein Nachrichtendienst angemeldet ist. Das allgemeine MAPI-Dialogfeld für die Anmeldung enthält auch ein Kontrollkästchen, in dem derselbe Vorgang angefordert wird. 
    
MAPI_TIMEOUT_SHORT 
  
> Die Anmeldung sollte fehlschlagen, wenn sie länger als einige Sekunden blockiert wird. 
    
MAPI_UNICODE 
  
> Die übergebenen Zeichenfolgen haben das Unicode-Format. Wenn das flag MAPI_UNICODE nicht festgelegt ist, haben die Zeichenfolgen das ANSI-Format. 
    
MAPI_USE_DEFAULT 
  
> Das Messaging-Subsystem sollte den Profilnamen des Standardprofils durch den  _Parameter lpszProfileName_ ersetzen. Das flag MAPI_EXPLICIT_PROFILE wird ignoriert, es sei  _denn, lpszProfileName_ ist NULL oder leer. 
    
 _lppSession_
  
> [out] Zeiger auf einen Zeiger auf die MAPI-Sitzungsschnittstelle.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Die Anmeldung war erfolgreich.
    
MAPI_E_LOGON_FAILED 
  
> Die Anmeldung war nicht erfolgreich, entweder weil mindestens einer der Parameter für MAPILogonEx ungültig war oder weil zu viele Sitzungen bereits geöffnet waren.
    
MAPI_E_TIMEOUT 
  
> MapI serialisiert alle Anmeldungen über einen Mutex. Dies wird zurückgegeben, wenn das MAPI_TIMEOUT_SHORT-Flag festgelegt wurde und ein anderer Thread den Mutex gedrückt hat. 
    
MAPI_E_USER_CANCEL 
  
> Der Benutzer hat den Vorgang abgebrochen, in der Regel durch Klicken auf die Schaltfläche **Abbrechen** in einem Dialogfeld. 
    
## <a name="remarks"></a>HinwBemerkungeneise

MAPI-Clientanwendungen rufen die MAPILogonEx-Funktion auf, um sich bei einer Sitzung mit dem Messagingsystem anzumelden. Alle Zeichenfolgen, die übergeben und an und von MAPI-Aufrufen zurückgegeben werden, werden mit NULL beendet und müssen in der aktuellen Zeichensatz- oder Codeseite des Betriebssystems des aufrufenden Clients oder Anbieters angegeben werden.
  
Der  _Parameter lpszProfileName_ wird ignoriert, wenn es eine vorhandene vorherige Sitzung gibt, die MapiLogonEx mit festgelegter MAPI_ALLOW_OTHERS Flag aufgerufen hat und wenn das Flag MAPI_NEW_SESSION nicht festgelegt ist. Wenn der  _Parameter lpszProfileName_ NULL ist oder auf eine leere Zeichenfolge zeigt und der  _parameter flFlags_ das flag MAPI_LOGON_UI enthält, generiert die MAPILogonEx-Funktion ein Anmeldedialogfeld mit einem leeren Feld für den Profilnamen. 
  
Bei der Anmeldung bei einem bestimmten Profil sollte ein Client zusätzlich zum Profilnamen das MAPI_NEW_SESSION-Flag an MAPILogonEx übergeben. Wenn ein anderer Client eine freigegebene Sitzung eingerichtet hat, indem er sich bei MAPI_ALLOW_OTHERS anmeldet, wird der Client bei der freigegebenen Sitzung anstelle des angeforderten Profils angemeldet. 
  
Das MAPI_EXPLICIT_PROFILE Flag bewirkt nicht, dass der Standardprofilname verwendet wird, wenn  _lpszProfileName_ NULL oder leer ist, es sei denn, das MAPI_USE_DEFAULT Flag ist ebenfalls vorhanden. 
  
Das flag MAPI_NO_MAIL hat mehrere Auswirkungen, die folgende Auswirkungen haben, wenn der MAPI-Spooler nicht verwendet wird:
  
- Während dieser Sitzung können keine Nachrichten vom MAPI-Spooler gesendet oder übermittelt werden. Nur eng gekoppelte Speicher- und Transportanbieter können Nachrichten senden und übermitteln. 
    
- Serverbasierte Speicher können weiterhin Nachrichten senden oder übermitteln. 
    
- Nachrichten, die von serverbasierten Speichern gesendet oder übermittelt werden, werden von keinem Hookanbieter verarbeitet. 
    
- Optionen pro Nachricht und Empfänger für Transporte sind nicht verfügbar. 
    
- Die Statustabelle enthält keine Einträge für Transportanbieter, und von Statusobjekten abhängige Transportfunktionen (z. B. Konfiguration) sind nicht verfügbar. 
    
- Die Zeile "Nachrichtenspooler" in der Statustabelle enthält den STATUS_FAILURE Wert. 
    
- Anstägige Anmeldungen sind zulässig, aber diese Anmeldungen führen nicht dazu, dass die vorherige Anmeldung Statusobjektaktualisierungen empfängt. 
    
Ein Dienst sollte sich immer mit dem flag MAPI_NO_MAIL anmelden. 
  
## <a name="mfcmapi-reference"></a>MFCMAPI-Referenz

Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|MAPIObjects.cpp  <br/> |CMapiObjects::MAPILogonEx  <br/> |MFCMAPI verwendet die MAPILogonEx-Methode, um sich bei der MAPI anzumelden.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[IMAPISession::GetMsgStoresTable](imapisession-getmsgstorestable.md)
  
[IMAPISession::OpenMsgStore](imapisession-openmsgstore.md)


[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)

