---
title: IMsgServiceAdminCreateMsgService
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMsgServiceAdmin.CreateMsgService
api_type:
- COM
ms.assetid: 0135f049-0311-45e5-9685-78597d599a4e
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: e7d30c1aba8ddc1419045c1caa8524f7d2063dc5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434977"
---
# <a name="imsgserviceadmincreatemsgservice"></a>IMsgServiceAdmin::CreateMsgService

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Veraltet: Die Verwendung von [IMsgServiceAdmin2::CreateMsgServiceEx](imsgserviceadmin2-createmsgserviceex.md) wird empfohlen. Fügt dem aktuellen Profil einen Nachrichtendienst hinzu. 
  
```cpp
HRESULT CreateMsgService(
  LPSTR lpszService,
  LPSTR lpszDisplayName,
  ULONG_PTR ulUIParam,
  ULONG ulFlags    
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
  
> Beim Hinzufügen eines neuen Nachrichtendiensts zum Profil bestimmt das MAPI-Subsystem basierend auf verschiedenen Umständen und Kriterien häufig, dass für diese Aktion ein Neustart der Outlook. Wenn das SERVICE_NO_RESTART_WARNING-Flag nicht enthalten ist und die Benutzeroberfläche – basierend auf den SERVICE_UI_ALWAYS- und SERVICE_UI_ALLOWED-Flags – zulässig ist und mindestens ein Prozess am aktuellen Profil angemeldet ist, zeigt diese Funktion die Meldung "Sie müssen Outlook neu starten, damit diese Änderungen wirksam werden." Durch das SERVICE_NO_RESTART_WARNING wird die Anzeige dieser Warnmeldung unterdrückt.
    
SERVICE_UI_ALLOWED
  
> Die Benutzeroberfläche für die Nachrichtendienstkonfiguration ist bei Bedarf zulässig.
    
SERVICE_UI_ALWAYS 
  
> Der Nachrichtendienst zeigt sein Konfigurationseigenschaftsblatt an.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.
    
MAPI_E_NOT_FOUND 
  
> Der Name des Nachrichtendiensts befindet sich nicht im **Abschnitt [Dienste]** von MapiSvc.inf. 
    
## <a name="remarks"></a>Hinweise

Die **IMsgServiceAdmin::CreateMsgService-Methode** fügt dem aktuellen Profil einen Nachrichtendienst hinzu. **CreateMsgService ruft** die Einstiegspunktfunktion des Nachrichtendiensts auf, um dienstspezifische Konfigurationsaufgaben auszuführen. Wenn das SERVICE_UI_ALLOWED im  _ulFlags-Parameter_ festgelegt ist, kann der zu installierende Nachrichtendienst ein Eigenschaftenblatt anzeigen, damit der Benutzer seine Einstellungen konfigurieren kann. 
  
Die Datei MapiSvc.inf enthält die Liste der Anbieter, aus der ein Nachrichtendienst besteht, und die Jeweiligen Eigenschaften. **CreateMsgService** erstellt zunächst einen neuen Profilabschnitt für den Nachrichtendienst und kopiert dann alle Informationen für diesen Dienst aus der Datei MapiSvc.inf in das Profil, wodurch neue Abschnitte für jeden Anbieter erstellt werden. 
  
Nachdem alle Informationen aus MapiSvc.inf kopiert wurden, wird die Einstiegspunktfunktion des Nachrichtendiensts mit dem wert MSG_SERVICE_CREATE im  _ulContext-Parameter_ aufgerufen. Wenn das SERVICE_UI_ALLOWED im _ulFlags-Parameter_ der **CreateMsgService-Methode** festgelegt ist, werden die Werte in den Parametern _ulUIParam_ und _ulFlags_ auch übergeben, wenn die Einstiegspunktfunktion des Nachrichtendiensts aufgerufen wird. Dienstanbieter sollten ihre Konfigurationseigenschaftsblätter anzeigen, damit Benutzer den Nachrichtendienst konfigurieren können. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

 **CreateMsgService** gibt die [MAPIUID-Struktur](mapiuid.md) für den Nachrichtendienst, der dem Profil hinzugefügt wurde, nicht zurück. 
  
Verwenden Sie das folgende Verfahren, um die **MAPIUID** für den erstellten Nachrichtendienst abzurufen: 
  
1. Rufen Sie [die IMsgServiceAdmin::GetMsgServiceTable-Methode](imsgserviceadmin-getmsgservicetable.md) auf, um die Nachrichtendienstverwaltungstabelle zu erhalten. 
    
2. Suchen Sie die Zeile, die den Nachrichtendienst darstellt, indem Sie eine Einschränkung für die Tabelle **setzen,** die der PR_SERVICE_NAME ([PidTagServiceName](pidtagservicename-canonical-property.md)) -Eigenschaft mit dem Namen des Nachrichtendiensts entspricht. 
    
3. Rufen Sie die **PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)) -Eigenschaft des Diensts ab. 
    
4. Übergeben Sie den Wert der **PR_SERVICE_UID-Eigenschaft** im  _lpUid-Parameter_ an die [IMsgServiceAdmin::ConfigureMsgService-Methode,](imsgserviceadmin-configuremsgservice.md) um den Dienst zu konfigurieren. 
    
> [!CAUTION]
> Die Microsoft Outlook 2010 des MAPI-Subsystems unterstützt keine MAPI_UNICODE und führt bei Verwendung zu einem Fehler. 
  
> [!IMPORTANT]
> Die  _ulFlags SERVICE_NO_RESTART_WARNING-Datei_ ist möglicherweise nicht in der herunterladbaren Headerdatei definiert, die Sie derzeit haben. In diesem Fall können Sie sie ihrem Code mithilfe des folgenden Werts hinzufügen: >  `#define SERVICE_NO_RESTART_WARNING 0x00000080`
  
## <a name="mfcmapi-reference"></a>MFCMAPI-Referenz

Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|MAPIProfileFunctions.cpp  <br/> |HrAddServiceToProfile  <br/> |MFCMAPI verwendet die **IMsgServiceAdmin::CreateMsgService-Methode,** um einem Profil einen Dienst hinzuzufügen.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[IMsgServiceAdmin : IUnknown](imsgserviceadminiunknown.md)


[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)

