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
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 3aae61f7b21c507da7955dbb4393d13bfb5fa24c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792604"
---
# <a name="imsgserviceadmin2createmsgserviceex"></a>IMsgServiceAdmin2::CreateMsgServiceEx

  
  
**Betrifft**: Outlook 
  
Fügt einen Nachrichtendienst gibt, die Dienst-UID neu hinzugefügt und der aktuellen Profil hinzu.
  
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
    
 _lpuidService_
  
> [out] Der Zeiger auf die UID des Diensts Nachricht hinzugefügt.
    
## <a name="return-value"></a>R�ckgabewert

S_OK
  
> Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.
    
MAPI_E_NOT_FOUND
  
> Der Dienstname Nachricht ist nicht in der MapiSvc.inf im Abschnitt **[Services]** . 
    
## <a name="remarks"></a>Bemerkungen

Die **IMsgServiceAdmin2::CreateMsgServiceEx** -Methode wird das aktuelle Profil ein Messagingdiensts hinzugefügt. **CreateMsgServiceEx** Ruft die Messagingdiensts Eintrag Point-Funktion, um alle dienstspezifische Konfigurationsaufgaben ausführen. Wenn das Flag SERVICE_UI_ALLOWED im _UlFlags_ -Parameter festgelegt ist, kann der Message-Dienst installiert wird ein Eigenschaftenblatt durch den Benutzer zum Konfigurieren der Einstellungen anzeigen. 
  
Die Datei "MapiSvc.inf" enthält die Liste der Anbieter, die eine Message Service und die Eigenschaften für jede bilden. **CreateMsgServiceEx** zuerst erstellt einen neuen Profilabschnitt für den Dienst und kopiert alle Informationen für den betreffenden Dienst aus der Datei "MapiSvc.inf" in das Profil neue Abschnitte für jeden Anbieter erstellen. 
  
Nachdem alle Informationen aus MapiSvc.inf kopiert wurde, wird die Messagingdiensts Eintrag Point-Funktion, **MSGSERVICEENTRY**, mit dem Wert MSG_SERVICE_CREATE im _UlContext_ -Parameter aufgerufen. Wenn das Flag SERVICE_UI_ALLOWED in die **CreateMsgServiceEx** -Methode _UlFlags_ Parameter festgelegt ist, werden die Werte in den _UlUIParam_ und _UlFlags_ auch übergeben, wenn die Messagingdiensts Eintrag Point-Funktion aufgerufen wird. Dienstanbieter sollte ihre Konfiguration Eigenschaftenseiten angezeigt werden, damit Benutzer den Nachrichtendienst konfigurieren zu können. 
  
## <a name="notes-to-callers"></a>Hinweise für Aufrufer

Wenn Arguments _LpuidService_ **CreateMsgServiceEx** nicht NULL ist, wird die **PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md))-Eigenschaft des Diensts Nachricht, die dem Profil hinzugefügt wurde, die **GUID** zurückgegeben, auf die sie zeigt. 
  
Übergeben Sie den Wert der Eigenschaft **PR_SERVICE_UID** im _LpuidService_ -Parameter an die [IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md) -Methode zum Konfigurieren des Diensts. 
  
> [!CAUTION]
> Die Microsoft Outlook 2010-Implementierung des MAPI-Subsystems unterstützt keine Parameter MAPI_UNICODE und schlägt fehl, wenn sie verwendet wird. 
  
> [!IMPORTANT]
> Die IMsgServiceAdmin2-Schnittstelle wird durch das gleiche Objekt verfügbar gemacht, die die IMsgServiceAdmin-Schnittstelle implementiert und wurde mithilfe des Outlook-Implementierung des MAPI-Subsystems seit Outlook 2003 zur Verfügung. Die IID wird wie folgt definiert: > `#if !defined(INITGUID) || defined(USES_IID_IMsgServiceAdmin2)` >   `DEFINE_OLEGUID(IID_IMsgServiceAdmin2,0x00020387, 0, 0);`> _UlFlags_ SERVICE_NO_RESTART_WARNING möglicherweise nicht in der herunterladbaren Headerdatei derzeit definiert werden, in diesem Fall können Sie es dem Code mit dem folgenden Wert hinzufügen: >`#define SERVICE_NO_RESTART_WARNING 0x00000080`
  
## <a name="see-also"></a>Siehe auch



[IMsgServiceAdmin2 : IMsgServiceAdmin](imsgserviceadmin2imsgserviceadmin.md)


[MFCMAPI (engl.) als ein Codebeispiel](mfcmapi-as-a-code-sample.md)

