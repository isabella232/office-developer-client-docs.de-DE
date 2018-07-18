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
ms.openlocfilehash: 08782fe616fe260388cff8982dfbb09951453a00
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19793116"
---
# <a name="mapilogonex"></a>MAPILogonEx

  
  
**Betrifft**: Outlook 
  
Meldet eine Clientanwendung bei einer Sitzung mit der messaging-System. 
  
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
  
> [in] Handle für das Fenster, das Anmeldedialogfeld gebunden werden. Wenn kein Dialogfeld während des Anrufs angezeigt wird, wird der Parameter _UlUIParam_ ignoriert. Dieser Parameter kann 0 (null) sein. 
    
 _lpszProfileName_
  
> [in] Zeiger auf eine Zeichenfolge, die enthält den Namen des Profils beim Anmelden des Benutzers verwendet werden. Diese Zeichenfolge ist auf 64 Zeichen begrenzt.
    
 _lpszPassword_
  
> [in] Zeiger auf eine Zeichenfolge, die das Kennwort des Profils enthält. Der Parameter _LpszPassword_ muss NULL sein. 
    
 _flFlags_
  
> [in] Bitmaske aus Flags verwendet, um zu steuern, wie die Anmeldung ausgeführt wird. Die folgenden Kennzeichen können festgelegt werden:
    
MAPI_ALLOW_OTHERS 
  
> Die freigegebene Sitzung sollte zurückgegeben werden, wodurch höher Clients erhalten die Sitzung ohne Angabe von Anmeldeinformationen. 
    
MAPI_BG_SESSION
  
> Melden Sie sich bei einer Sitzung, und alle Vorgänge im Hintergrund ausgeführt. Im Allgemeinen Clientidentität will Verarbeitung in einem Hintergrundthread oder in einem gesonderten Prozess in einer Weise, die nicht störend auf den Vordergrundthread ist, muss sie mit dem MAPI_BG_SESSION-Flag aufrufen. Eine Clientanwendung wie indexing-Engine oder öffnen eine Persönliche Ordner Datei (PST) für den Hintergrund Typ Zugriff sind einige Beispiele für die Verwendung mit dem MAPI_BG_SESSION. MAPILogonEx.
    
MAPI_EXPLICIT_PROFILE 
  
> Das Standardprofil sollte nicht verwendet werden, und der Benutzer sollte erforderlich, um ein Profil angeben. 
    
MAPI_EXTENDED 
  
> Melden Sie sich mit erweiterten Funktionen. Dieses Kennzeichen sollte immer festgelegt werden.
    
MAPI_FORCE_DOWNLOAD 
  
> Es sollten Sie alle Nachrichten des Benutzers vor der Rückgabe herunterladen versucht werden. Wenn das Flag MAPI_FORCE_DOWNLOAD nicht festgelegt ist, können Nachrichten im Hintergrund heruntergeladen werden, nachdem der Anruf an MAPILogonEx zurückgegeben. 
    
MAPI_LOGON_UI 
  
> Ein Dialogfeld sollte angezeigt werden, um den Benutzer zur Anmeldeinformationen auffordern, falls erforderlich. Wenn das Flag MAPI_LOGON_UI nicht festgelegt ist, der aufrufende Client ein Anmeldedialogfeld wird nicht angezeigt und gibt einen Fehlerwert zurück, wenn der Benutzer nicht angemeldet ist.
    
MAPI_NEW_SESSION 
  
> Soll versucht werden, erstellen Sie eine neue MAPI-Sitzung anstelle die freigegebene Sitzung erwerben. Wenn das Flag MAPI_NEW_SESSION nicht festgelegt ist, verwendet MAPILogonEx eine vorhandene freigegebene Sitzung, selbst wenn der Parameter _LpszprofileName_ nicht NULL ist. 
    
MAPI_NO_MAIL 
  
> MAPI informiert sollte nicht die MAPI-Warteschlange des Vorhandenseins der Sitzung. Das Ergebnis ist, dass keine Nachrichten gesendet oder in der Sitzung außer über einen eng gekoppelten speichern und-Paar Transport empfangen werden können. Ein aufrufende Client wird dieses Flag, wenn es als ein Agent fungiert, wenn Sie Konfigurationsarbeit erledigt werden muss, oder wenn der Client den verfügbaren Nachrichtenspeicher durchsucht. 
    
MAPI_NT_SERVICE 
  
> Der Anrufer wird als Windows-Dienst ausgeführt. Anrufer, die wie ein Windows-Dienst nicht dieses Flag festlegen sollten nicht ausgeführt werden; Anrufer, die als Dienst ausgeführt werden, müssen dieses Flag festgelegt. 
    
MAPI_SERVICE_UI_ALWAYS 
  
> MAPILogonEx sollte ein Konfigurationsdialogfeld für jeden Nachrichtendienst im Profil angezeigt werden. Die Dialogfelder werden angezeigt, nachdem das Profil gewählt wurde, jedoch bevor eine beliebige Nachricht Service angemeldet ist. MAPI-Standarddialogfeld für die Anmeldung enthält auch ein Kontrollkästchen, die den gleichen Vorgang anfordert. 
    
MAPI_TIMEOUT_SHORT 
  
> Wenn für mehr als ein paar Sekunden blockiert, sollte die Anmeldung fehlschlagen. 
    
PARAMETER MAPI_UNICODE 
  
> Die übergebenen Zeichenfolgen sind im Unicode-Format. Wenn die Option MAPI_UNICODE nicht festgelegt ist, sind die Zeichenfolgen in ANSI-Format. 
    
MAPI_USE_DEFAULT 
  
> Das messaging Subsystem sollten den Profilnamen des Standardprofils für den Parameter _LpszProfileName_ ersetzen. Das Flag MAPI_EXPLICIT_PROFILE wird ignoriert, es sei denn, _LpszProfileName_ NULL oder leer ist. 
    
 _lppSession_
  
> [out] Zeiger auf einen Zeiger auf die MAPI-Sitzung-Schnittstelle.
    
## <a name="return-value"></a>R�ckgabewert

S_OK 
  
> Die Anmeldung war erfolgreich.
    
MAPI_E_LOGON_FAILED 
  
> Die Anmeldung ist fehlgeschlagen, da eine oder mehrere der Parameter MAPILogonEx ungültig waren oder bereits zu viele Sitzungen geöffnet waren.
    
MAPI_E_TIMEOUT 
  
> MAPI serialisiert alle Anmeldungen über einen Mutex. Dies wird zurückgegeben, wenn das Flag MAPI_TIMEOUT_SHORT festgelegt wurde, und ein anderer Thread den Mutex frei. 
    
MAPI_E_USER_CANCEL 
  
> Der Benutzer hat den Vorgang in der Regel durch Klicken auf die Schaltfläche " **Abbrechen** " in einem Dialogfeld abgebrochen. 
    
## <a name="remarks"></a>Bemerkungen

MAPI-Clientanwendungen rufen Sie die Funktion MAPILogonEx zur Anmeldung bei einer Sitzung mit der messaging-System. Alle Zeichenfolgen, die übergeben und zurückgegeben, zu und von MAPI-Aufrufe Null endende werden und müssen in der aktuellen Zeichensatz angegeben werden oder Codepage des aufrufenden Client oder Anbieter des Betriebssystems.
  
Der Parameter _LpszProfileName_ wird ignoriert, wenn eine vorhandene vorherige Sitzung, die mit dem MAPI_ALLOW_OTHERS-Flag MapiLogonEx aufgerufen vorhanden ist und das Flag MAPI_NEW_SESSION nicht festgelegt ist. Wenn der Parameter _LpszProfileName_ NULL ist oder verweist auf eine leere Zeichenfolge und der Parameter _FlFlags_ umfasst das MAPI_LOGON_UI-Flag, generiert die MAPILogonEx-Funktion ein Anmeldedialogfeld, die ein leeres Feld für den Namen des Profils verfügt. 
  
Bei der Anmeldung an einem bestimmten Profil sollte ein Client das Flag MAPI_NEW_SESSION in MAPILogonEx zusätzlich zu den Profilnamen übergeben. Andernfalls, wenn ein anderer Client eine freigegebene Sitzung anmelden, auf mit MAPI_ALLOW_OTHERS hergestellt, wird der Client an der freigegebenen Sitzung anstatt auf das Profil angefordert angemeldet sein. 
  
Das Flag MAPI_EXPLICIT_PROFILE nicht dazu führen, dass der Name verwendet werden, wenn _LpszProfileName_ NULL ist oder leer, wenn das Flag MAPI_USE_DEFAULT auch vorhanden ist. 
  
Das Flag MAPI_NO_MAIL hat mehrere Effekte, die die folgenden verursachen, wenn die Warteschlange MAPI nicht verwenden:
  
- Keine Nachrichten können gesendet oder durch die MAPI-Warteschlange diese Sitzung bereitgestellt werden. Nur eng gekoppelten Store und Transport-Provider können senden und Nachrichten übermitteln. 
    
- Serverbasierte Speicher möglicherweise noch senden oder Nachrichten übermitteln. 
    
- Nachrichten gesendet oder von Server-basierte Speicher bereitgestellt werden von Anbietern Hook nicht verarbeitet. 
    
- Optionen für einzelne Nachrichten und pro Empfänger für Transporten sind nicht verfügbar. 
    
- Die Statustabelle enthält keine Einträge für Transportanbieter für, und alle Transport-Funktionalität abhängig vom Status-Objekte (Konfiguration) ist nicht verfügbar. 
    
- Die Nachricht Warteschlange Zeile in der Tabelle "Status" enthält den STATUS_FAILURE-Wert. 
    
- Anmeldungen Benachtichtigung sind zulässig, aber diese Anmeldungen führen nicht die vorherige Anmeldung Statusupdates-Objekt zu erhalten. 
    
Ein Dienst sollte immer melden Sie sich mit dem MAPI_NO_MAIL-Flag. 
  
## <a name="mfcmapi-reference"></a>MFCMAPI (engl.) (engl.)

Beispielcode MFCMAPI (engl.) finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|MAPIObjects.cpp  <br/> |CMapiObjects::MAPILogonEx  <br/> |MFCMAPI (engl.) verwendet die MAPILogonEx-Methode zur Anmeldung bei MAPI an.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[IMAPISession::GetMsgStoresTable](imapisession-getmsgstorestable.md)
  
[IMAPISession::OpenMsgStore](imapisession-openmsgstore.md)


[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)

