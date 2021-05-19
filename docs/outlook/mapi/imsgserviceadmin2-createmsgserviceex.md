---
title: IMsgServiceAdmin2CreateMsgServiceEx
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMsgServiceAdmin2.CreateMsgServiceEx
api_type:
- COM
ms.assetid: 4910dabd-9380-4fde-a440-5c64d74c0bba
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: b7fe25491228f00f6865af963db36f27bae5d7a7
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410182"
---
# <a name="imsgserviceadmin2createmsgserviceex"></a>IMsgServiceAdmin2::CreateMsgServiceEx

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Fügt dem aktuellen Profil einen Nachrichtendienst hinzu und gibt die neu hinzugefügte Dienst-UID zurück.
  
```cpp
HRESULT CreateMsgServiceEx(
  LPSTR lpszService,
  LPSTR lpszDisplayName,
  ULONG_PTR ulUIParam,
  ULONG ulFlags,    
  LPMAPIUID lpuidService
);
```

## <a name="parameters"></a>Parameter

 _lpszService_
  
> [in] Ein Zeiger auf den Namen des hinzuzufügende Nachrichtendiensts. Dieser Nachrichtendienstname muss im **Abschnitt [Dienste]** der Datei MapiSvc.inf angezeigt werden. 
    
 _lpszDisplayName_
  
> [in] Ein Zeiger auf den Anzeigenamen des hinzuzufügende Nachrichtendiensts. Der  _lpszDisplayName-Parameter_ wird ignoriert, wenn der Nachrichtendienst die **eigenschaft PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) in der Datei MapiSvc.inf festgelegt hat.
    
 _ulUIParam_
  
> [in] Ein Handle zum übergeordneten Fenster aller Dialogfelder oder Fenster, die diese Methode anzeigt.
    
 _ulFlags_
  
> [in] Eine Bitmaske mit Flags, die steuert, wie der Nachrichtendienst installiert wird. Die folgenden Kennzeichen können festgelegt werden:
    
MAPI_UNICODE
  
> Die Parameter lpszService und lpszDisplayName sollten in LPWSTR umvertiert und als Unicode-Zeichenfolgen interpretiert werden.
    
SERVICE_NO_RESTART_WARNING
  
> Beim Hinzufügen eines neuen Nachrichtendiensts zum Profil bestimmt das MAPI-Subsystem basierend auf verschiedenen Umständen und Kriterien häufig, dass diese Aktion einen Neustart von Outlook erfordert. Wenn das SERVICE_NO_RESTART_WARNING-Flag nicht enthalten ist und die Benutzeroberfläche – basierend auf den SERVICE_UI_ALWAYS- und SERVICE_UI_ALLOWED-Flags – zulässig ist und mindestens ein Prozess am aktuellen Profil angemeldet ist, zeigt diese Funktion die Meldung "Sie müssen Outlook neu starten, damit diese Änderungen wirksam werden." Durch das SERVICE_NO_RESTART_WARNING wird die Anzeige dieser Warnmeldung unterdrückt.
    
SERVICE_UI_ALLOWED
  
> Die Benutzeroberfläche für die Nachrichtendienstkonfiguration ist bei Bedarf zulässig.
    
SERVICE_UI_ALWAYS
  
> Der Nachrichtendienst zeigt sein Konfigurationseigenschaftsblatt an.
    
 _lpuidService_
  
> [out] Der Zeiger auf die UID des hinzugefügten Nachrichtendiensts.
    
## <a name="return-value"></a>Rückgabewert

S_OK
  
> Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.
    
MAPI_E_NOT_FOUND
  
> Der Name des Nachrichtendiensts befindet sich nicht im **Abschnitt [Dienste]** von MapiSvc.inf. 
    
## <a name="remarks"></a>Hinweise

Die **IMsgServiceAdmin2::CreateMsgServiceEx-Methode** fügt dem aktuellen Profil einen Nachrichtendienst hinzu. **CreateMsgServiceEx** ruft die Einstiegspunktfunktion des Nachrichtendiensts auf, um dienstspezifische Konfigurationsaufgaben auszuführen. Wenn das SERVICE_UI_ALLOWED im  _ulFlags-Parameter_ festgelegt ist, kann der zu installierende Nachrichtendienst ein Eigenschaftenblatt anzeigen, mit dem der Benutzer seine Einstellungen konfigurieren kann. 
  
Die Datei MapiSvc.inf enthält die Liste der Anbieter, aus der ein Nachrichtendienst besteht, und die Jeweiligen Eigenschaften. **CreateMsgServiceEx** erstellt zunächst einen neuen Profilabschnitt für den Nachrichtendienst und kopiert dann alle Informationen für diesen Dienst aus der Datei MapiSvc.inf in das Profil, wodurch neue Abschnitte für jeden Anbieter erstellt werden. 
  
Nachdem alle Informationen aus MapiSvc.inf kopiert wurden, wird die Einstiegspunktfunktion des Nachrichtendiensts **MSGSERVICEENTRY** mit dem im  _ulContext-Parameter_ festgelegten MSG_SERVICE_CREATE aufgerufen. Wenn das SERVICE_UI_ALLOWED-Flag im _ulFlags-Parameter_ der **CreateMsgServiceEx-Methode** festgelegt ist, werden die Werte in den Parametern _ulUIParam_ und _ulFlags_ auch übergeben, wenn die Einstiegspunktfunktion des Nachrichtendiensts aufgerufen wird. Dienstanbieter sollten ihre Konfigurationseigenschaftsblätter anzeigen, damit Benutzer den Nachrichtendienst konfigurieren können. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Wenn das **Argument CreateMsgServiceEx** _lpuidService_ nicht NULL ist, wird die **PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md))-Eigenschaft des Nachrichtendiensts, der dem Profil hinzugefügt wurde, in der **GUID** zurückgegeben, auf die es verweist. 
  
Übergeben Sie den Wert der **PR_SERVICE_UID-Eigenschaft** im  _lpuidService-Parameter_ an die [IMsgServiceAdmin::ConfigureMsgService-Methode,](imsgserviceadmin-configuremsgservice.md) um den Dienst zu konfigurieren. 
  
> [!CAUTION]
> Die Microsoft Outlook 2010 des MAPI-Subsystems unterstützt keine MAPI_UNICODE und führt bei Verwendung zu einem Fehler. 
  
> [!IMPORTANT]
> Die IMsgServiceAdmin2-Schnittstelle wird von demselben Objekt verfügbar gemacht, das die IMsgServiceAdmin-Schnittstelle implementiert, und steht seit Outlook 2003 mithilfe der Implementierung des MAPI-Subsystems von Outlook zur Verfügung. Die IID ist wie folgt definiert: >> Die `#if !defined(INITGUID) || defined(USES_IID_IMsgServiceAdmin2)` >   `DEFINE_OLEGUID(IID_IMsgServiceAdmin2,0x00020387, 0, 0);` _ulFlags_ SERVICE_NO_RESTART_WARNING ist möglicherweise nicht in der herunterladbaren Headerdatei definiert, die Sie derzeit haben. In diesem Fall können Sie sie ihrem Code mithilfe des folgenden Werts hinzufügen: >`#define SERVICE_NO_RESTART_WARNING 0x00000080`
  
## <a name="see-also"></a>Siehe auch



[IMsgServiceAdmin2 : IMsgServiceAdmin](imsgserviceadmin2imsgserviceadmin.md)


[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)

