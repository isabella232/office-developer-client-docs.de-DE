---
title: IMsgServiceAdminCreateMsgService
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMsgServiceAdmin.CreateMsgService
api_type:
- COM
ms.assetid: 0135f049-0311-45e5-9685-78597d599a4e
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 0b3d8327607db0546a4737cdddb3d913e54077eb
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59579873"
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
  
> [in] Ein Zeiger auf den Namen des hinzuzufügenden Nachrichtendiensts. Dieser Nachrichtendienstname muss im Abschnitt **[Dienste]** der Datei MapiSvc.inf angezeigt werden. 
    
 _lpszDisplayName_
  
> [in] Ein Zeiger auf den Anzeigenamen des hinzuzufügenden Nachrichtendiensts. Der  _Parameter lpszDisplayName_ wird ignoriert, wenn der Nachrichtendienst die **Eigenschaft PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) in der Datei MapiSvc.inf festgelegt hat.
    
 _ulUIParam_
  
> [in] Ein Handle für das übergeordnete Fenster aller Dialogfelder oder Fenster, die von dieser Methode angezeigt werden.
    
 _ulFlags_
  
> [in] Eine Bitmaske mit Flags, die steuert, wie der Nachrichtendienst installiert wird. Die folgenden Flags können festgelegt werden:
    
MAPI_UNICODE
  
> Die Parameter lpszService und lpszDisplayName sollten in LPWSTR umgewandelt und als Unicode-Zeichenfolgen interpretiert werden.
    
SERVICE_NO_RESTART_WARNING
  
> Beim Hinzufügen eines neuen Nachrichtendiensts zum Profil bestimmt das MAPI-Subsystem basierend auf verschiedenen Umständen und Kriterien häufig, dass für diese Aktion ein Neustart von Outlook erforderlich ist. Wenn das SERVICE_NO_RESTART_WARNING Flag nicht enthalten ist und die Benutzeroberfläche – basierend auf den Flags SERVICE_UI_ALWAYS und SERVICE_UI_ALLOWED – zulässig ist und mindestens ein Prozess am aktuellen Profil angemeldet ist, zeigt diese Funktion die Meldung an: "Sie müssen Outlook neu starten, damit diese Änderungen wirksam werden." Durch das Einschließen der SERVICE_NO_RESTART_WARNING-Kennzeichnung wird die Anzeige dieser Warnmeldung unterdrückt.
    
SERVICE_UI_ALLOWED
  
> Die Konfigurations-UI des Nachrichtendiensts ist bei Bedarf zulässig.
    
SERVICE_UI_ALWAYS 
  
> Der Nachrichtendienst zeigt das Konfigurationseigenschaftenblatt an.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.
    
MAPI_E_NOT_FOUND 
  
> Der Name des Nachrichtendiensts befindet sich nicht im Abschnitt **[Dienste]** von MapiSvc.inf. 
    
## <a name="remarks"></a>HinwBemerkungeneise

Die **IMsgServiceAdmin::CreateMsgService-Methode** fügt dem aktuellen Profil einen Nachrichtendienst hinzu. **CreateMsgService** ruft die Einstiegspunktfunktion des Nachrichtendiensts auf, um dienstspezifische Konfigurationsaufgaben auszuführen. Wenn das SERVICE_UI_ALLOWED Flag im  _ulFlags-Parameter_ festgelegt ist, kann der installierte Nachrichtendienst ein Eigenschaftenblatt anzeigen, damit der Benutzer seine Einstellungen konfigurieren kann. 
  
Die Datei MapiSvc.inf enthält die Liste der Anbieter, aus denen ein Nachrichtendienst besteht, sowie die Jeweiligen Eigenschaften. **CreateMsgService** erstellt zuerst einen neuen Profilabschnitt für den Nachrichtendienst und kopiert dann alle Informationen für diesen Dienst aus der Datei MapiSvc.inf in das Profil, wodurch neue Abschnitte für jeden Anbieter erstellt werden. 
  
Nachdem alle Informationen aus MapiSvc.inf kopiert wurden, wird die Einstiegspunktfunktion des Nachrichtendiensts mit dem im  _ulContext-Parameter_ festgelegten MSG_SERVICE_CREATE Wert aufgerufen. Wenn das flag SERVICE_UI_ALLOWED im _ulFlags-Parameter_ der **CreateMsgService-Methode** festgelegt ist, werden auch die Werte in den _Parametern ulUIParam_ und _ulFlags_ übergeben, wenn die Einstiegspunktfunktion des Nachrichtendiensts aufgerufen wird. Dienstanbieter sollten ihre Konfigurationseigenschaftenblätter anzeigen, damit Benutzer den Nachrichtendienst konfigurieren können. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

 **CreateMsgService** gibt nicht die [MAPIUID-Struktur](mapiuid.md) für den Nachrichtendienst zurück, der dem Profil hinzugefügt wurde. 
  
Gehen Sie folgendermaßen vor, um **die MAPIUID** für den erstellten Nachrichtendienst abzurufen: 
  
1. Rufen Sie die [IMsgServiceAdmin::GetMsgServiceTable-Methode](imsgserviceadmin-getmsgservicetable.md) auf, um die Verwaltungstabelle des Nachrichtendiensts abzurufen. 
    
2. Suchen Sie die Zeile, die den Nachrichtendienst darstellt, indem Sie eine Einschränkung für die Tabelle festlegen, die der **PR_SERVICE_NAME** ([PidTagServiceName](pidtagservicename-canonical-property.md)) -Eigenschaft mit dem Namen des Nachrichtendiensts entspricht. 
    
3. Rufen Sie die **eigenschaft PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)) des Diensts ab. 
    
4. Übergeben Sie den Wert der **PR_SERVICE_UID-Eigenschaft** im Parameter  _lpUid_ an die [IMsgServiceAdmin::ConfigureMsgService-Methode,](imsgserviceadmin-configuremsgservice.md) um den Dienst zu konfigurieren. 
    
> [!CAUTION]
> Die Microsoft Outlook 2010 Implementierung des MAPI-Subsystems unterstützt MAPI_UNICODE nicht und schlägt fehl, wenn sie verwendet wird. 
  
> [!IMPORTANT]
> Die  _ulFlags-SERVICE_NO_RESTART_WARNING_ ist möglicherweise nicht in der herunterladbaren Headerdatei definiert, die Sie derzeit haben. In diesem Fall können Sie sie Ihrem Code mit dem folgenden Wert hinzufügen: >  `#define SERVICE_NO_RESTART_WARNING 0x00000080`
  
## <a name="mfcmapi-reference"></a>MFCMAPI-Referenz

Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|MAPIProfileFunctions.cpp  <br/> |HrAddServiceToProfile  <br/> |MFCMAPI verwendet die **IMsgServiceAdmin::CreateMsgService-Methode,** um einem Profil einen Dienst hinzuzufügen.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[IMsgServiceAdmin : IUnknown](imsgserviceadminiunknown.md)


[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)

