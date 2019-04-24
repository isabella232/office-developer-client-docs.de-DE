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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 9f2ec8f0ec00f7314982e9b112415f69901c358c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32346648"
---
# <a name="mapilogonex"></a>MAPILogonEx

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Protokolliert eine Clientanwendung für eine Sitzung mit dem Messagingsystem. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapix. h  <br/> |
|Implementiert von:  <br/> |MAPI  <br/> |
|Aufgerufen von:  <br/> |Client Anwendungen  <br/> |
   
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
  
> in Handle für das Fenster, in dem das Anmeldedialogfeld modal ist. Wenn während des Anrufs kein Dialogfeld angezeigt wird, wird der _ulUIParam_ -Parameter ignoriert. Dieser Parameter kann NULL sein. 
    
 _lpszProfileName_
  
> in Zeiger auf eine Zeichenfolge, die den Namen des Profils enthält, das bei der Anmeldung des Benutzers verwendet werden soll. Diese Zeichenfolge ist auf 64 Zeichen beschränkt.
    
 _lpszPassword_
  
> in Zeiger auf eine Zeichenfolge, die das Kennwort des Profils enthält. Der _lpszPassword_ -Parameter muss NULL sein. 
    
 _flFlags_
  
> in Bitmaske der Flags, die verwendet werden, um die Ausführung der Anmeldung zu steuern. Die folgenden Flags können festgelegt werden:
    
MAPI_ALLOW_OTHERS 
  
> Die freigegebene Sitzung sollte zurückgegeben werden, sodass spätere Clients die Sitzung ohne Angabe von Benutzeranmeldeinformationen abrufen können. 
    
MAPI_BG_SESSION
  
> Melden Sie sich bei einer Sitzung an, und führen Sie alle Vorgänge im Hintergrund aus. Wenn ein Client die Verarbeitung in einem Hintergrundthread oder in einem separaten Prozess auf eine Weise beabsichtigt, die unauffällig für den Vordergrundthread ist, sollte er im Allgemeinen mit dem MAPI_BG_SESSION-Flag aufgerufen werden. Eine Clientanwendung wie ein Indizierungsmodul oder das Öffnen einer PST-Datei (Personal Folders) für den Hintergrundtyp Zugriff sind einige Beispiele dafür, wo MAPI_BG_SESSION verwendet werden soll. MAPILogonEx.
    
MAPI_EXPLICIT_PROFILE 
  
> Das Standardprofil sollte nicht verwendet werden, und der Benutzer muss ein Profil angeben müssen. 
    
MAPI_EXTENDED 
  
> Melden Sie sich mit erweiterten Funktionen an. Dieses Flag sollte immer festgelegt werden.
    
MAPI_FORCE_DOWNLOAD 
  
> Es sollte versucht werden, alle Nachrichten des Benutzers herunterzuladen, bevor Sie zurückkehren. Wenn das MAPI_FORCE_DOWNLOAD-Flag nicht festgelegt ist, können Nachrichten im Hintergrund heruntergeladen werden, nachdem der Aufruf von MAPILogonEx zurückgegeben wird. 
    
MAPI_LOGON_UI 
  
> Es sollte ein Dialogfeld angezeigt werden, um den Benutzer bei Bedarf um Anmeldeinformationen zu informieren. Wenn das MAPI_LOGON_UI-Flag nicht festgelegt ist, zeigt der aufrufende Client kein Anmeldedialogfeld an und gibt einen Fehlerwert zurück, wenn der Benutzer nicht angemeldet ist.
    
MAPI_NEW_SESSION 
  
> Es sollte versucht werden, eine neue MAPI-Sitzung zu erstellen, anstatt die freigegebene Sitzung zu erwerben. Wenn das MAPI_NEW_SESSION-Flag nicht festgelegt ist, verwendet MAPILogonEx eine vorhandene freigegebene Sitzung, auch wenn der _lpszprofileName_ -Parameter nicht NULL ist. 
    
MAPI_NO_MAIL 
  
> MAPI sollte den MAPI-Spooler nicht über die Existenz der Sitzung informieren. Das Ergebnis ist, dass keine Nachrichten in der Sitzung gesendet oder empfangen werden können, mit Ausnahme eines eng gekoppelten Speicher-und Transport Paars. Ein aufrufende Client legt dieses Flag fest, wenn es als Agent fungiert, wenn Konfigurationsaufgaben ausgeführt werden müssen oder wenn der Client die verfügbaren Nachrichtenspeicher durchsucht. 
    
MAPI_NT_SERVICE 
  
> Der Anrufer wird als Windows-Dienst gestartet. Anrufer, die nicht als Windows-Dienst gestartet werden, sollten dieses Flag nicht festlegen; Aufrufer, die als Dienst gestartet werden, müssen dieses Flag festlegen. 
    
MAPI_SERVICE_UI_ALWAYS 
  
> MAPILogonEx sollte ein Konfigurationsdialogfeld für jeden Nachrichtendienst im Profil anzeigen. Die Dialogfelder werden angezeigt, nachdem das Profil ausgewählt wurde, aber bevor ein Nachrichtendienst angemeldet ist. Das allgemeine MAPI-Dialogfeld für die Anmeldung enthält auch ein Kontrollkästchen, das den gleichen Vorgang anfordert. 
    
MAPI_TIMEOUT_SHORT 
  
> Die Anmeldung sollte fehlschlagen, wenn Sie für mehr als ein paar Sekunden gesperrt ist. 
    
MAPI_UNICODE 
  
> Die übergebenen Zeichenfolgen sind im Unicode-Format. Wenn das MAPI_UNICODE-Flag nicht festgelegt ist, werden die Zeichenfolgen im ANSI-Format. 
    
MAPI_USE_DEFAULT 
  
> Das Messaging Subsystem sollte den Profilnamen des Standardprofils des _lpszProfileName_ -Parameters ersetzen. Das MAPI_EXPLICIT_PROFILE-Flag wird ignoriert, es sei denn, _lpszProfileName_ ist NULL oder leer. 
    
 _lppSession_
  
> Out Zeiger auf einen Zeiger auf die MAPI-Sitzungs Schnittstelle.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Die Anmeldung war erfolgreich.
    
MAPI_E_LOGON_FAILED 
  
> Die Anmeldung war erfolglos, da mindestens einer der Parameter für MAPILogonEx ungültig war oder weil zu viele Sitzungen bereits geöffnet waren.
    
MAPI_E_TIMEOUT 
  
> MAPI serialisiert alle Anmeldungen über einen Mutex. Dieser Wert wird zurückgegeben, wenn das MAPI_TIMEOUT_SHORT-Flag festgelegt wurde und ein anderer Thread den Mutex gehalten hat. 
    
MAPI_E_USER_CANCEL 
  
> Der Benutzer hat den Vorgang abgebrochen, indem er in einem Dialogfeld auf die Schaltfläche **Abbrechen** geklickt hat. 
    
## <a name="remarks"></a>Bemerkungen

MAPI-Clientanwendungen rufen die MAPILogonEx-Funktion auf, um sich bei einer Sitzung mit dem Messagingsystem anzumelden. Alle Zeichenfolgen, die übergeben und an und von MAPI-Aufrufen zurückgegeben werden, werden mit Null beendet und müssen im aktuellen Zeichensatz oder der Codepage des Betriebssystems des aufrufenden Clients oder Anbieters angegeben werden.
  
Der Parameter _lpszProfileName_ wird ignoriert, wenn eine frühere Sitzung mit dem Namen MapiLogonEx mit dem MAPI_ALLOW_OTHERS-Flag festgelegt ist und das Flag MAPI_NEW_SESSION nicht festgelegt ist. Wenn der _lpszProfileName_ -Parameter NULL ist oder auf eine leere Zeichenfolge verweist und der Parameter _flFlags_ das MAPI_LOGON_UI-Flag enthält, generiert die MAPILogonEx-Funktion ein Anmeldedialogfeld mit einem leeren Feld für den Profilnamen. 
  
Bei der Anmeldung an einem bestimmten Profil sollte ein Client das MAPI_NEW_SESSION-Flag zusätzlich zu dem Profilnamen an MAPILogonEx weitergeben. Wenn ein anderer Client eine freigegebene Sitzung durch Anmelden bei MAPI_ALLOW_OTHERS erstellt hat, wird der Client bei der freigegebenen Sitzung anstelle des angeforderten Profils angemeldet. 
  
Das MAPI_EXPLICIT_PROFILE-Flag bewirkt nicht, dass der Standardprofilname verwendet wird, wenn _LPSZPROFILENAME_ NULL oder leer ist, es sei denn, das MAPI_USE_DEFAULT-Flag ist ebenfalls vorhanden. 
  
Das MAPI_NO_MAIL-Flag weist mehrere Effekte auf, die Folgendes verursachen, wenn der MAPI-Spooler nicht verwendet wird:
  
- Während dieser Sitzung können keine Nachrichten vom MAPI-Spooler gesendet oder übermittelt werden. Nur eng gekoppelte Speicher-und Transportanbieter können Nachrichten senden und übermitteln. 
    
- Server basierte Speicher können weiterhin Nachrichten senden oder übermitteln. 
    
- Nachrichten, die von Server basierten Stores gesendet oder übermittelt werden, werden von keinem Hook-Anbieter verarbeitet. 
    
- Pro Nachricht und pro-Empfänger-Optionen für den Verkehr sind nicht verfügbar. 
    
- Die Statustabelle enthält keine Einträge für Transportanbieter, und alle Transportfunktionen, die von Statusobjekten (wie Konfiguration) abhängig sind, sind nicht verfügbar. 
    
- Die Zeile Nachrichtenwarteschlange in der Statustabelle enthält den STATUS_FAILURE-Wert. 
    
- Huckepack Anmeldungen sind zulässig, aber diese Anmeldungen führen nicht dazu, dass die vorherige Anmeldung Statusobjekt Aktualisierungen empfängt. 
    
Ein Dienst sollte sich immer mit dem MAPI_NO_MAIL-Flag anmelden. 
  
## <a name="mfcmapi-reference"></a>MFCMAPI-Referenz

Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|MAPIObjects. cpp  <br/> |CMapiObjects:: MAPILogonEx  <br/> |MFCMAPI verwendet die MAPILogonEx-Methode, um sich bei MAPI anzumelden.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[IMAPISession::GetMsgStoresTable](imapisession-getmsgstorestable.md)
  
[IMAPISession::OpenMsgStore](imapisession-openmsgstore.md)


[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)

