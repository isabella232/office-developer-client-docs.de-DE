---
title: MAPILogonEx
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPILogonEx
api_type:
- HeaderDef
ms.assetid: 98091e5b-1abd-4814-9c7a-583b420ee11d
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 9f2ec8f0ec00f7314982e9b112415f69901c358c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424119"
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
  
> [in] Behandeln Sie das Fenster, in das das Anmeldedialogfeld modal ist. Wenn während des Aufrufs kein Dialogfeld angezeigt wird, wird der  _ulUIParam-Parameter_ ignoriert. Dieser Parameter kann null sein. 
    
 _lpszProfileName_
  
> [in] Zeiger auf eine Zeichenfolge, die den Namen des Profils enthält, das verwendet werden soll, wenn sich der Benutzer anmeldet. Diese Zeichenfolge ist auf 64 Zeichen beschränkt.
    
 _lpszPassword_
  
> [in] Zeiger auf eine Zeichenfolge, die das Kennwort des Profils enthält. Der  _lpszPassword-Parameter_ muss NULL sein. 
    
 _flFlags_
  
> [in] Bitmaske von Flags, die verwendet werden, um zu steuern, wie die Anmeldung ausgeführt wird. Die folgenden Kennzeichen können festgelegt werden:
    
MAPI_ALLOW_OTHERS 
  
> Die freigegebene Sitzung sollte zurückgegeben werden, wodurch spätere Clients die Sitzung ohne Angabe von Benutzeranmeldeinformationen abrufen können. 
    
MAPI_BG_SESSION
  
> Melden Sie sich bei einer Sitzung an, und führen Sie alle Vorgänge im Hintergrund aus. Im Allgemeinen sollte ein Client, wenn er beabsichtigt, die Verarbeitung in einem Hintergrundthread oder in einem separaten Prozess auf eine Weise durchzuführen, die unauffällig für den Vordergrundthread ist, mit dem MAPI_BG_SESSION aufrufen. Eine Clientanwendung wie ein Indizierungsmodul oder das Öffnen einer Persönlichen Ordnerdatei (Pst) für den Hintergrundtypzugriff sind einige Beispiele für die Verwendung von MAPI_BG_SESSION. MAPILogonEx.
    
MAPI_EXPLICIT_PROFILE 
  
> Das Standardprofil sollte nicht verwendet werden, und der Benutzer sollte zur Bereitstellung eines Profils verpflichtet sein. 
    
MAPI_EXTENDED 
  
> Melden Sie sich mit erweiterten Funktionen an. Dieses Flag sollte immer festgelegt werden.
    
MAPI_FORCE_DOWNLOAD 
  
> Es sollte versucht werden, alle Nachrichten des Benutzers herunterzuladen, bevor sie zurückkehren. Wenn das MAPI_FORCE_DOWNLOAD nicht festgelegt ist, können Nachrichten im Hintergrund heruntergeladen werden, nachdem der Aufruf von MAPILogonEx zurückgegeben wurde. 
    
MAPI_LOGON_UI 
  
> Es sollte ein Dialogfeld angezeigt werden, in dem der Benutzer bei Bedarf zur Eingabe von Anmeldeinformationen aufgefordert wird. Wenn das MAPI_LOGON_UI nicht festgelegt ist, zeigt der aufrufende Client kein Anmeldedialogfeld an und gibt einen Fehlerwert zurück, wenn der Benutzer nicht angemeldet ist.
    
MAPI_NEW_SESSION 
  
> Es sollte versucht werden, eine neue MAPI-Sitzung zu erstellen, anstatt die freigegebene Sitzung zu erwerben. Wenn das MAPI_NEW_SESSION nicht festgelegt ist, verwendet MAPILogonEx eine vorhandene freigegebene Sitzung, auch wenn der  _lpszprofileName-Parameter_ nicht NULL ist. 
    
MAPI_NO_MAIL 
  
> MAPI sollte den MAPI-Spooler nicht über das Vorhandensein der Sitzung informieren. Das Ergebnis ist, dass keine Nachrichten in der Sitzung gesendet oder empfangen werden können, außer über ein eng gekoppeltes Speicher- und Transportpaar. Ein aufrufender Client legt dieses Flag fest, wenn er als Agent agiert, wenn Konfigurationsarbeiten ausgeführt werden müssen oder wenn der Client die verfügbaren Nachrichtenspeicher durchstöbert. 
    
MAPI_NT_SERVICE 
  
> Der Anrufer wird als Dienst Windows ausgeführt. Anrufer, die nicht als Dienst Windows, sollten dieses Flag nicht festlegen. Anrufer, die als Dienst ausgeführt werden, müssen dieses Flag festlegen. 
    
MAPI_SERVICE_UI_ALWAYS 
  
> MAPILogonEx sollte ein Konfigurationsdialogfeld für jeden Nachrichtendienst im Profil anzeigen. Die Dialogfelder werden angezeigt, nachdem das Profil ausgewählt wurde, aber bevor ein Nachrichtendienst angemeldet ist. Das allgemeine Dialogfeld MAPI für die Anmeldung enthält auch ein Kontrollkästchen, das denselben Vorgang anfordert. 
    
MAPI_TIMEOUT_SHORT 
  
> Die Anmeldung sollte fehlschlagen, wenn sie länger als ein paar Sekunden blockiert wird. 
    
MAPI_UNICODE 
  
> Die übergebenen Zeichenfolgen sind im Unicode-Format. Wenn das MAPI_UNICODE nicht festgelegt ist, befinden sich die Zeichenfolgen im ANSI-Format. 
    
MAPI_USE_DEFAULT 
  
> Das Messagingsubsystem sollte den Profilnamen des Standardprofils durch den  _lpszProfileName-Parameter_ ersetzen. Das MAPI_EXPLICIT_PROFILE wird ignoriert, es sei  _denn, lpszProfileName_ ist NULL oder leer. 
    
 _lppSession_
  
> [out] Zeiger auf einen Zeiger auf die MAPI-Sitzungsschnittstelle.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Die Anmeldung war erfolgreich.
    
MAPI_E_LOGON_FAILED 
  
> Die Anmeldung war nicht erfolgreich, weil einer oder mehrere Parameter für MAPILogonEx ungültig waren oder weil bereits zu viele Sitzungen geöffnet waren.
    
MAPI_E_TIMEOUT 
  
> MAPI serialisiert alle Anmeldungen über ein Mutex. Dies wird zurückgegeben, wenn das MAPI_TIMEOUT_SHORT festgelegt wurde und ein anderer Thread den Mutex gehalten hat. 
    
MAPI_E_USER_CANCEL 
  
> Der Benutzer hat den Vorgang abgebrochen, in der Regel durch Klicken auf die **Schaltfläche** Abbrechen in einem Dialogfeld. 
    
## <a name="remarks"></a>Hinweise

MAPI-Clientanwendungen rufen die MAPILogonEx-Funktion auf, um sich bei einer Sitzung mit dem Messagingsystem zu anmelden. Alle Zeichenfolgen, die an und von MAPI-Aufrufen übergeben und von diesen zurückgegeben werden, sind null-terminated und müssen im aktuellen Zeichensatz oder der Codeseite des Betriebssystems des aufrufenden Clients oder Anbieters angegeben werden.
  
Der  _lpszProfileName-Parameter_ wird ignoriert, wenn es eine vorhandene vorherige Sitzung mit dem Namen MapiLogonEx mit dem MAPI_ALLOW_OTHERS-Flag gibt und das Flag MAPI_NEW_SESSION nicht festgelegt ist. Wenn der  _lpszProfileName-Parameter_ NULL ist oder auf eine leere Zeichenfolge verweist und der  _flFlags-Parameter_ das MAPI_LOGON_UI-Flag enthält, generiert die MAPILogonEx-Funktion ein Anmeldedialogfeld mit einem leeren Feld für den Profilnamen. 
  
Bei der Anmeldung bei einem bestimmten Profil sollte ein Client das MAPI_NEW_SESSION zusätzlich zum Profilnamen an MAPILogonEx übergeben. Andernfalls wird der Client bei der freigegebenen Sitzung anstelle des angeforderten Profils angemeldet, wenn ein anderer Client eine freigegebene Sitzung durch die Anmeldung bei MAPI_ALLOW_OTHERS eingerichtet hat. 
  
Das MAPI_EXPLICIT_PROFILE führt nicht dazu, dass der Standardprofilname verwendet wird, wenn  _lpszProfileName_ NULL oder leer ist, es sei denn, das MAPI_USE_DEFAULT-Flag ist ebenfalls vorhanden. 
  
Das MAPI_NO_MAIL hat mehrere Effekte, die Folgendes verursachen, wenn der MAPI-Spooler nicht verwendet wird:
  
- Während dieser Sitzung können keine Nachrichten vom MAPI-Spooler gesendet oder zugestellt werden. Nur eng gekoppelte Speicher- und Transportanbieter können Nachrichten senden und senden. 
    
- Serverbasierte Speicher senden oder senden möglicherweise weiterhin Nachrichten. 
    
- Nachrichten, die von serverbasierten Speichern gesendet oder zugestellt werden, werden von keinem Hookanbieter verarbeitet. 
    
- Optionen pro Nachricht und Empfänger für Transporte sind nicht verfügbar. 
    
- Die Statustabelle enthält keine Einträge für Transportanbieter, und von Statusobjekten (z. B. Konfiguration) abhängige Transportfunktionen sind nicht verfügbar. 
    
- Die Zeile "Nachrichtenspooler" in der Statustabelle enthält den STATUS_FAILURE Wert. 
    
- Schweinchen-Anmeldungen sind zulässig, aber diese Anmeldungen führen nicht dazu, dass die vorherige Anmeldung Statusobjektaktualisierungen erhält. 
    
Ein Dienst sollte sich immer mit dem MAPI_NO_MAIL anmelden. 
  
## <a name="mfcmapi-reference"></a>MFCMAPI-Referenz

Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|MAPIObjects.cpp  <br/> |CMapiObjects::MAPILogonEx  <br/> |MFCMAPI verwendet die MAPILogonEx-Methode, um sich bei MAPI zu anmelden.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[IMAPISession::GetMsgStoresTable](imapisession-getmsgstorestable.md)
  
[IMAPISession::OpenMsgStore](imapisession-openmsgstore.md)


[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)

