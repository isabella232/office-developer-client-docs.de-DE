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
    
 _lpuidService_
  
> Out Der Zeiger auf die UID des hinzugefügten Nachrichtendiensts.
    
## <a name="return-value"></a>Rückgabewert

S_OK
  
> Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.
    
MAPI_E_NOT_FOUND
  
> Der Name des Nachrichtendiensts befindet sich nicht im Abschnitt **[Dienste]** von MapiSvc. inf. 
    
## <a name="remarks"></a>Bemerkungen

Mit der **IMsgServiceAdmin2:: CreateMsgServiceEx** -Methode wird dem aktuellen Profil ein Nachrichtendienst hinzugefügt. **CreateMsgServiceEx** Ruft die Einstiegspunktfunktion des Nachrichtendiensts auf, um dienstspezifische Konfigurationsaufgaben auszuführen. Wenn das SERVICE_UI_ALLOWED-Flag im Parameter _ulFlags_ festgelegt ist, kann der zu installierende Nachrichtendienst ein Eigenschaftenfenster anzeigen, das es dem Benutzer ermöglicht, seine Einstellungen zu konfigurieren. 
  
Die Datei MapiSvc. inf enthält die Liste der Anbieter, aus denen sich ein Nachrichtendienst zusammensetzen, und die jeweiligen Eigenschaften. **CreateMsgServiceEx** erstellt zunächst einen neuen Profil Abschnitt für den Nachrichtendienst und kopiert dann alle Informationen für diesen Dienst aus der Datei MapiSvc. inf in das Profil, sodass für jeden Anbieter neue Abschnitte erstellt werden. 
  
Nachdem alle Informationen aus MapiSvc. inf kopiert wurden, wird die Einstiegspunktfunktion des Nachrichtendiensts, **MSGSERVICEENTRY**, mit dem MSG_SERVICE_CREATE-Wert aufgerufen, der im Parameter _ulContext_ festgelegt ist. Wenn das SERVICE_UI_ALLOWED-Flag im _ulFlags_ -Parameter der **CreateMsgServiceEx** -Methode festgelegt ist, werden die Werte in den Parametern _ulUIParam_ und _ulFlags_ auch übergeben, wenn die Einstiegspunktfunktion des Nachrichtendiensts aufgerufen wird. Dienstanbieter sollten Ihre Konfigurationseigenschaften Blätter anzeigen, damit Benutzer den Nachrichtendienst konfigurieren können. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Wenn das Argument **CreateMsgServiceEx** _lpuidService_ nicht NULL ist, wird die **PR_SERVICE_UID** ([pidtagserviceuid (](pidtagserviceuid-canonical-property.md))-Eigenschaft des Nachrichtendiensts, der dem Profil hinzugefügt wurde, in der **GUID** zurückgegeben, auf die es zeigt. 
  
Übergeben Sie den Wert der **PR_SERVICE_UID** -Eigenschaft im _lpuidService_ -Parameter an die [IMsgServiceAdmin:: ConfigureMsgService](imsgserviceadmin-configuremsgservice.md) -Methode, um den Dienst zu konfigurieren. 
  
> [!CAUTION]
> Die Microsoft Outlook 2010-Implementierung des MAPI-Subsystems unterstützt MAPI_UNICODE nicht und schlägt fehl, wenn Sie verwendet wird. 
  
> [!IMPORTANT]
> Die IMsgServiceAdmin2-Schnittstelle wird durch das gleiche Objekt verfügbar gemacht, das die IMsgServiceAdmin-Schnittstelle implementiert, und ist in der Outlook-Implementierung des MAPI-Subsystems seit Outlook 2003 verfügbar. Die IID ist wie folgt definiert: > `#if !defined(INITGUID) || defined(USES_IID_IMsgServiceAdmin2)` >   `DEFINE_OLEGUID(IID_IMsgServiceAdmin2,0x00020387, 0, 0);`> der _ulFlags_ -SERVICE_NO_RESTART_WARNING ist möglicherweise nicht in der herunterladbaren Headerdatei definiert, die Sie derzeit haben, in diesem Fall können Sie ihn mithilfe des folgenden Werts zu Ihrem Code hinzufügen: >`#define SERVICE_NO_RESTART_WARNING 0x00000080`
  
## <a name="see-also"></a>Siehe auch



[IMsgServiceAdmin2 : IMsgServiceAdmin](imsgserviceadmin2imsgserviceadmin.md)


[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)

