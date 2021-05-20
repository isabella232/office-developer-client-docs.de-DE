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
ms.openlocfilehash: c1509918eb587c17deebf95317cf57b4ab19928a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437385"
---
# <a name="launchwizardentry"></a>LAUNCHWIZARDENTRY

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Definiert eine Funktion, mit der die Anwendung des Profil-Assistenten gestartet wird, um einem Profil einen oder mehrere Nachrichtendienste hinzufügen zu können. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapiwz.h  <br/> |
|Definierte Funktion implementiert von:  <br/> |MAPI  <br/> |
|Definierte Funktion, die von:  <br/> |Clientanwendungen  <br/> |
   
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
  
> [in] Ein Handle zum übergeordneten Fenster des Anrufers. Wenn der Aufrufer kein übergeordnetes Fenster hat, sollte  _der hParentWnd-Parameter_ NULL sein. 
    
 _ulFlags_
  
> [in] Bitmaske mit Flags, die Optionen für den Profil-Assistenten angibt. Die folgenden Kennzeichen können festgelegt werden:
    
MAPI_PW_ADD_SERVICE_ONLY 
  
> Der Profil-Assistent fügt nur die Nachrichtendienste hinzu, die über den  _lppszServiceNameToAdd-Parameter_ aufgelistet sind, und nicht seine Seite zum Auswählen von Nachrichtendiensten anzeigen. 
    
MAPI_PW_FIRST_PROFILE 
  
> Das zu erstellende Profil ist das erste für diese Arbeitsstation. 
    
MAPI_PW_HIDE_SERVICES_LIST 
  
> Die Seite des Profil-Assistenten zum Auswählen von Nachrichtendiensten sollte nicht angezeigt werden. 
    
MAPI_PW_LAUNCHED_BY_CONFIG 
  
> Der Profil-Assistent wurde von der Systemsteuerungskonfigurationsanwendung gestartet. 
    
MAPI_PW_PROVIDER_UI_ONLY 
  
> Es sollten nur die Konfigurationsdialogfelder der Dienstanbieter angezeigt werden, und die Seiten des Profil-Assistenten sollten nicht angezeigt werden. Dieses Flag kann nur festgelegt werden, wenn MAPI_PW_ADD_SERVICE_ONLY festgelegt ist. 
    
 _lppszServiceNameToAdd_
  
> [in] Zeiger auf ein Array von Zeichenfolgen, das die Namen der Nachrichtendienste enthält, die dem Profil hinzugefügt werden sollen. Das Array muss mit einem NULL-Wert beendet werden. 
    
 _cbBufferMax_
  
> [in] Die Größe des Puffers, auf den der  _lpszNewProfileName-Parameter_ verweist. 
    
 _lpszNewProfileName_
  
> [out] Zeiger auf einen Zeichenfolgenpuffer, in dem die auf **LAUNCHWIZARDENTRY** basierende Funktion den Namen des erstellten Profils zurückgibt. 
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat. 
    
MAPI_E_CALL_FAILED 
  
> Ein Fehler mit unerwartetem oder unbekanntem Ursprung verhinderte den Abschluss des Vorgangs. Zu den Möglichkeiten gehören das Nicht initialisieren des MAPI-Subsystems für den Profil-Assistenten, der Nichtzugriff auf das Standardprofil und eine Fehlerrückskehr aus dem Dialogfeld.
    
## <a name="remarks"></a>Hinweise

Die MAPI-Implementierung des **LAUNCHWIZARDENTRY-Funktionsprototyps** ist der Einstiegspunkt in die MAPI-Profil-Assistenten-Anwendung. MAPI benennt diesen Einstiegspunkt **LaunchWizard**. 
  
Wenn das MAPI_PW_ADD_SERVICE_ONLY im  _ulFlags-Parameter_ festgelegt ist, gelten die folgenden Regeln: 
  
- Das MAPI_PW_LAUNCHED_BY_CONFIG verhindert, dass die Willkommensseite angezeigt wird. 
    
- Die MAPI_PW_HIDE_SERVICES_LIST und MAPI_PW_PROVIDER_UI_ONLY sind nur nützlich, wenn kein Standardprofil vorlag. In diesem Fall bestimmen diese Kennzeichen, welche Seite des Profil-Assistenten angezeigt werden soll. 
    
- Wenn ein Standardprofil vorhanden ist, wird keine der Seiten des Profil-Assistenten angezeigt. 
    
- Wenn ein Standardprofil vorhanden ist, nur ein Nachrichtendienst über den  _lppszServiceNameToAdd-Parameter_ aufgelistet wird und sich dieser Nachrichtendienst bereits im Standardprofil befindet, gibt der Profil-Assistent S_OK zurück, ohne dem Profil etwas hinzufügen zu müssen. 
    
Damit jeder Nachrichtendienst dem Profil hinzugefügt werden kann, ruft der Profil-Assistent die Einstiegspunktfunktion des Diensts basierend auf dem [MSGSERVICEENTRY-Prototyp](msgserviceentry.md) auf. Für jeden Dienstanbieter, der aus einem Nachrichtendienst ausgewählt wurde, der dem Profil hinzugefügt werden soll, ruft der Profil-Assistent die Einstiegspunktfunktion des Anbieters basierend auf dem [WIZARDENTRY-Prototyp](wizardentry.md) auf. Während der interaktiven Konfiguration führt jedes Benutzerereignis auf den Eigenschaftenseiten dazu, dass der Profil-Assistent die Rückruffunktion des Anbieters basierend auf dem [SERVICEWIZARDDLGPROC-Prototyp](servicewizarddlgproc.md) aufruft. 
  
Wenn ein Dienstanbieter, der dem Profil hinzugefügt wird, die Seiten des Profil-Assistenten unterstützt, muss er die programmgesteuerte Konfiguration des Profils zulassen.
  

