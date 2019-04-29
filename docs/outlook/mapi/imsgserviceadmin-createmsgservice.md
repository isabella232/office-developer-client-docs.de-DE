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
  
Veraltet: die Verwendung von [IMsgServiceAdmin2:: CreateMsgServiceEx](imsgserviceadmin2-createmsgserviceex.md) wird empfohlen. Fügt dem aktuellen Profil einen Nachrichtendienst hinzu. 
  
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
  
> in Ein Zeiger auf den Namen des hinzuzufügenden Nachrichtendiensts. Dieser Nachrichtendienst Name muss im Abschnitt **[Dienste]** der Datei MapiSvc. inf angezeigt werden. 
    
 _lpszDisplayName_
  
> in Ein Zeiger auf den Anzeigenamen des hinzuzufügenden Nachrichtendiensts. Der Parameter _lpszDisplayName_ wird ignoriert, wenn der Nachrichtendienst die **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))-Eigenschaft in der Datei MapiSvc. inf festgelegt hat.
    
 _ulUIParam_
  
> in Ein Handle für das übergeordnete Fenster aller Dialogfelder oder Fenster, die diese Methode anzeigt.
    
 _ulFlags_
  
> in Eine Bitmaske von Flags, die die Installation des Nachrichtendiensts steuert. Die folgenden Flags können festgelegt werden:
    
MAPI_UNICODE
  
> Die Parameter lpszService und lpszDisplayName sollten in LPWSTR umgewandelt und als Unicode-Zeichenfolgen interpretiert werden.
    
SERVICE_NO_RESTART_WARNING
  
> Beim Hinzufügen eines neuen Nachrichtendiensts zum Profil bestimmt das MAPI-Subsystem, basierend auf verschiedenen Umständen und Kriterien, häufig, dass diese Aktion einen Neustart von Outlook erfordert. Wenn das SERVICE_NO_RESTART_WARNING-Flag nicht enthalten ist und die Benutzeroberfläche basierend auf den SERVICE_UI_ALWAYS-und SERVICE_UI_ALLOWED-Flags zulässig ist und mindestens ein Prozess am aktuellen Profil angemeldet ist, zeigt diese Funktion die Meldung "Sie müssen Outlook neu starten für Diese Änderungen werden wirksam. " Mit dem SERVICE_NO_RESTART_WARNING-Flag wird die Anzeige der Warnmeldung unterdrückt.
    
SERVICE_UI_ALLOWED
  
> Die Benutzeroberfläche der Nachrichtendienst Konfiguration ist bei Bedarf zulässig.
    
SERVICE_UI_ALWAYS 
  
> Der Nachrichtendienst zeigt das zugehörige Konfigurationseigenschaften Fenster an.
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.
    
MAPI_E_NOT_FOUND 
  
> Der Name des Nachrichtendiensts befindet sich nicht im Abschnitt **[Dienste]** von MapiSvc. inf. 
    
## <a name="remarks"></a>Bemerkungen

Mit der **IMsgServiceAdmin:: CreateMsgService** -Methode wird dem aktuellen Profil ein Nachrichtendienst hinzugefügt. **CreateMsgService** Ruft die Einstiegspunktfunktion des Nachrichtendiensts auf, um dienstspezifische Konfigurationsaufgaben auszuführen. Wenn das SERVICE_UI_ALLOWED-Flag im Parameter _ulFlags_ festgelegt ist, kann der installierte Nachrichtendienst ein Eigenschaftenfenster anzeigen, um dem Benutzer die Konfiguration seiner Einstellungen zu ermöglichen. 
  
Die Datei MapiSvc. inf enthält die Liste der Anbieter, aus denen sich ein Nachrichtendienst zusammensetzen, und die jeweiligen Eigenschaften. **CreateMsgService** erstellt zunächst einen neuen Profil Abschnitt für den Nachrichtendienst und kopiert dann alle Informationen für diesen Dienst aus der Datei MapiSvc. inf in das Profil, sodass für jeden Anbieter neue Abschnitte erstellt werden. 
  
Nachdem alle Informationen aus MapiSvc. inf kopiert wurden, wird die Einstiegspunktfunktion des Nachrichtendiensts aufgerufen, wobei der MSG_SERVICE_CREATE-Wert im _ulContext_ -Parameter festgelegt ist. Wenn das SERVICE_UI_ALLOWED-Flag im _ulFlags_ -Parameter der **CreateMsgService** -Methode festgelegt ist, werden die Werte in den Parametern _ulUIParam_ und _ulFlags_ auch übergeben, wenn die Einstiegspunktfunktion des Nachrichtendiensts aufgerufen wird. Dienstanbieter sollten Ihre Konfigurationseigenschaften Blätter anzeigen, damit Benutzer den Nachrichtendienst konfigurieren können. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

 **CreateMsgService** gibt nicht die [MAPIUID](mapiuid.md) -Struktur für den Nachrichtendienst zurück, der dem Profil hinzugefügt wurde. 
  
Gehen Sie folgendermaßen vor, um die **MAPIUID** für den erstellten Nachrichtendienst abzurufen: 
  
1. Rufen Sie die [IMsgServiceAdmin:: GetMsgServiceTable](imsgserviceadmin-getmsgservicetable.md) -Methode auf, um die Verwaltungstabelle des Nachrichtendiensts abzurufen. 
    
2. Suchen Sie die Zeile, die den Nachrichtendienst darstellt, indem Sie eine Einschränkung für die Tabelle platzieren, die mit der **PR_SERVICE_NAME** ([pidtagservicename (](pidtagservicename-canonical-property.md))-Eigenschaft mit dem Namen des Nachrichtendiensts übereinstimmt. 
    
3. Rufen Sie die **PR_SERVICE_UID** ([pidtagserviceuid (](pidtagserviceuid-canonical-property.md))-Eigenschaft des Diensts ab. 
    
4. Übergeben Sie den Wert der **PR_SERVICE_UID** -Eigenschaft im _lpUid_ -Parameter an die [IMsgServiceAdmin:: ConfigureMsgService](imsgserviceadmin-configuremsgservice.md) -Methode, um den Dienst zu konfigurieren. 
    
> [!CAUTION]
> Die Microsoft Outlook 2010-Implementierung des MAPI-Subsystems unterstützt MAPI_UNICODE nicht und schlägt fehl, wenn Sie verwendet wird. 
  
> [!IMPORTANT]
> Der _ulFlags_ -SERVICE_NO_RESTART_WARNING ist möglicherweise nicht in der herunterladbaren Headerdatei definiert, die Sie derzeit haben, in diesem Fall können Sie ihn mithilfe des folgenden Werts zu Ihrem Code hinzufügen: >`#define SERVICE_NO_RESTART_WARNING 0x00000080`
  
## <a name="mfcmapi-reference"></a>MFCMAPI-Referenz

Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.
  
|**Datei**|**Funktion**|**Comment**|
|:-----|:-----|:-----|
|MAPIProfileFunctions. cpp  <br/> |HrAddServiceToProfile  <br/> |MFCMAPI verwendet die **IMsgServiceAdmin:: CreateMsgService** -Methode, um einen Dienst zu einem Profil hinzuzufügen.  <br/> |
   
## <a name="see-also"></a>Siehe auch



[IMsgServiceAdmin : IUnknown](imsgserviceadminiunknown.md)


[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)

