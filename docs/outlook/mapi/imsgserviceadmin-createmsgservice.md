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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 6e0bdd7108bacd17134592ac05ba71510fde76d8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792634"
---
# <a name="imsgserviceadmincreatemsgservice"></a>IMsgServiceAdmin::CreateMsgService

  
  
**Betrifft**: Outlook 
  
Veraltet: Die Verwendung von [IMsgServiceAdmin2::CreateMsgServiceEx](imsgserviceadmin2-createmsgserviceex.md) wird empfohlen. Fügt einen Nachrichtendienst zum aktuellen Profil hinzu. 
  
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
  
> [in] Ein Zeiger auf den Namen des Diensts Nachricht hinzufügen. Diese Meldung Dienstname muss in der die Datei "MapiSvc.inf" im Abschnitt **[Services]** angezeigt werden. 
    
 _lpszDisplayName_
  
> [in] Ein Zeiger auf den Anzeigenamen des Diensts Nachricht hinzufügen. Der Parameter _LpszDisplayName_ wird ignoriert, wenn der Message-Dienst die **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))-Eigenschaft in der Datei "MapiSvc.inf" festgelegt wurde.
    
 _ulUIParam_
  
> [in] Ein Handle für das übergeordnete Fenster des alle Dialogfelder oder Fenster zeigt diese Methode an.
    
 _ulFlags_
  
> [in] Eine Bitmaske aus Flags, die steuert, wie der Nachrichtendienst installiert ist. Die folgenden Kennzeichen können festgelegt werden:
    
PARAMETER MAPI_UNICODE
  
> Die LpszService und die LpszDisplayName-Parameter sollte in LPWSTR umgewandelt und als Unicode-Zeichenfolgen interpretiert werden.
    
SERVICE_NO_RESTART_WARNING
  
> Beim Hinzufügen eines neuen Nachricht-Diensts auf das Profil, bestimmt das MAPI-Subsystem, basierend auf verschiedenen Umständen und Kriterien, häufig, dass diese Aktion einen Neustart von Outlook erfordert. Wenn das Flag SERVICE_NO_RESTART_WARNING ist nicht mit inbegriffen und Benutzeroberfläche zulässig - basierend auf die Flags SERVICE_UI_ALWAYS und SERVICE_UI_ALLOWED - und mindestens einen Prozess das aktuelle Profil angemeldet ist, gibt diese Funktion die Nachricht "müssen Sie Outlook neu starten diese Änderungen wirksam werden." Das Flag SERVICE_NO_RESTART_WARNING einschließlich unterdrückt die Anzeige dieser Warnung Nachricht.
    
SERVICE_UI_ALLOWED
  
> Die Konfiguration des Dienstes ist Benutzeroberfläche zulässig, falls erforderlich.
    
SERVICE_UI_ALWAYS 
  
> Die Messagingdiensts zeigt das Eigenschaftenfenster Konfiguration.
    
## <a name="return-value"></a>R�ckgabewert

S_OK 
  
> Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.
    
MAPI_E_NOT_FOUND 
  
> Der Dienstname Nachricht ist nicht in der MapiSvc.inf im Abschnitt **[Services]** . 
    
## <a name="remarks"></a>Bemerkungen

Die **IMsgServiceAdmin:: CreateMsgService** -Methode wird das aktuelle Profil ein Messagingdiensts hinzugefügt. **CreateMsgService** Ruft die Messagingdiensts Eintrag Point-Funktion, um alle dienstspezifische Konfigurationsaufgaben ausführen. Wenn das Flag SERVICE_UI_ALLOWED im _UlFlags_ -Parameter festgelegt ist, kann der Message-Dienst installiert wird ein Eigenschaftenblatt zum Aktivieren des Benutzers so konfigurieren Sie ihre Einstellungen anzeigen. 
  
Die Datei "MapiSvc.inf" enthält die Liste der Anbieter, die eine Message Service und die Eigenschaften für jede bilden. **CreateMsgService** zuerst erstellt einen neuen Profilabschnitt für den Dienst und kopiert alle Informationen für den betreffenden Dienst aus der Datei "MapiSvc.inf" in das Profil neue Abschnitte für jeden Anbieter erstellen. 
  
Nachdem alle Informationen aus MapiSvc.inf kopiert wurde, wird die Messagingdiensts Eintrag Point-Funktion mit dem Wert MSG_SERVICE_CREATE im _UlContext_ -Parameter aufgerufen. Wenn das Flag SERVICE_UI_ALLOWED in die **CreateMsgService** -Methode _UlFlags_ Parameter festgelegt ist, werden die Werte in den _UlUIParam_ und _UlFlags_ auch übergeben, wenn die Messagingdiensts Eintrag Point-Funktion aufgerufen wird. Dienstanbieter sollte ihre Konfiguration Eigenschaftenseiten angezeigt werden, damit Benutzer den Nachrichtendienst konfigurieren zu können. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

 **CreateMsgService** gibt keine [MAPIUID](mapiuid.md) -Struktur für den Dienst zurück, das dem Profil hinzugefügt wurde. 
  
Verwenden Sie zum Abrufen der **MAPIUID** für den Nachrichtendienst erstellten die folgende Schritte aus: 
  
1. Rufen Sie die [IMsgServiceAdmin::GetMsgServiceTable](imsgserviceadmin-getmsgservicetable.md) -Methode, um die Nachricht Service Administration-Tabelle zu erhalten. 
    
2. Suchen Sie die Zeile, die den Dienst durch eine Einschränkung für die Tabelle, die die **PR_SERVICE_NAME** ([PidTagServiceName](pidtagservicename-canonical-property.md))-Eigenschaft mit dem Namen des Diensts Nachricht entspricht platzieren darstellt. 
    
3. Rufen Sie den Dienst **PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md))-Eigenschaft ab. 
    
4. Übergeben Sie den Wert der Eigenschaft **PR_SERVICE_UID** im _LpUid_ -Parameter an die [IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md) -Methode zum Konfigurieren des Diensts. 
    
> [!CAUTION]
> Die Microsoft Outlook 2010-Implementierung des MAPI-Subsystems unterstützt keine Parameter MAPI_UNICODE und schlägt fehl, wenn sie verwendet wird. 
  
> [!IMPORTANT]
> _UlFlags_ SERVICE_NO_RESTART_WARNING möglicherweise nicht in der herunterladbaren Headerdatei derzeit definiert werden, in diesem Fall können Sie es dem Code mit dem folgenden Wert hinzufügen: >`#define SERVICE_NO_RESTART_WARNING 0x00000080`
  
## <a name="mfcmapi-reference"></a>MFCMAPI (engl.) (engl.)

Beispielcode MFCMAPI (engl.) finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|MAPIProfileFunctions.cpp  <br/> |HrAddServiceToProfile  <br/> |MFCMAPI (engl.) verwendet die **IMsgServiceAdmin:: CreateMsgService** -Methode, um einen Dienst zu einem Profil hinzufügen.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[IMsgServiceAdmin : IUnknown](imsgserviceadminiunknown.md)


[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)

