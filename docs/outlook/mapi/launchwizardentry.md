---
title: LAUNCHWIZARDENTRY
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.LAUNCHWIZARDENTRY
api_type:
- COM
ms.assetid: 5778dffa-f01b-46b3-9c19-862793740918
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: f2cc9a6f97fa51a255f8c24c2bb52c912aef7718
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22566250"
---
# <a name="launchwizardentry"></a>LAUNCHWIZARDENTRY

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Definiert eine Funktion, die die Anwendung-Profil-Assistent zum Hinzufügen von mindestens eine Nachricht-Diensten zu einem Profil gestartet wird. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapiwz.h  <br/> |
|Definierte Funktion von implementiert:  <br/> |MAPI  <br/> |
|Definierte Funktion aufgerufen:  <br/> |Clientanwendungen  <br/> |
   
```cpp
HRESULT LAUNCHWIZARDENTRY(
  HWND hParentWnd,
  ULONG ulFlags,
  LPCSTR FAR * lppszServiceNameToAdd,
  ULONG cbBufferMax,
  LPSTR lpszNewProfileName
);
```

## <a name="parameters"></a>Parameter

 _hParentWnd_
  
> [in] Ein Handle für den Anrufer übergeordnetes Fenster. Wenn der Aufrufer übergeordnetes Fenster nicht vorhanden ist, sollte der _hParentWnd_ -Parameter auf NULL sein. 
    
 _ulFlags_
  
> [in] Bitmaske der Flags, die Optionen für den Assistenten-Profil angeben. Die folgenden Kennzeichen können festgelegt werden:
    
MAPI_PW_ADD_SERVICE_ONLY 
  
> Der Profil-Assistent ist nur die Message-Dienste aufgeführt, die über den _LppszServiceNameToAdd_ -Parameter hinzufügen und zeigen auf der Seite für die Auswahl von Message-Dienste nicht. 
    
MAPI_PW_FIRST_PROFILE 
  
> Das zu erstellende Profil ist der erste für diese Arbeitsstation. 
    
MAPI_PW_HIDE_SERVICES_LIST 
  
> Der Profil-Assistent-Seite für die Auswahl von Message Dienste sollte nicht angezeigt werden. 
    
MAPI_PW_LAUNCHED_BY_CONFIG 
  
> Der Profil-Assistent wurde von der Systemsteuerung Konfiguration Anwendung gestartet. 
    
MAPI_PW_PROVIDER_UI_ONLY 
  
> Nur die Dienstanbieter Konfigurationsdialogfelder angezeigt werden sollen, und der Profil-Assistent Seiten sollte nicht angezeigt werden. Dieses Kennzeichen können nur festgelegt werden, wenn das Flag MAPI_PW_ADD_SERVICE_ONLY festgelegt ist. 
    
 _lppszServiceNameToAdd_
  
> [in] Zeiger auf ein Array von Zeichenfolgen mit den Namen der Nachrichtendienste, die dem Profil hinzugefügt werden soll. Das Array muss mit einem NULL-Wert enden. 
    
 _cbBufferMax_
  
> [in] Größe des Puffers, auf den durch den Parameter _LpszNewProfileName_ verwiesen wird. 
    
 _lpszNewProfileName_
  
> [out] Zeiger auf einen Puffer vom Typ String, in dem die Funktion basierend auf **LAUNCHWIZARDENTRY** den Namen des erstellten Profils zurückgibt. 
    
## <a name="return-value"></a>R�ckgabewert

S_OK 
  
> Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat. 
    
MAPI_E_CALL_FAILED 
  
> Ein Fehler unerwartete oder unbekannten Ursprungs verhindert den Abschluss des Vorgangs. Mögliche Werte Fehler beim Initialisieren des MAPI-Subsystems für den Benutzerprofildienst-Assistenten eingeschlossen, der Fehler beim Zugriff auf das Standardprofil und einen Fehler zurück, aus dem Dialogfeld.
    
## <a name="remarks"></a>HinwBemerkungeneise

Die MAPI-Implementierung der Funktion **LAUNCHWIZARDENTRY** Prototyp ist der Einstiegspunkt in die Anwendung MAPI-Profil-Assistent. Den Namen dieser Einstiegspunkt **LaunchWizard**MAPI. 
  
Wenn das Flag MAPI_PW_ADD_SERVICE_ONLY im _UlFlags_ -Parameter festgelegt ist, gelten die folgenden Regeln: 
  
- Das Flag MAPI_PW_LAUNCHED_BY_CONFIG unterdrückt die Seite Willkommen angezeigt wird. 
    
- Die Flags MAPI_PW_HIDE_SERVICES_LIST und MAPI_PW_PROVIDER_UI_ONLY eignen sich nur, wenn kein Standardprofil vorhanden ist. In diesem Fall bestimmen diese Flags welche-Profil-Assistent Seite ist, angezeigt werden soll. 
    
- Wenn ein Standardprofil vorhanden ist, werden keine der Profil-Assistent Seiten angezeigt werden soll. 
    
- Wenn ein Standardprofil vorhanden ist, wird nur eine Nachricht-Dienst über den Parameter _LppszServiceNameToAdd_ aufgeführt, und Messagingdiensts bereits im Standardprofil lautet, gibt der Profil-Assistent S_OK zurück, ohne das Profil nichts hinzufügen. 
    
Für jeden Nachrichtendienst, die dem Profil hinzugefügt werden soll ruft der Profil-Assistent des Dienstes Eintrag Funktion basierend auf den [MSGSERVICEENTRY](msgserviceentry.md) Prototyp. Für jede Dienstanbieter ausgewählt aus einem Nachrichtendienst, die dem Profil hinzugefügt werden soll ruft der Profil-Assistent des Anbieters Eintrag Funktion basierend auf den [WIZARDENTRY](wizardentry.md) Prototyp. Während der interaktiven Konfiguration bewirkt, dass jedes Benutzerereignis in die Eigenschaftenseiten Profil des Anbieters Callback-Funktion basierend auf den Prototyp [SERVICEWIZARDDLGPROC](servicewizarddlgproc.md) aufrufen. 
  
Wenn ein Dienstanbieter, die dem Profil hinzugefügt wird die Seiten des Assistenten Profil unterstützt, müssen sie programmgesteuerte Konfiguration des Profils zulassen.
  

