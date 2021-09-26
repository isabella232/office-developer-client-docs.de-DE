---
title: IMsgServiceAdmin2CreateMsgServiceEx
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMsgServiceAdmin2.CreateMsgServiceEx
api_type:
- COM
ms.assetid: 4910dabd-9380-4fde-a440-5c64d74c0bba
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 3317c3c1ed4eed28e12215aac7e64595be094d22
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59620702"
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
  
> Beim Hinzufügen eines neuen Nachrichtendiensts zum Profil bestimmt das MAPI-Subsystem basierend auf verschiedenen Umständen und Kriterien häufig, dass für diese Aktion ein Neustart von Outlook erforderlich ist. Wenn das SERVICE_NO_RESTART_WARNING Flag nicht enthalten ist und die Benutzeroberfläche – basierend auf den Flags SERVICE_UI_ALWAYS und SERVICE_UI_ALLOWED – zulässig ist und mindestens ein Prozess am aktuellen Profil angemeldet ist, zeigt diese Funktion die Meldung an: "Sie müssen Outlook neu starten, damit diese Änderungen wirksam werden." Durch Das Einschließen der SERVICE_NO_RESTART_WARNING-Kennzeichnung wird die Anzeige dieser Warnmeldung unterdrückt.
    
SERVICE_UI_ALLOWED
  
> Die Konfigurations-UI des Nachrichtendiensts ist bei Bedarf zulässig.
    
SERVICE_UI_ALWAYS
  
> Der Nachrichtendienst zeigt das Konfigurationseigenschaftenblatt an.
    
 _lpuidService_
  
> [out] Der Zeiger auf die UID des hinzugefügten Nachrichtendiensts.
    
## <a name="return-value"></a>Rückgabewert

S_OK
  
> Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.
    
MAPI_E_NOT_FOUND
  
> Der Name des Nachrichtendiensts befindet sich nicht im Abschnitt **[Dienste]** von MapiSvc.inf. 
    
## <a name="remarks"></a>Bemerkungen

Die **IMsgServiceAdmin2::CreateMsgServiceEx-Methode** fügt dem aktuellen Profil einen Nachrichtendienst hinzu. **CreateMsgServiceEx** ruft die Einstiegspunktfunktion des Nachrichtendiensts auf, um dienstspezifische Konfigurationsaufgaben auszuführen. Wenn das flag SERVICE_UI_ALLOWED im  _UlFlags-Parameter_ festgelegt ist, kann der installierte Nachrichtendienst ein Eigenschaftenblatt anzeigen, mit dem der Benutzer seine Einstellungen konfigurieren kann. 
  
Die Datei MapiSvc.inf enthält die Liste der Anbieter, aus denen ein Nachrichtendienst besteht, sowie die Jeweiligen Eigenschaften. **CreateMsgServiceEx** erstellt zuerst einen neuen Profilabschnitt für den Nachrichtendienst und kopiert dann alle Informationen für diesen Dienst aus der Datei MapiSvc.inf in das Profil, wodurch neue Abschnitte für jeden Anbieter erstellt werden. 
  
Nachdem alle Informationen aus MapiSvc.inf kopiert wurden, wird die Einstiegspunktfunktion des Nachrichtendiensts, **MSGSERVICEENTRY,** mit dem im  _ulContext-Parameter_ festgelegten MSG_SERVICE_CREATE Wert aufgerufen. Wenn das flag SERVICE_UI_ALLOWED im _ulFlags-Parameter_ der **CreateMsgServiceEx-Methode** festgelegt ist, werden auch die Werte in den _Parametern ulUIParam_ und _ulFlags_ übergeben, wenn die Einstiegspunktfunktion des Nachrichtendiensts aufgerufen wird. Dienstanbieter sollten ihre Konfigurationseigenschaftenblätter anzeigen, damit Benutzer den Nachrichtendienst konfigurieren können. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Wenn das **CreateMsgServiceEx** _lpuidService-Argument_ nicht NULL ist, wird die **PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)) -Eigenschaft des Nachrichtendiensts, der dem Profil hinzugefügt wurde, in der **GUID** zurückgegeben, auf die es zeigt. 
  
Übergeben Sie den Wert der **PR_SERVICE_UID-Eigenschaft** im  _Parameter "lpuidService"_ an die [IMsgServiceAdmin::ConfigureMsgService-Methode,](imsgserviceadmin-configuremsgservice.md) um den Dienst zu konfigurieren. 
  
> [!CAUTION]
> Die Microsoft Outlook 2010 Implementierung des MAPI-Subsystems unterstützt MAPI_UNICODE nicht und schlägt fehl, wenn sie verwendet wird. 
  
> [!IMPORTANT]
> Die IMsgServiceAdmin2-Schnittstelle wird von demselben Objekt verfügbar gemacht, das die IMsgServiceAdmin-Schnittstelle implementiert, und ist seit Outlook 2003 über die Implementierung des MAPI-Subsystems Outlook verfügbar. Die IID ist wie folgt definiert: > `#if !defined(INITGUID) || defined(USES_IID_IMsgServiceAdmin2)` >   `DEFINE_OLEGUID(IID_IMsgServiceAdmin2,0x00020387, 0, 0);`> Die _ulFlags-SERVICE_NO_RESTART_WARNING_ ist möglicherweise nicht in der herunterladbaren Headerdatei definiert, die Sie derzeit haben. In diesem Fall können Sie sie ihrem Code mit dem folgenden Wert hinzufügen: >`#define SERVICE_NO_RESTART_WARNING 0x00000080`
  
## <a name="see-also"></a>Siehe auch



[IMsgServiceAdmin2 : IMsgServiceAdmin](imsgserviceadmin2imsgserviceadmin.md)


[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)

