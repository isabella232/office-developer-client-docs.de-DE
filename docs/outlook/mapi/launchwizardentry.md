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
  
Definiert eine Funktion, mit der die Profil-Assistentenanwendung gestartet wird, um einen oder mehrere Nachrichtendienste zu einem Profil hinzuzufügen. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapiwz. h  <br/> |
|Definierte Funktion, implementiert von:  <br/> |MAPI  <br/> |
|Definierte Funktion, aufgerufen von:  <br/> |Client Anwendungen  <br/> |
   
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
  
> in Ein Handle für das übergeordnete Fenster des Anrufers. Wenn der Aufrufer kein übergeordnetes Fenster hat, sollte der _hParentWnd_ -Parameter NULL sein. 
    
 _ulFlags_
  
> in Bitmaske von Flags, die Optionen für den Profil-Assistenten angeben. Die folgenden Flags können festgelegt werden:
    
MAPI_PW_ADD_SERVICE_ONLY 
  
> Der Profil-Assistent besteht darin, nur die Nachrichtendienste hinzuzufügen, die über den Parameter _lppszServiceNameToAdd_ aufgeführt sind, und nicht die zugehörige Seite für die Auswahl der Nachrichtendienste anzuzeigen. 
    
MAPI_PW_FIRST_PROFILE 
  
> Das zu erstellende Profil ist das erste für diese Arbeitsstation. 
    
MAPI_PW_HIDE_SERVICES_LIST 
  
> Die Seite des Profil-Assistenten zum Auswählen von Nachrichtendiensten sollte nicht angezeigt werden. 
    
MAPI_PW_LAUNCHED_BY_CONFIG 
  
> Der Profil-Assistent wurde von der Konfigurationsanwendung der Systemsteuerung gestartet. 
    
MAPI_PW_PROVIDER_UI_ONLY 
  
> Nur die Konfigurationsdialogfelder der Dienstanbieter sollten angezeigt werden, und die Seiten des Profil-Assistenten sollten nicht angezeigt werden. Dieses Flag kann nur festgelegt werden, wenn das MAPI_PW_ADD_SERVICE_ONLY-Flag festgelegt ist. 
    
 _lppszServiceNameToAdd_
  
> in Zeiger auf ein Array von Zeichenfolgen, die die Namen der Nachrichtendienste enthalten, die dem Profil hinzugefügt werden sollen. Das Array muss mit einem NULL-Wert beendet werden. 
    
 _cbBufferMax_
  
> in Die Größe des Puffers, auf den durch den _lpszNewProfileName_ -Parameter verwiesen wird. 
    
 _lpszNewProfileName_
  
> Out Zeiger auf einen Zeichenfolgenpuffer, in dem die auf **LAUNCHWIZARDENTRY** basierende Funktion den Namen des erstellten Profils zurückgibt. 
    
## <a name="return-value"></a>Rückgabewert

S_OK 
  
> Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat. 
    
MAPI_E_CALL_FAILED 
  
> Der Vorgang konnte nicht abgeschlossen werden. Zu den Möglichkeiten gehört das Initialisieren des MAPI-Subsystems für den Profil-Assistenten, das nicht zugreifen auf das Standardprofil und das Zurückgeben eines Fehlers aus dem Dialogfeld.
    
## <a name="remarks"></a>Bemerkungen

Die MAPI-Implementierung des Prototyps der **LAUNCHWIZARDENTRY** -Funktion ist der Einstiegspunkt in die MAPI-Profil-Assistentenanwendung. MAPI benennt diesen Einstiegspunkt **LaunchWizard**. 
  
Wenn das MAPI_PW_ADD_SERVICE_ONLY-Flag im Parameter _ulFlags_ festgelegt ist, gelten die folgenden Regeln: 
  
- Das MAPI_PW_LAUNCHED_BY_CONFIG-Flag verhindert, dass die Willkommensseite angezeigt wird. 
    
- Die MAPI_PW_HIDE_SERVICES_LIST-und MAPI_PW_PROVIDER_UI_ONLY-Flags sind nur dann nützlich, wenn kein Standardprofil vorhanden ist. In diesem Fall bestimmen diese Flags, welche Seite des Profil-Assistenten angezeigt werden soll. 
    
- Wenn ein Standardprofil vorhanden ist, werden keine der Profil-Assistentenseiten angezeigt. 
    
- Wenn ein Standardprofil vorhanden ist, wird nur ein Nachrichtendienst über den Parameter _lppszServiceNameToAdd_ aufgeführt, und der Nachrichtendienst befindet sich bereits im Standardprofil, der Profil-Assistent gibt S_OK zurück, ohne dem Profil etwas hinzuzufügen. 
    
Für jeden Nachrichtendienst, der dem Profil hinzugefügt werden soll, ruft der Profil-Assistent die Einstiegspunktfunktion des Diensts auf der Grundlage des [MSGSERVICEENTRY](msgserviceentry.md) -Prototyps auf. Für jeden von einem Nachrichtendienst ausgewählten Dienstanbieter, der dem Profil hinzugefügt werden soll, ruft der Profil-Assistent die Einstiegspunktfunktion des Anbieters basierend auf dem [WIZARDENTRY](wizardentry.md) -Prototypen auf. Während der interaktiven Konfiguration führt jedes Benutzerereignis auf den Eigenschaftenseiten dazu, dass der Profil-Assistent die Rückruffunktion des Anbieters basierend auf dem [SERVICEWIZARDDLGPROC](servicewizarddlgproc.md) -Prototyp aufruft. 
  
Wenn ein Dienstanbieter, der dem Profil hinzugefügt wird, die Profil-Assistentenseiten unterstützt, muss die programmgesteuerte Konfiguration des Profils zugelassen werden.
  

